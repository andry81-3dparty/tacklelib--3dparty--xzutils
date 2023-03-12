cmake_minimum_required(VERSION 3.0)

include(tacklelib/Project)

project("xz_lzma")

set(PROJECT_LIB_NAME xz_lzma)

tkl_check_var(REQUIRED PATH   XZUTILS_BRANCH_NAME) # ex: `5_2_5_release`

set(PROJECT_EXTERNALS_DIR "_externals")
set(XZUTILS_EXTERNAL_SOURCE_DIR "${CMAKE_CURRENT_LIST_DIR}/${PROJECT_EXTERNALS_DIR}/${XZUTILS_BRANCH_NAME}")


#tkl_check_var(REQUIRED PATH ARC_XZ_UTILS_ROOT)


find_library(XZ_LZMA_LIBRARY NAMES liblzma ${XZUTILS_EXTERNAL_SOURCE_DIR}/lib)
