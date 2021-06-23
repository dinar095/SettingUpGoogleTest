cmake_minimum_required(VERSION 3.16)
project(SettingUpGoogleTest)


set(CMAKE_CXX_STANDARD 11)

add_subdirectory(lib/googletest-master)
include_directories(lib/googletest-master/googletest/include)
include_directories(lib/googletest-master/googlemock/include)

add_executable(SettingUpGoogleTest main.cpp Tests/ClassName.h Tests/test.cpp project/project.c project/project.h)
target_link_libraries(SettingUpGoogleTest gtest gtest_main)