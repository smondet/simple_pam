simple_pam
==========

Tiny binding around PAM


## Installation:

    oasis setup
    ocaml setup.ml -configure [--prefix <prefix]
    ocaml setup.ml -build
    ocaml setup.ml -install

## Usage

There is only one function:

    Simple_pam.authenticate "service" "user" "password"

if it returns <tt>()</tt>, then the user/password is valid for the given service definition (usually <tt>/etc/pam/&lt;service&gt;</tt>).

if it throws a Failure exception, then the user, password, or service are wrong :)


# Author(s):

The code in `src/lib/simple_pam_stubs.c` has been extracted from XEN-API:
https://github.com/xen-org/xen-api

    Copyright (C) 2006-2009 Citrix Systems Inc.

Sebastien Mondet (http://seb.mondet.org)

