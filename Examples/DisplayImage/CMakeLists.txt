# Find Pangolin (https://github.com/stevenlovegrove/Pangolin)
find_package(Pangolin 0.1 REQUIRED)
include_directories(${Pangolin_INCLUDE_DIRS})

# Find Scenegraph
include_directories(${CMAKE_BINARY_DIR}/Examples/DisplayImage ${SCENEGRAPH_INCLUDE_DIRS})

# Set GCC style compiler flags
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

add_executable(DisplayImage main.cpp)
target_link_libraries(DisplayImage ${Pangolin_LIBRARIES})
target_link_libraries(DisplayImage ${SCENEGRAPH_LIBRARIES})
