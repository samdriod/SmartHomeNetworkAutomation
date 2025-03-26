cmake_minimum_required(VERSION 3.30)
project(SmartHomeNetworkAutomation
        VERSION 1.0
        DESCRIPTION "Smart Home Network Automation System"
        LANGUAGES CXX
)

# Enable C++17
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Policy settings
cmake_policy(SET CMP0079 NEW)

# Global include directory
include_directories(${CMAKE_SOURCE_DIR}/shared/include)

add_executable(SmartHomeNetworkAutomation main.cpp)
target_compile_options(SmartHomeNetworkAutomation PRIVATE -Wall -Wextra)

# Add subdirectories (order matters - shared first)
add_subdirectory(shared)
add_subdirectory(client)
add_subdirectory(server)
add_subdirectory(tests)


# Enable testing
enable_testing()
