**This repository is used for preparing and recording deliveries to HST DMS.**
The release notes for each build are tracked and stored with the astroconda spec build which recreates the environment that was delivered


Installing a fresh pipeline environment 
=======================================

- Install Anaconda3 or Miniconda
    - For detailed instructions regarding this step, please visit:  http://docs.continuum.io/anaconda/install#linux-install
``` 
    # Anaconda

    $ wget https://repo.continuum.io/archive/Anaconda3-4.2.0-Linux-x86_64.sh
    $ bash Anaconda3-4.2.0-Linux-x86_64.sh
    $ export PATH=$HOME/anaconda3/bin:$PATH

    # Miniconda (if preferred)

    $ wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
    $ bash Miniconda3-latest-Linux-x86_64.sh
    $ export PATH=$HOME/miniconda3/bin:$PATH
```

Notes
-----
A fresh installation of Anaconda3 or Miniconda3 is not required for each HSTDP release. The method described here allows multiple, entirely segregated pipeline installations. To facilitate ease of use, all future Anaconda3-based release messages will provide a "one-liner" installation procedure. This text will precede the generic installation instructions. The format will be as follows:

For existing Anaconda3 or Miniconda3 installations:
```
$ conda create -n %NAME_%YEAR_%BUILD --file %NAME-%YEAR.$BUILD/%NAME-%YEAR.%BUILD-%PLATFORM-%PYTHON_VERSION.%ITERATION.txt
```
As bug fixes are announced, your pipeline software may be updated by issuing the command:
```
# (%ITERATION denotes the next available update, i.e. 0.txt, 1.txt, 2.txt, etc.)
$ conda update --file %NAME-%YEAR.$BUILD/%NAME-%YEAR.%BUILD-%PLATFORM-%PYTHON_VERSION.%ITERATION.txt
```

Under Anaconda, updates will not be supplied via external installation addons as either tarballs or scripts. Also keep in mind, Conda, the Anaconda package manager, may prompt you automatically to upgrade packages deemed out of date.

