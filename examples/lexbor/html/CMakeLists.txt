cmake_minimum_required(VERSION 2.8.12...3.27)

################
## Sources
#########################
file(GLOB_RECURSE EXAMPLES_LEXBOR_HTML_SOURCES "*.c")

################
## ARGS for tests
#########################
set(html2sexpr_arg "${CMAKE_SOURCE_DIR}/test/files/lexbor/html/lexbor.html")
set(encoding_arg "${CMAKE_SOURCE_DIR}/test/files/lexbor/html/lexbor.html")

################
## Create executable
#########################
EXECUTABLE_LIST("" "${EXAMPLES_LEXBOR_HTML_SOURCES}" ${EXAMPLES_DEPS_LIB_NAMES})

IF(LEXBOR_BUILD_TESTS)
    APPEND_TESTS("examples_lexbor_html_" "${EXAMPLES_LEXBOR_HTML_SOURCES}")
ENDIF()