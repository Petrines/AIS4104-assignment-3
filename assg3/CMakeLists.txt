find_package(Eigen3 CONFIG REQUIRED)

add_executable(assg3 main.cpp
        petrine_library.h
        petrine_library.cpp)

target_link_libraries(assg3 PRIVATE Eigen3::Eigen)