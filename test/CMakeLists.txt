if(MSVC)
  if(MSVC_VERSION LESS "1900")
    # < VS2015, no "/utf-8" option, can not build test
    return()
  endif()
endif()

enable_testing()

set(LIB_NAME "onig_ng")
if(ONIG_COMPAT_API)
  set(LIB_NAME "onig")
endif()

add_executable(test_utf8 test_utf8.c)
target_link_libraries(test_utf8 ${LIB_NAME})
if(MSVC)
  target_compile_options(test_utf8 PRIVATE /utf-8)
endif(MSVC)

add_executable(test_syntax test_syntax.c)
target_link_libraries(test_syntax ${LIB_NAME})
if(MSVC)
  target_compile_options(test_syntax PRIVATE /utf-8)
endif(MSVC)

add_executable(test_options test_options.c)
target_link_libraries(test_options ${LIB_NAME})
if(MSVC)
  target_compile_options(test_options PRIVATE /utf-8)
endif(MSVC)

if(NOT MSVC)
  # EUC
  add_executable(testc testc.c)
  target_link_libraries(testc ${LIB_NAME})
  if (CMAKE_C_COMPILER_ID MATCHES "Clang|GNU")
	target_compile_options(testc PRIVATE -Wall -Wno-invalid-source-encoding)
  endif()
endif(NOT MSVC)

if(ENABLE_POSIX_API)
  add_executable(testp testp.c)
  target_link_libraries(testp ${LIB_NAME})
endif()

add_executable(testcu testu.c)
target_link_libraries(testcu ${LIB_NAME})

add_executable(test_regset test_regset.c)
target_link_libraries(test_regset ${LIB_NAME})
if(MSVC)
  target_compile_options(test_regset PRIVATE /utf-8)
endif(MSVC)

add_executable(test_back test_back.c)
target_link_libraries(test_back ${LIB_NAME})
if(MSVC)
  target_compile_options(test_back PRIVATE /utf-8)
endif(MSVC)
