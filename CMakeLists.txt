CMAKE_MINIMUM_REQUIRED(VERSION 3.5)

ADD_COMPILE_OPTIONS(-std=c++11 -Wall)

PROJECT(cpphello)

SET(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${PROJECT_SOURCE_DIR}/build/bin")

IF(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)
  SET(CMAKE_INSTALL_PREFIX ${PROJECT_SOURCE_DIR}/install CACHE PATH "" FORCE)
ENDIF()

SET(targetname cpphello)

SET(sources
main.cpp
)

SET(headers
)

ADD_EXECUTABLE(${targetname} ${sources} ${headers})
INSTALL(TARGETS cpphello DESTINATION bin)
