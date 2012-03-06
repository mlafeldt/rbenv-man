rbenv-man
=========

rbenv-man is a plugin for [rbenv] to easily access the man pages for the
currently set Ruby version, e.g. `ruby(1)` and `irb(1)`.

Technically, rbenv-man is a wrapper for `man(1)` that takes care of using the
correct `MANPATH`.

Note: To view a gem's man page, install [gem-man].


Installation
------------

To install rbenv-man, clone this repository into your `~/.rbenv/plugins`
directory. (You'll need a recent version of rbenv that supports plugin
bundles.)

    $ mkdir -p ~/.rbenv/plugins
    $ cd ~/.rbenv/plugins
    $ git clone git://github.com/mlafeldt/rbenv-man.git


Usage
-----

Simply use rbenv-man in the same way as `man(1)`.

Show `ruby(1)` manual:

    $ rbenv man ruby

Show `ri(1)` manual:

    $ rbenv man 1 ri

Print location of `ruby(1)` manual:

    $ rbenv man -w ruby
    /home/mlafeldt/.rbenv/versions/1.9.2-p290/share/man/man1/ruby.1

Change Ruby version and print new location of man page:

    $ rbenv global 1.9.3-p0
    $ rbenv man -w ruby
    /home/mlafeldt/.rbenv/versions/1.9.3-p0/share/man/man1/ruby.1


License
-------

rbenv-man is licensed under the terms of the MIT License. See [LICENSE] file.


Contact
-------

* Web: <https://github.com/mlafeldt/rbenv-man>
* Mail: <mathias.lafeldt@gmail.com>
* Twitter: [@mlafeldt](https://twitter.com/mlafeldt)


[LICENSE]: https://github.com/mlafeldt/rbenv-man/blob/master/LICENSE
[gem-man]: https://github.com/defunkt/gem-man
[rbenv]: https://github.com/sstephenson/rbenv
