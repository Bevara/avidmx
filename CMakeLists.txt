cmake_minimum_required(VERSION 3.7)
project(Filters)

include(filters.cmake)

add_definitions(-fpic)

SET(AVIDMX_LIB
)


SET(AVIDMX_SRC
        ${CMAKE_CURRENT_SOURCE_DIR}/dmx_avi.c
)

SET(AVIDMX_INCLUDE
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)

add_filter(avidmx
        "${AVIDMX_SRC}"
        "${AVIDMX_LIB}"
        []
        ""
        "${AVIDMX_INCLUDE}"
        ""
        "1")