cmake_minimum_required (VERSION 3.20)
project(hello-curl)

file(GLOB SOURCES
	"*.c"
)

include(FindCURL)
find_package(CURL REQUIRED)

add_executable(stage ${SOURCES})

target_link_libraries(${PROJECT_NAME}
    CURL::libcurl
)
