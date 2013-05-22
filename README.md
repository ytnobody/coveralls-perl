# NAME

Devel::Cover::Report::Coveralls - coveralls backend for Devel::Cover

# USAGE

1\. Add your repo to coveralls. https://coveralls.io/repos/new

2\. Add setting to .travis.yaml (before\_install and script section)

    language: perl
    perl:
      - 5.16.3
      - 5.14.4
    before_install:
      cpanm -n Devel::Cover::Report::Coveralls
    script:
      perl Build.PL && ./Build build && cover -test -report coveralls

3\. push new change to github

4\. updated coveralls your project page

<img src="http://kan.github.io/images/p5-ltsv.png" />

## another CI

1\. Get repo\_token from your project page in coveralls.

2\. Write .coveralls.yml (don't add this to public repo)

    repo_token: xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

3\. Run CI.

# DESCRIPTION

[https://coveralls.io/](https://coveralls.io/) is service to publish your coverage stats online with a lot of nice features. This module provides seamless integration with [Devel::Cover](http://search.cpan.org/perldoc?Devel::Cover) in your perl projects.

# SEE ALSO

[https://coveralls.io/](https://coveralls.io/)
[https://coveralls.io/docs](https://coveralls.io/docs)
[https://github.com/coagulant/coveralls-python](https://github.com/coagulant/coveralls-python)
[Devel::Cover](http://search.cpan.org/perldoc?Devel::Cover)

# LICENSE

Copyright (C) Kan Fushihara

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# AUTHOR

Kan Fushihara <kan.fushihara@gmail.com>
