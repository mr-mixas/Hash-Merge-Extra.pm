# NAME

Hash::Merge::Extra - Collection of extra behaviors for [Hash::Merge](https://metacpan.org/pod/Hash::Merge)

<a href="https://travis-ci.org/mr-mixas/Hash-Merge-Extra.pm"><img src="https://travis-ci.org/mr-mixas/Hash-Merge-Extra.pm.svg?branch=master" alt="Travis CI"/></a>
<a href='https://coveralls.io/github/mr-mixas/Hash-Merge-Extra.pm?branch=master'><img src='https://coveralls.io/repos/github/mr-mixas/Hash-Merge-Extra.pm/badge.svg?branch=master' alt='Coverage Status'/></a>
<a href="https://badge.fury.io/pl/Hash-Merge-Extra"><img src="https://badge.fury.io/pl/Hash-Merge-Extra.svg" alt="CPAN version"/></a>

# VERSION

Version 0.05

# SYNOPSIS

    use Hash::Merge qw(merge);
    use Hash::Merge::Extra;

    Hash::Merge::set_behavior('R_OVERRIDE');

    $result = merge($left, $right);

# EXPORT

Nothing is exported.

All behaviors registered in [Hash::Merge](https://metacpan.org/pod/Hash::Merge) if used as

    use Hash::Merge::Extra;

Nothing registered if passed empty list:

    use Hash::Merge::Extra qw();

Only specified behaviors registered if list defined:

    use Hash::Merge::Extra qw(L_OVERRIDE R_REPLACE);

# BEHAVIORS

- __L\_ADDITIVE__, __R\_ADDITIVE__

    Hashes merged, arrays joined, undefined scalars overrided. Left and right
    precedence.

- __L\_MERGE\_PATCH__, __R\_MERGE\_PATCH__

    JSON Merge Patch ([rfc7386](https://tools.ietf.org/html/rfc7386)) patch
    behavior for perl structures. Almost the same as `L_OVERRIDE` and
    `R_OVERRIDE`, but hash keys with `undef` values in the patch cause removal of
    existing keys in the main structure. Left and right precedence.

- __L\_OVERRIDE__, __R\_OVERRIDE__

    Hashes merged, arrays and scalars overrided. Left and right precedence.

- __L\_REPLACE__, __R\_REPLACE__

    Nothing merged. One thing simply replaced by another. Left and right
    precedence.

# AUTHOR

Michael Samoglyadov, `<mixas at cpan.org>`

# BUGS

Please report any bugs or feature requests to
[https://github.com/mr-mixas/Hash-Merge-Extra.pm/issues](https://github.com/mr-mixas/Hash-Merge-Extra.pm/issues)

# SEE ALSO

[Hash::Merge](https://metacpan.org/pod/Hash::Merge)

# LICENSE AND COPYRIGHT

Copyright 2017 Michael Samoglyadov.

This program is free software; you can redistribute it and/or modify it
under the terms of either: the GNU General Public License as published
by the Free Software Foundation; or the Artistic License.

See [http://dev.perl.org/licenses/](http://dev.perl.org/licenses/) for more information.
