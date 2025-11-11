cmake_minimum_required(VERSION 3.10)

project(ProjectName)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(${PROJECT_NAME}
    src/main.cpp
)

target_include_directories(${PROJECT_NAME} PRIVATE include)

# Example: Using vcpkg dependencies
#
# find_package(SFML 2.6 COMPONENTS system window graphics CONFIG REQUIRED)
# find_package(EnTT CONFIG REQUIRED)
#
# target_link_libraries(${PROJECT_NAME} PRIVATE
#   fml::system
#   sfml::window
#   sfml::graphics
#   EnTT::EnTT
# )