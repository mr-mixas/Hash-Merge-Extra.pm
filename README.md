# NAME

Hash::Merge::Extra - Collection of extra behaviors for [Hash::Merge](https://metacpan.org/pod/Hash::Merge)

# VERSION

Version 0.03

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

- L\_ADDITIVE, R\_ADDITIVE

    Hashes merged, arrays joined, scalars overrided if undefined. Left and right precedence.

- L\_OVERRIDE, R\_OVERRIDE

    Merge hashes, override arrays and scalars. Left and right precedence.

- L\_REPLACE, R\_REPLACE

    Don't merge, simply replace one thing by another. Left and right precedence.

# SEE ALSO

[Hash::Merge](https://metacpan.org/pod/Hash::Merge)

# LICENSE AND COPYRIGHT

Copyright 2017 Michael Samoglyadov.

This program is free software; you can redistribute it and/or modify it
under the terms of either: the GNU General Public License as published
by the Free Software Foundation; or the Artistic License.

See [http://dev.perl.org/licenses/](http://dev.perl.org/licenses/) for more information.
