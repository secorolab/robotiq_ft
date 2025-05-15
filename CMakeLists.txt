cmake_minimum_required(VERSION 3.15)
project(robotiq_ft)

add_subdirectory(src/example)

add_library(robotiq_ft_driver SHARED
    src/rq_sensor_com.c
    src/rq_sensor_state.c
)
target_include_directories(robotiq_ft_driver PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:include>
)

install(TARGETS robotiq_ft_driver
    LIBRARY DESTINATION lib
    ARCHIVE DESTINATION lib
    RUNTIME DESTINATION bin
)

install(DIRECTORY include/robotiq_ft
    DESTINATION include
    FILES_MATCHING PATTERN "*.h"
)