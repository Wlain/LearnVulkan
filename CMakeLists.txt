cmake_minimum_required(VERSION 3.8)
project(learnVulkan)

# glfw
add_subdirectory(3rdparty/glfw)

set(CMAKE_CXX_STANDARD 20)

include_directories(${PROJECT_SOURCE_DIR}/src
        ${PROJECT_SOURCE_DIR}/3rdparty/glfw/deps)
file(GLOB_RECURSE SOURCES CONFIGURE_DEPENDS src/*.cpp samples/*.cpp)
add_executable(learnVulkan ${SOURCES})

target_link_libraries(learnVulkan glfw)

