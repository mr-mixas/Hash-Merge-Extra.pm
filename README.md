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

- __L\_ADDITIVE__, __R\_ADDITIVE__

    Hashes merged, arrays joined, undefined scalars overrided. Left and right precedence.

- __L\_OVERRIDE__, __R\_OVERRIDE__

    Hashes merged, arrays and scalars overrided. Left and right precedence.

- __L\_REPLACE__, __R\_REPLACE__

    Nothing merged. One thing simply replaced by another. Left and right precedence.

# SEE ALSO

[Hash::Merge](https://metacpan.org/pod/Hash::Merge)

# LICENSE AND COPYRIGHT

Copyright 2017 Michael Samoglyadov.

This program is free software; you can redistribute it and/or modify it
under the terms of either: the GNU General Public License as published
by the Free Software Foundation; or the Artistic License.

See [http://dev.perl.org/licenses/](http://dev.perl.org/licenses/) for more information.
