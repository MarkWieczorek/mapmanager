---
layout: page
title: "File format"
category: post
date: 2015-05-28 22:01:06
tags:
- xxx
---

Map Manager 3 can save two different types of files

- Text
- HDF5

###HDF5

[HDF5][1] is an open source cross platform binary file format. It can be read from [Matlab][2], [Python][3], [Igor Pro][4] and from a [command line][5].

####Python

It is suggested that you use the [Anaconda][6] python distribution as it comes with many useful packages pre-installed including hdf5 for python. Download Anaconda it [here][7].

    import h5py
    import numpy as np
    
    #open h5 file
    f = h5py.File('a5n.hdf5', 'r')
    
    #get list of top level groups (these are mm3 maps)
    for g in f:
        print g
        
    #assign myMap to top level map
    for myMap in f: print myMap
    
    #get list of objects within a map
    #these objects include {objmap, stackdb, int, line, linedb}
    #keys() returns a list [0], [1], [2], ...
    for key in f[myMap].keys():
        print key
        
    #datasets within group 'a104'
    for ds in f[myMap].values():
        print ds
        
    
    # get an object
    objectIndex = 4
    f[myMap].values()[objectIndex][:][:]
    
    # get the value of a spine from an object
    objectIndex = 4
    spineIndex = 10
    f[myMap].values()[objectIndex][spineIndex]
    
    #attributes of a dataset
    objectIndex= 4
    for a in f[myMap].values()[objectIndex].attrs:
        print a

    #this is trying to pull form an intensity object
    #for some reaosn i can't transpose the rows
    f[myMap].values()[9].values()[0][0][:]
    
    #spine 0, spineLen2 (spineLen2 is in column 1)
    f[myMap].values()[9].values()[0][0][1]
    
    #spine 1, spineLen2
    f[myMap].values()[9].values()[0][1][1]

In [64]: f[myMap].values()[9].values()
Out[64]: 
[<HDF5 dataset "a5n_s0_Int1": shape (385, 41), type "<f4">,
 <HDF5 dataset "a5n_s0_Int2": shape (385, 41), type "<f4">,
 <HDF5 dataset "a5n_s0_db2": shape (385, 44), type "|O8">,
 <HDF5 dataset "a5n_s0_l": shape (3903, 19), type "<f4">,
 <HDF5 dataset "a5n_s1_Int1": shape (378, 41), type "<f4">,
 <HDF5 dataset "a5n_s1_Int2": shape (378, 41), type "<f4">,
 <HDF5 dataset "a5n_s1_db2": shape (378, 44), type "|O8">,
 <HDF5 dataset "a5n_s1_l": shape (3871, 19), type "<f4">,
 <HDF5 dataset "a5n_s2_Int1": shape (369, 41), type "<f4">,
 <HDF5 dataset "a5n_s2_Int2": shape (369, 41), type "<f4">,
 <HDF5 dataset "a5n_s2_db2": shape (369, 44), type "|O8">,
 <HDF5 dataset "a5n_s2_l": shape (3742, 19), type "<f4">,
 <HDF5 dataset "a5n_s3_Int1": shape (364, 41), type "<f4">,
 <HDF5 dataset "a5n_s3_Int2": shape (364, 41), type "<f4">,
 <HDF5 dataset "a5n_s3_db2": shape (364, 44), type "|O8">,
 <HDF5 dataset "a5n_s3_l": shape (3837, 19), type "<f4">]

i got 385 from shape (how do i do this with code?)

In [82]: for a in range(385):
    print f[myMap].values()[9].values()[0][a][1]


###this is working

    mya=np.arange(385, dtype=np.float32)
    for a in range(385):
        mya[a] = f[myMap].values()[9].values()[0][a][1]
    
    import matplotlib.pyplot as plt
    plt.plot(mya, 'ro')
    plt.xlabel('Spine Index')
    plt.ylabel('Spine Length 2D (um)')
    plt.show()
    
        
####Use the Python hdf5Manager

For now this is not very useful for my hdf5 files but is a proof of concept.

1. Download hdf5 manager [here][8].

2. Run it

    python h5_manager.py 

3. Getting h5_manager to work  
    
    
        #install pyqt4 in anaconda
        conda install pyqt
        #update anaconda (h5_manager was failing to import matplotlib)
        conda update --prefix /Users/cudmore/anaconda anaconda
        #run h5_manager
        python h5_manager.py 
    
    
[1]: https://www.hdfgroup.org/HDF5/
[2]: http://www.mathworks.com/help/matlab/hdf5-files.html
[3]: http://www.h5py.org
[4]: http://www.wavemetrics.com/products/igorpro/dataaccess/hdf5.htm
[5]: https://www.hdfgroup.org/products/hdf5_tools/#h5dist
[6]: https://store.continuum.io/cshop/anaconda/
[7]: http://continuum.io/downloads
[8]: https://github.com/mgraupe/hdf5Manager