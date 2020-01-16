cmake_minimum_required(VERSION "3.10.2")

project(myProgram)


include_directories(include)

add_library(liberino SHARED src/libtest.cpp)

install(TARGETS liberino DESTINATION lib)

set(PROJECT_LINK_LIBS libliberino.so)
link_directories("/home/spidi/school/kolokwium_ostatnie/kolokwium_git/zad_6/lib")

add_executable(${PROJECT_NAME} src/Student.cpp)

install(TARGETS ${PROJECT_NAME} DESTINATION bin)
target_link_libraries(${PROJECT_NAME} liberino)
