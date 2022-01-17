cmake_minimum_required( VERSION 3.1.0 )

project ( RTWeekend
  VERSION 1.0.0
  LANGUAGES CXX
)

# Set to c++11
set ( CMAKE_CXX_STANDARD 11 )

# Source
set ( COMMON_ALL
  src/common/rtweekend.hpp
  src/common/camera.hpp
  src/common/ray.hpp
  src/common/vec3.hpp
)

set ( SOURCE_ONE_WEEKEND
  ${COMMON_ALL}
  src/InOneWeekend/hittable.hpp
  src/InOneWeekend/hittable_list.hpp
  src/InOneWeekend/material.hpp
  src/InOneWeekend/sphere.hpp
  src/InOneWeekend/main.cpp
)

# Executables
add_executable(inOneWeekend     ${SOURCE_ONE_WEEKEND})

include_directories(src/common)