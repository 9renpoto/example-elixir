[Codecov][1] Elixir Example
=======================

[![Build Status](https://travis-ci.org/codecov/example-elixir.svg?branch=master)](https://travis-ci.org/codecov/example-elixir) [![codecov](https://codecov.io/gh/codecov/example-elixir/branch/master/graph/badge.svg?token=)](https://codecov.io/gh/codecov/example-elixir)

This repository serves as an **example** on how to use [Codecov Global][4] for Elixir.

# Mix.exs

Add [excoveralls](https://hex.pm/packages/excoveralls) to your mix.exs deps.

# Travis CI

Add to your `.travis.yml` file.
```yml
language: elixir
elixir:
  - 1.3.4
otp_release:
  - 19.1

script:
  - MIX_ENV=test mix do compile --warnings-as-errors, coveralls.json

after_success:
  - bash <(curl -s https://codecov.io/bash)
```

See the [Travis CI documentation](https://docs.travis-ci.com/user/languages/elixir/) for more information.


View source and learn more about [Codecov Global Uploader][4]

We are happy to help if you have any questions. Please contact email our Support at [support@codecov.io](mailto:support@codecov.io)

[1]: https://codecov.io/
[4]: https://github.com/codecov/codecov-bash
