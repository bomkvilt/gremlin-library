cmake_minimum_required(VERSION 3.15)
include("cmake/gremlin/gremlin.cmake")

# ---------------------------| enviroment
# use a gloab vcpkg instance
GN_option(GN_vcpkg_vcpkgRoot "")

# tune directory names
GN_option(GN_dir_private "private")
GN_option(GN_dir_public "public")
GN_option(GN_dir_tests "tests")

# ---------------------------|

GN_init()
project("libs")
GN_subprojects(
    libs/boost
    libs/reflect
    libs/math
    )
