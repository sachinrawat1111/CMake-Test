cmake_minimum_required(VERSION "3.19.1")
project("CMakeTest")
add_executable("${PROJECT_NAME}" "Main.cpp")
install(TARGETS "${PROJECT_NAME}" DESTINATION bin)
install(FILES "Main.cpp" DESTINATION src)

include(CTest)
add_test("Test1" "${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}")