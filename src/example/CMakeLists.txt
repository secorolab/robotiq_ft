add_executable(robotiq_ft_blocking_ex
    blocking.c
)
target_link_libraries(robotiq_ft_blocking_ex
    robotiq_ft_driver
)

add_executable(robotiq_ft_non_blocking_ex
    non_blocking.c
)
target_link_libraries(robotiq_ft_non_blocking_ex
    robotiq_ft_driver
)