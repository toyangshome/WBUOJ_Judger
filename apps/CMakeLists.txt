add_executable(judger judger.cpp)
target_compile_features(judger PRIVATE cxx_std_17)

target_link_libraries(judger PRIVATE judger_library)