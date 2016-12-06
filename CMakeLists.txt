cmake_minimum_required()
project(tp4_embsys)

set(dir ${CMAKE_CURRENT_SOURCE_DIR}/build/)
set(EXECUTABLE_OUTPUT_PATH ${dir} CACHE PATH "Build directory" FORCE)
set(LIBRARY_OUTPUT_PATH ${dir} CACHE PATH "Build directory" FORCE)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${dir})
set(CMAKE_BUILD_FILES_DIRECTORY ${dir})
set(CMAKE_BUILD_DIRECTORY ${dir})
set(CMAKE_BINARY_DIR  ${dir})
set(EXECUTABLE_OUTPUT_PATH ${dir})
set(LIBRARY_OUTPUT_PATH ${dir}lib)
set(CMAKE_CACHEFILE_DIR ${dir})

set(SOURCE_CLIENT
        src/autotools/src/client/client.c)

set(SOURCE_SERVER
        src/autotools/src/miniserver/miniserver.c)

set(SOURCE_SYSLOG
        src/syslog/syslog.c)


add_executable(client.o ${SOURCE_CLIENT})
add_executable(server.o ${SOURCE_SERVER})
add_executable(syslog.o ${SOURCE_SYSLOG})