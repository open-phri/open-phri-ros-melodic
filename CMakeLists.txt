CMAKE_MINIMUM_REQUIRED(VERSION 3.0.2)
set(WORKSPACE_DIR ${CMAKE_SOURCE_DIR}/../.. CACHE PATH "root of the PID workspace directory")
list(APPEND CMAKE_MODULE_PATH ${WORKSPACE_DIR}/share/cmake/system) # using generic scripts/modules of the workspace
include(Package_Definition NO_POLICY_SCOPE)

project(open-phri-ros)

PID_Package(
			AUTHOR      idhuser
			YEAR        2019
			LICENSE     CeCILL
			DESCRIPTION TODO: input a short description of package open-phri-ros utility here
			VERSION     0.0.0
		)

#now finding packages

build_PID_Package()
