include_directories(SYSTEM ${gtest_SOURCE_DIR}/include ${gtest_SOURCE_DIR})
aux_source_directory(. TEST_FILES)
set(TARGET_NAME "oqs_cpp_testing")
add_executable(${TARGET_NAME} ${TEST_FILES})
target_link_libraries(${TARGET_NAME} gmock oqs)
