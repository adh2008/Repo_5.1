cmake_minimum_required(VERSION 3.14)
project(Repo_5_1)

set(CMAKE_CXX_STANDARD 14)

# Автоматично завантажуємо Google Test з GitHub
include(FetchContent)
FetchContent_Declare(
  googletest
  URL https://github.com/google/googletest/archive/refs/tags/v1.14.0.zip
)
FetchContent_MakeAvailable(googletest)

# Створюємо тестовий виконуваний файл
add_executable(unit_test5.1 unit_test5.1.cpp)
target_link_libraries(unit_test5.1 gtest gtest_main)