cmake_minimum_required(VERSION 3.20)

# add the executable
# add new test files here
add_executable(
    test_${CMAKE_PROJECT_NAME} 
    ${PROJECT_SOURCE_DIR}/tests/test_create.cpp
    ${PROJECT_SOURCE_DIR}/tests/test_passGetter.cpp
    ${PROJECT_SOURCE_DIR}/tests/test_encryptor.cpp
    ${PROJECT_SOURCE_DIR}/tests/test_encryptor_handler.cpp
) 

# link libraries to the executable
target_link_libraries(
    test_${CMAKE_PROJECT_NAME}
    _${CMAKE_PROJECT_NAME}
    Catch2::Catch2WithMain
    trompeloeil::trompeloeil
)
