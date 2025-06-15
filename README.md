# NAME

Hash::Merge::Extra - Collection of extra behaviors for [Hash::Merge](https://metacpan.org/pod/Hash%3A%3AMerge)

<div>
    <a href="https://github.com/mr-mixas/Hash-Merge-Extra.pm/actions?query=branch%3Amaster"><img src="https://github.com/mr-mixas/Hash-Merge-Extra.pm/actions/workflows/test.yaml/badge.svg?branch=master" alt="Tests"/></a>
    <a href='https://coveralls.io/github/mr-mixas/Hash-Merge-Extra.pm?branch=master'><img src='https://coveralls.io/repos/github/mr-mixas/Hash-Merge-Extra.pm/badge.svg?branch=master' alt='Coverage Status'/></a>
    <a href="https://badge.fury.io/pl/Hash-Merge-Extra"><img src="https://badge.fury.io/pl/Hash-Merge-Extra.svg" alt="CPAN version"/></a>
</div>

# VERSION

Version 0.06

# SYNOPSIS

    use Hash::Merge qw(merge);
    use Hash::Merge::Extra;

    Hash::Merge::set_behavior('R_OVERRIDE');

    $result = merge($left, $right);

# EXPORT

Nothing is exported.

All behaviors registered in [Hash::Merge](https://metacpan.org/pod/Hash%3A%3AMerge) if used as

    use Hash::Merge::Extra;

Nothing registered if passed empty list:

    use Hash::Merge::Extra qw();

Only specified behaviors registered if list defined:

    use Hash::Merge::Extra qw(L_OVERRIDE R_REPLACE);

# BEHAVIORS

- **L\_ADDITIVE**, **R\_ADDITIVE**

    Hashes merged, arrays joined, undefined scalars overridden. Left and right
    precedence.

- **L\_OVERRIDE**, **R\_OVERRIDE**

    Hashes merged, arrays and scalars overridden. Left and right precedence.

- **L\_REPLACE**, **R\_REPLACE**

    Nothing merged. One thing simply replaced by another. Left and right
    precedence.

# AUTHOR

Michael Samoglyadov, `<mixas at cpan.org>`

# BUGS

Please report any bugs or feature requests to
[https://github.com/mr-mixas/Hash-Merge-Extra.pm/issues](https://github.com/mr-mixas/Hash-Merge-Extra.pm/issues)

# SEE ALSO

[Hash::Merge](https://metacpan.org/pod/Hash%3A%3AMerge)

# LICENSE AND COPYRIGHT

Copyright 2017,2018 Michael Samoglyadov.

This program is free software; you can redistribute it and/or modify it
under the terms of either: the GNU General Public License as published
by the Free Software Foundation; or the Artistic License.

See [http://dev.perl.org/licenses/](http://dev.perl.org/licenses/) for more information.
