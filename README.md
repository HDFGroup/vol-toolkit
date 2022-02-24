# A Toolkit for HDF5 VOL Connector Authors

This toolkit is intended to help HDF5 Virtual Object Layer (VOL) connector
authors get up and running. It includes empty "templates" for both pass-through
and terminal VOL connectors, a tutorial, and copies of the current VOL
documentation.

Most of the code is obtained via git submodules that refer to particular
branches in external repositories. To ensure you have these submodules, either
clone this repository using:

    `git clone --recursive <path>`

or:

    `git clone <path>`
    `git submodule update --init`

As a convenience and to ensure that everything stays in sync, we've also
included the HDF5 library as a submodule. This is currently set to point to
the HDF5 1.13.0 release tag.

**NOTE**

All VOL development should target HDF5 1.13.x. Important changes were made to
the VOL interface in 1.13 that could not be brought to the 1.12 branch due to
binary compatibility issues.
