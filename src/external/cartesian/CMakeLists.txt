CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

SET(CARTESIAN_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR} CACHE PATH "Path to cartesian library")

ADD_LIBRARY(cartesian
Cartesian.cpp
Cartesian.H
)

INCLUDE_DIRECTORIES( ${FLTK_INCLUDE_DIR} )

ADD_EXECUTABLE( Ca_Example
example.cpp
)

TARGET_LINK_LIBRARIES( Ca_Example
	cartesian
	${FLTK_LIBRARIES}
)

