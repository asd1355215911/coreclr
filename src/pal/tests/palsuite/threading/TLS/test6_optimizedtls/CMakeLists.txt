cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  test.c
)

add_executable(paltest_tls_test6_optimizedtls
  ${SOURCES}
)

add_dependencies(paltest_tls_test6_optimizedtls CoreClrPal)

target_link_libraries(paltest_tls_test6_optimizedtls
  pthread
  rt
  m
  CoreClrPal
)
