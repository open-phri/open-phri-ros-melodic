CMAKE_MINIMUM_REQUIRED(VERSION 3.0.2)
set(WORKSPACE_DIR ${CMAKE_SOURCE_DIR}/../.. CACHE PATH "root of the PID workspace directory")
list(APPEND CMAKE_MODULE_PATH ${WORKSPACE_DIR}/share/cmake/system) # using generic scripts/modules of the workspace
include(Package_Definition NO_POLICY_SCOPE)

project(open-phri-ros-melodic)

PID_Package(
    AUTHOR 		    Benjamin Navarro
    INSTITUTION	    LIRMM
    MAIL		    navarro@lirmm.fr
    ADDRESS 	    git@github.com:open-phri/open-phri-ros-melodic.git 
    PUBLIC_ADDRESS  https://github.com/open-phri/open-phri-ros-melodic.git 
    YEAR 		    2019
    LICENSE 	    CeCILL
    DESCRIPTION     "A wrapper package to use OpenPHRI from a ROS Melodic package"
    CODE_STYLE		pid11
    VERSION			1.0.0
)

check_PID_Platform(CONFIGURATION ros[distribution=melodic])

PID_Dependency(boost EXACT VERSION SYSTEM)
PID_Dependency(open-phri VERSION 1.0)

build_PID_Package()
