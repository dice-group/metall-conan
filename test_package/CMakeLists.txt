cmake_minimum_required(VERSION 3.10)
project(PackageTest CXX)

find_package(Metall REQUIRED)

add_executable(example example.cpp)

target_link_libraries(example PUBLIC
        Metall::Metall
        )

set_target_properties(
        example PROPERTIES
        CXX_STANDARD 20
        CXX_STANDARD_REQUIRED ON
        CXX_EXTENSIONS OFF
)
