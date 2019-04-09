cmake_minimum_required(VERSION 3.6)
project(pos VERSION 0.0.0)
include(GNUInstallDirs)

set(CMAKE_CXX_STANDARD 14)

add_library(ampos SHARED
	trade.h
	trade.cpp
	)

set_target_properties(ampos PROPERTIES 
	VERSION ${PROJECT_VERSION} 
	SOVERSION 1
	PUBLIC_HEADER trade.h)

install(TARGETS ampos
	LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
	PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})


