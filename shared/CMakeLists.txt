# SmartHomeNetworkAutomation/shared/CMakeLists.txt
cmake_minimum_required(VERSION 3.20)

project(Shared
        DESCRIPTION "Shared code for Smart Home System"
)

# Source files
set(SHARED_SOURCES
        src/file1.cpp
        # Add all shared source files here
)

# Header files (for IDE organization)
set(SHARED_HEADERS
        include/file1.h
        # Add all shared header files here
)

# Create library
add_library(shared STATIC ${SHARED_SOURCES} ${SHARED_HEADERS})

# Public include directory (for clients of this library)
target_include_directories(shared PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
        $<INSTALL_INTERFACE:include>
)
