cmake_minimum_required(VERSION 2.8)
project(http-parser C)


set(HTTP_PARSER_INCLUDE_DIRS ${CMAKE_CURRENT_SOURCE_DIR} CACHE INTERNAL "Http parser include directories")

set(HTTP_PARSER_SOURCES
    ${CMAKE_CURRENT_SOURCE_DIR}/http_parser.c
)

set(HTTP_PARSER_LIBRARY http-parser CACHE INTERNAL "Http parser libary")
set(HTTP_PARSER_LIBRARIES ${HTTP_PARSER_LIBRARY} CACHE INTERNAL "Http parser libaries")

add_library(${HTTP_PARSER_LIBRARY} STATIC
    ${HTTP_PARSER_SOURCES})