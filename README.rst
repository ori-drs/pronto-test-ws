Test environment for pronto's core estimator

::

  git submodule update --init --recursive
  cd externals
  make -j
  cd ../code
  catkin build

  This take about 80 seconds to compile