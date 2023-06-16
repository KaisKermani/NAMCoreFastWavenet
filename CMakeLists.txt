cmake_minimum_required(VERSION 3.12)

project(YourProjectName)

# Set C++ standard to C++17
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Add your source files
set(SOURCES
    src/main.cpp
    src/your_source_file.cpp
)

# Add your test files
set(TEST_SOURCES
    test/test_main.cpp
    test/your_test_file.cpp
)

# Add your include directories
include_directories(include)

# Create an executable for your project
add_executable(YourProject ${SOURCES})

# Add any necessary dependencies
target_link_libraries(YourProject
    # Add your libraries or dependencies here
)

# Add the testing framework (e.g., Google Test)
add_subdirectory(lib/googletest)

# Create an executable for your tests
add_executable(YourTests ${TEST_SOURCES})

# Link your tests with the testing framework and any necessary dependencies
target_link_libraries(YourTests
    gtest
    gtest_main
    # Add your libraries or dependencies here
)

# Add a test target that runs your tests
enable_testing()
add_test(NAME YourTests COMMAND YourTests)
