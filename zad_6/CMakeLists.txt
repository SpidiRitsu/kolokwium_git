cmake_minimum_required(VERSION "3.10.2")

project(myProgram)


include_directories(include)

add_library(liberino SHARED src/libtest.cpp)

install(TARGETS liberino DESTINATION lib)

SET(CMAKE_INSTALL_RPATH "${CMAKE_INSTALL_PREFIX}/lib")

link_directories("/home/spidi/school/kolokwium_ostatnie/kolokwium_git/zad_6/lib")

add_executable(${PROJECT_NAME} src/Student.cpp)

install(TARGETS ${PROJECT_NAME} DESTINATION bin)
target_link_libraries(${PROJECT_NAME} liberino)
