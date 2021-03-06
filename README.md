# ocaml-imap -- a client IMAP4rev1 library for OCaml

`ocaml-imap` is a non-blocking IMAP codec to decode and encode the IMAP4rev1
email protocol.

`ocaml-imap` is made of a single module `Imap` and distributed under the MIT
license. Its only dependencies are [Uutf](https://github.com/dbuenzli/uutf),
[Base64](https://github.com/mirage/ocaml-base64), and
[Uint](https://github.com/andrenth/ocaml-uint).

Home page: https://github.com/nojb/ocaml-imap

Contact: Nicolas Ojeda Bar `<n.oje.bar@gmail.com>`

## Installation

`ocaml-imap` can be installed with `opam`:

    opam install imap

If you don't use `opam` consult the [`opam`](opam) file for build
instructions and a complete specification of the dependencies.

## Documentation

The documentation and API reference is automatically generated by `ocamldoc`
from `imap.mli`. It can be consulted [online](https://nojb.github.io/ocaml-imap).
It can also be generated with:

    make doc

and accessed at `api.docdir/index.html`.

## Sample programs

Sample programs are located in the `test` directory of the
distribution. They can be built with:

    make test

The resulting binaries are in the root directory:

- `wait_mail.native` is a simple utility that alerts the user of new arrived
  mail in a chosen mailbox.  Depends on [Cmdliner] and [Ssl].
- `imap_shell.native` is a small ineractive shell that can be used to interact
  with IMAP servers in order to test the library and experiment with the
  protocol.  Invoke with `--help` for more information. Depends on [Cmdliner],
  [Ssl] and [Lwt].

[Cmdliner]: http://erratique.ch/software/cmdliner
[Ssl]: https://github.com/savonet/ocaml-ssl
[Lwt]: http://ocsigen.org/lwt/
