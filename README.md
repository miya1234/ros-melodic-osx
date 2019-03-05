===============

This page is copy from https://github.com/mikepurvis/ros-install-osx

Usage
-----

```shell
git clone ************************
cd ros-install-osx
./install
```



*****************************************************************************************************
after error do this bellow

pushd melodic_desktop_full_ws

rosdep install --from-paths src --ignore-src --rosdistro melodic -y --skip-keys google-mock --as-root pip:no

./src/catkin/bin/catkin_make_isolated --install --install-space /opt/ros/melodic --cmake-args -DCATKIN_ENABLE_TESTING=0 -DCMAKE_BUILD_TYPE=Release -DCMAKE_FIND_FRAMEWORK=LAST -DCMAKE_CXX_STANDARD=14 -DPYTHON_EXECUTABLE=$(which python2) -DPYTHON_LIBRARY=$(python2 -c "import sys; print sys.prefix")/lib/libpython2.7.dylib -DPYTHON_INCLUDE_DIR=$(python2 -c "import sys; print sys.prefix")/include/python2.7

