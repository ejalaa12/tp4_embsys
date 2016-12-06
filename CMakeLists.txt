cmake_minimum_required()
project(tp4_embsys)

set(SOURCE_CLIENT
        src/autotools/src/client/client.c)

set(SOURCE_SERVER
        src/autotools/src/miniserver/miniserver.c)

set(SOURCE_SYSLOG
        src/syslog/syslog.c)

add_executable(client ${SOURCE_CLIENT})
add_executable(server ${SOURCE_SERVER})
add_executable(syslog ${SOURCE_SYSLOG})