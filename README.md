# A toolkit for HDF5 VOL connector authors

This toolkit is intended to help HDF5 Virtual Object Layer (VOL) connector
authors get up and running. It includes empty "templates" for both pass-through
and terminal VOL connectors, a tutorial, and copies of the VOL documentation.

Most of the code is obtained via git submodules that refer to particular
branches in external repositories. To ensure you have these submodules, either
clone this repository using:

    `git clone --recursive <path>`

or:

    `git clone <path>`
    `git submodule update --init`

Note that the tutorial is a work in progress and will not be ready until 
December 2021.

As a convenience and to ensure that everything stays in sync, we've also
included the HDF5 library as a submodule. This is currently set to use the
develop branch, but it will point to the HDF5 1.13.0 tag when that version is
released.

**NOTE**

All VOL development should target HDF5 1.13.0 (or the develop branch until 1.13
is released). Important changes were made to the VOL interface that could not
be brought to the 1.12 branch due to binary compatibility issues.
