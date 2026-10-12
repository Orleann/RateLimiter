cmake_minimum_required(VERSION 4.3)
project(RateLimiter CXX)

set(CMAKE_CXX_STANDARD 26)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_compile_options(-Wall -Wextra -Wpedantic -Wconversion)

add_library(limiter_core
    src/Limiter.cpp
        src/Limiter.cpp
        include/Limiter.h
)

target_include_directories(limiter_core PUBLIC include)

add_executable(RateLimiter
    src/main.cpp
        src/Limiter.cpp
        include/Limiter.h
)

target_link_libraries(RateLimiter PRIVATE limiter_core)