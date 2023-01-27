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
included the HDF5 library as a submodule.

Git tags can be used to check out versions of this toolkit that map to specific
versions of the HDF5 library. These will be maintained as the VOL and VOL-related
products evolve.

**IMPORTANT NOTE**

All VOL development should target HDF5 1.14.x. Important changes were made to
the VOL interface in 1.14.0 that could not be brought to the 1.12 branch due to
binary compatibility issues. 1.13.x releases were experimental releases
(essentially betas that went through the full release process) that were
created while preparing the 1.14.0 release. 1.13.x releases should not be used
for VOL development.

## Contents

|Directory|Contents|
|---------|--------|
|hdf5|Source for HDF5 1.13.0|
|templates/vol-external-passthrough|Pass-through VOL template|
|templates/vol-template|Terminal VOL template|
|tutorial/vol-tutorial|Tutorial VOL connector (slides in doc/)|
|vol-tests|Test suite for external VOL connectors|

## VOL Documentation

The VOL documentation is a part of the HDF5 release documentation. The current version
can be found [here](https://docs.hdfgroup.org/hdf5/develop/index.html). Links to the
VOL connector author's guide and VOL user's guide can be found in the documentation
sidebar.

Additional information can be found in the [VOL documentation](https://portal.hdfgroup.org/display/HDF5/Virtual+Object+Layer)
on the HDF5 support portal, though most of this will eventually move to the release
documentation.

Questions about the VOL and creating a connector can be asked on the [HDF Forum](https://forum.hdfgroup.org/),
where you will find a 'VOLs and VFDs' category.

## Registered VOL Connectors

This table was copied from the VOL documentation in the HDF5 support portal.
The original can be found [here](https://portal.hdfgroup.org/display/support/Registered+VOL+Connectors).


|Connector|Description|URL|
|---------|-----------|---|
|Asynchronous I/O|Provides support for asynchronous operations in HDF5.|[link](https://github.com/hpc-io/vol-async)|
|Cache|Provides support for multi-level, multi-location data caching to dataset I/O operations.|[link](https://github.com/hpc-io/vol-cache)|
|Log-based|The log-based VOL plugin stores HDF5 datasets in a log-based storage layout.|[link](https://github.com/DataLib-ECP/vol-log-based)|
|DAOS|Designed to utilize the DAOS object storage system by use of the DAOS API.|[link](https://github.com/HDFGroup/vol-daos)|
|dset-split|Creates separate sub files for each dataset created and mounts these sub-files as external links in the main file. It enables versioning of HDF5 files at a dataset boundary.|[link](https://github.com/hpc-io/vol-dset-split)|
|PDC-VOL|Terminal VOL connector that reads and writes HDF5 objects to the PDC system.|[link](https://github.com/hpc-io/vol-pdc)|

