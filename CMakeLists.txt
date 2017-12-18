CMAKE_MINIMUM_REQUIRED (VERSION 3.0)
PROJECT (chaitest)

INCLUDE_DIRECTORIES(
	libs/chaiscript/include
   ) 
SET(SRCS
       	src/chai.cpp 
   ) 

if(MINGW OR CYGWIN) 
	set_property(SOURCE src/chai.cpp APPEND PROPERTY COMPILE_FLAGS "-O3" ) 

  #add_definitions(-O3)
endif()


ADD_DEFINITIONS(-std=c++14)
ADD_EXECUTABLE(chai ${SRCS}) 
