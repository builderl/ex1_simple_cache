An example project that demonstrates various features of the `builderl` tool.

https://github.com/yoonka/builderl

This project can also be used as a template, whether or not you intend to use
`builderl`, to create your own Erlang projects.

Applications are based on chapter 11 of the excellent book
Erlang and OTP in Action.

https://github.com/erlware/Erlang-and-OTP-in-Action-Source/tree/master/chapter_11

This example consists of six applications:
* `builderl_sample_setup` is a helper application used by builderl to configure
  installed nodes
* `http_interface` / `builderl_sample_http_if` and
  `tcp_interface` / `builderl_sample_tcp_if` are example applications that this
  project installs in separate nodes named `htif` and `tcif`.
* `gen_web_server`, `resource_discovery`, and `simple_cache` are example
  applications included in this project's lib folder.

In this iteration the project can be compiled and the nodes installed
and started. That's what has been tested. In future iterations the applications
will be updated to actually provide the functionality as intended by the book.

Note: The main node that contains the `simple_cache` application is installed
as a pair of nodes with a shared mnesia scheme mainly for demonstration
purposes.

For a quick start (try `gmake` if `make` doesn't cut the mustard):

    make get-deps
    make rel
    ./bin/init.esh
    ./bin/start.esh
    to_erl ../sc-1/shell/
