
# --------------- sdf_lab_console.exe
add_executable(sdf_lab_console console.cpp)

target_link_libraries(sdf_lab_console PRIVATE sdf-lab)
target_link_libraries(sdf_lab_console PRIVATE obj_io)
target_link_libraries(sdf_lab_console PRIVATE gflags)


# --------------- obj_io_example.exe
add_executable(obj_io_example obj_io_example.cpp)
target_link_libraries(obj_io_example PRIVATE obj_io)