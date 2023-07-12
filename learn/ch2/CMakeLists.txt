# state the lowest version required cmake
cmake_minimum_required( VERSION 3.2 )

# state a cmake project
project( HelloSLAM )

# add an executable program
# grammar: add_executable( program_name source_code_file )
add_executable(helloSLAM helloSLAM.cpp)

# add an library
# grammar: add_library( library_name source_code_file )
# a static library .a
add_library(hello libHelloSLAM.cpp)  

# a shared library .so
add_library(hello_shared SHARED libHelloSLAM.cpp)

add_executable(useHello useHello.cpp)
target_link_libraries(useHello hello_shared)

