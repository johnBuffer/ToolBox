cmake_minimum_required(VERSION 3.10)

set(PROJECT_NAME ToolBox)
project(${PROJECT_NAME} VERSION 1.0.0 LANGUAGES CXX)

file(GLOB source_files
	"src/*.cpp"
)

file(GLOB header_files
	"include/*.hpp"
)

set(SOURCES ${source_files} ${header_files})

add_executable(${PROJECT_NAME} ${SOURCES})
target_include_directories(${PROJECT_NAME} PRIVATE "include")
target_link_libraries(${PROJECT_NAME})