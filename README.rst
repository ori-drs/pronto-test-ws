Test environment for pronto's core estimator

First add these lines to bashrc. pronto_estimator_core finds dependencies using PKG_CONFIG_PATH
(using a build system called PODS)

::

  source /opt/ros/kinetic/setup.bash
  source <YOUR-PATH-TO>/pronto-test-ws/code/devel/setup.bash
  export PKG_CONFIG_PATH=<YOUR-PATH-TO>/pronto-test-ws/externals/build/lib/pkgconfig:$PKG_CONFIG_PATH

The compile the dependencies and then the module itself

::

  git submodule update --init --recursive
  cd externals
  make -j
  cd ../code
  catkin build

  This take about 80 seconds to compile