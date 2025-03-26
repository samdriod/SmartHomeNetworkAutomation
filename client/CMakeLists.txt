# SmartHomeNetworkAutomation/client/CMakeLists.txt
cmake_minimum_required(VERSION 3.20)

project(Client
        DESCRIPTION "Smart Home Client Application"
)

# Source files (explicit listing preferred over GLOB for production)
set(CLIENT_SOURCES
        src/main.cpp
        # Add other source files explicitly here
)

# Create executable
add_executable(SmartHomeClient ${CLIENT_SOURCES})

# Link dependencies
target_link_libraries(SmartHomeClient PRIVATE shared)
