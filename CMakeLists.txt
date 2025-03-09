cmake_minimum_required(VERSION 3.25)
project(PNTV)

set(INCLUDE_DIR src/include)
set(SRC_DIR src)

file(GLOB HEADER_FILES ${INCLUDE_DIR}/*.h) 
file(GLOB SOURCE_FILES ${SRC_DIR}/*.c)


add_executable(PNTV ${SOURCE_FILES} ${HEADER_FILES})

# target_link_libraries(PNTV PRIVATE LIB::LIB)

target_include_directories(PNTV PRIVATE ${INCLUDE_DIR})