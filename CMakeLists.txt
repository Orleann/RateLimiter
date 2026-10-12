cmake_minimum_required(VERSION 4.3)
project(RateLimitter)

set(CMAKE_CXX_STANDARD 14)

add_executable(RateLimitter
        src/main.cpp
        src/Limiter.cpp
        include/Limiter.h
)
