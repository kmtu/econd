decond
=====
A framework for calculating the electrical conductivity from MD trajectories and performing various decomposition methods

----------

Project structure
-----
This project consists of two parts:
1. Decomposition of the velocity time correlation functions of ions calculated from the [Gromacs](http://www.gromacs.org/) MD trajectories. It is done throught the Fortran program `fortran/decompose_mpi`.
2. Analysis of the decomposed correlation data. It is done through the Python scripts in `python/` folder.


Dependency
-----
Fortran:
   - [XTC library](http://www.gromacs.org/Developer_Zone/Programming_Guide/XTC_Library): Please use the customized version in `fortran/lib/xdrfile-1.1.1-d`, which has been modified to double precision.
   - [HDF5](http://www.hdfgroup.org/HDF5/): You can use the system built-in HDF5 if available, or download it from the [HDF5 group page](http://www.hdfgroup.org/HDF5/).

Python 3:
   - [SciPy](http://www.scipy.org/): Using the [Anaconda Python Distribution](http://continuum.io/downloads#34) is the easiest way, which includes many packages useful for scientific purposes including SciPy.
   
General setup instructions
-----
The general idea of the setup process is:
1. Compile and install the customized XTC library `fortran/lib/xdrfile-1.1.1-d`
2. Compile and install the HDF5 library, if it is not available on your system.
3. Manually edit the file `fortran/Makefile` to suit your environment and then compile with `make`
4. Download and install [Anaconda Python Distribution](http://continuum.io/downloads#34)

More details may be added to the [wiki page](https://github.com/kmtu/decond/wiki).

----------

#### This project uses [semantic versioning (2.0.0)](http://semver.org/)
