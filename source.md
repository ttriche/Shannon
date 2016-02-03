---
layout: page
title: "Installation"
description: ""
group: navigation
---
{% include JB/setup %}

The __Shannon__ GitHub repository is [here](https://github.com/sreeramkannan/shannon). Source code can also be downloaded from the [download page](download.html). Currently, __Shannon__ can be built on Linux and Mac. 

<!--
If building on Mac, we suggest using a package manager such as [Homebrew](http://brew.sh) to download dependencies. Homebrew is easily installed by copying and pasting the command below at a terminal prompt:

`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`


Other dependencies are either included, or can be installed using package managers on the system.
-->

#### Requirements: 

- Python 2.7 or greater
- __Metis__ 
    - See [here](http://glaros.dtc.umn.edu/gkhome/metis/metis/download) for instructions on installing metis. In Ubuntu systems, metis can be simply installed using the following command: 
    `sudo apt-get install metis`
- __NUMPY__ 
    - Python package. See [here](http://docs.scipy.org/doc/numpy-1.10.1/user/install.html) for installing. The following command will work if you have pip installed: 
    `pip install numpy`  (you may need sudo access) 
- __CVXOPT__ 
    - Python oackage. See [here](http://cvxopt.org/install/index.html) for installing. The following command will work if you have pip installed: 
    `pip install cvxopt`  (you may need sudo access)
    CVXOPT does require ATLAS or BLAS libraries and LAPACK to be installed prior to its installation. On Ubuntu, it can simply be installed using apt-get with the following set of commands.
    `sudo apt-get install libatlas-dev`
    `sudo apt-get install liblapack-dev`
    `sudo apt-get install libblas-dev`
    `sudo pip install cvxopt`
- __Quorum__ 
    - See [here](http://www.genome.umd.edu/quorum.html) for installing. Both Quorum and Jellyfish can be installed using a [single file](ftp://ftp.genome.umd.edu/pub/QuorUM/quorum_easy_install)
- __Jellyfish__ v2.0 or higher. 
    - Jellyfish should be installed along with Quorum, but in case it is not installed, see [here](http://www.genome.umd.edu/jellyfish.html) for downloading and installing.
- __GNU-Parallel__
	- Optional. It is needed for running multiple jobs simultaneously. See [here](https://www.gnu.org/software/parallel/) for installing.


#### Download

__Shannon__ is hosted on GitHub. The source code can be obtained by cloning the repository as follows:

`git clone https://github.com/sreeramkannan/Shannon.git`

#### Configuration
Shannon needs to be configured so that it can find the dependencies. If the programs can be found directly in the shell, then the default configuration is fine. Otherwise the following four path variables need to be set in the file shannon.py

gpmetis_path = 'gpmetis'
jellyfish_path = 'jellyfish'
gnu_parallel_path = 'parallel'
quorum_path = 'quorum'

For example if quorum is available in '/Packages/quorum-1.0.0/' set the variable as follows:

`quorum_path = '/Packages/quorum-1.0.0/quorum'`

#### Test



The __Shannon__ package comes with a small set of read files that can be used to test that the package was compiled and installed correctly. The [Getting started](starting.html) page provides a complete description of how to run __Shannon__ on these files.
