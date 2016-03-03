# OpenCV-2.4.3-custom

# install 

mkdir release
cd release

cmake ../OpenCV-2.4.3 -D BUILD_NEW_PYTHON_SUPPORT=ON -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=$OPENSHIFT_DATA_DIR -D PYTHON_LIBRARY=$LD_LIBRARY_PATH/libpython2.7.so -D CMAKE_INCLUDE_PATH=$OPENSHIFT_HOMEDIR/python/virtenv/include/python2.7 -D PYTHON_INCLUDE_DIR=$OPENSHIFT_HOMEDIR/python/virtenv/include/python2.7 -D PYTHON_PACKAGES_PATH=$OPENSHIFT_HOMEDIR/python/virtenv/lib/python2.7/site-packages -D PYTHON_EXECUTABLE=$OPENSHIFT_HOMEDIR/python/virtenv/bin/python -D WITH_OPENEXR=OFF -D BUILD_DOCS=OFF -DBUILD_SHARED_LIBS=ON ..

make
make install
