soth
====

[![Building Status](https://travis-ci.org/stack-of-tasks/soth.svg?branch=master)](https://travis-ci.org/stack-of-tasks/soth)
[![Pipeline status](https://gepgitlab.laas.fr/stack-of-tasks/soth/badges/master/pipeline.svg)](https://gepgitlab.laas.fr/stack-of-tasks/soth/commits/master)
[![Coverage report](https://gepgitlab.laas.fr/stack-of-tasks/soth/badges/master/coverage.svg?job=doc-coverage)](http://projects.laas.fr/stack-of-tasks/doc/stack-of-tasks/soth/master/coverage/)


Setup
-----
mkdir ~/install_dir
cd ~/install_dir
git clone https://github.com/sotiris-stav/soth.git
cd soth
git checkout focal
cd cmake
git clone --depth 1 --branch before_setup_project_deprecation https://github.com/jrl-umi3218/jrl-cmakemodules ./
cd ..
mkdir _build
cd _build
cmake -DCMAKE_BUILD_TYPE=Release ..
sudo make install
LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/lib

Please note that CMake produces a `CMakeCache.txt` file which should
be deleted to reconfigure a package from scratch.


### Dependencies

The matrix abstract layer depends on several packages which
have to be available on your machine.

 - Libraries:
   - eigen3
 - System tools:
   - CMake (>=2.6)
   - pkg-config
   - usual compilation tools (GCC/G++, make, etc.)
