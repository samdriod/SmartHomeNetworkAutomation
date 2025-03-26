# SmartHomeNetworkAutomation/server/CMakeLists.txt
cmake_minimum_required(VERSION 3.20)

project(Server
        DESCRIPTION "Smart Home Server Application"
)

# Source files
set(SERVER_SOURCES
        src/main.cpp
        # Add other source files explicitly here
)

# Create executable
add_executable(SmartHomeServer ${SERVER_SOURCES})

# Link dependencies
target_link_libraries(SmartHomeServer PRIVATE shared)