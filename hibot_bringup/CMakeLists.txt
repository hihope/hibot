cmake_minimum_required(VERSION 2.8.3)
project(hibot_bringup)

find_package(catkin REQUIRED COMPONENTS)

catkin_package()

catkin_install_python(PROGRAMS
        scripts/test.py
        scripts/go_rect.py
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(DIRECTORY launch
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(DIRECTORY param
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(DIRECTORY icons
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(DIRECTORY interactions
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(DIRECTORY maps
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
