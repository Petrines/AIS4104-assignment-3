find_package(Eigen3 CONFIG REQUIRED)

add_executable(assg1 main.cpp
        petrine_library.h
        petrine_library.cpp)
target_link_libraries(assg1 PRIVATE Eigen3::Eigen)