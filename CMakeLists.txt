cmake_minimum_required(VERSION 3.11 FATAL_ERROR)

project(
  plf_list
  DESCRIPTION "A high-performance drop-in replacement for std::list"
  HOMEPAGE_URL "https://www.plflib.org/list.htm"
  LANGUAGES CXX
  VERSION 2.3)

add_library(plf_list INTERFACE)
target_include_directories(plf_list INTERFACE include/)

include(CMakePackageConfigHelpers)

install(
  TARGETS plf_list
  INCLUDES
  DESTINATION include)

write_basic_package_version_file(
  "${PROJECT_NAME}ConfigVersion.cmake"
  VERSION ${PACKAGE_VERSION}
  COMPATIBILITY SameMajorVersion)

# TODO continue here
# https://cliutils.gitlab.io/modern-cmake/chapters/install/installing.html
install(EXPORT)

# TODO how to add ctest
