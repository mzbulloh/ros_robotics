cmake_minimum_required(VERSION 3.8)
project(bulls_gazebo)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# Find dependencies
find_package(ament_cmake REQUIRED)

# Install directories BEFORE calling ament_package()
install(DIRECTORY launch config worlds
  DESTINATION share/${PROJECT_NAME})

# This MUST be the final macro invocation in the file
ament_package()
