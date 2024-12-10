# SPDX-License-Identifier: Apache-2.0
# Copyright (C) 2022-2023, Advanced Micro Devices, Inc. All rights reserved.

add_subdirectory(driver)
add_subdirectory(shim)
include_directories(/usr/include/libdrm)
find_package(PkgConfig REQUIRED)
pkg_check_modules(LIBDRM REQUIRED libdrm)
include_directories(${LIBDRM_INCLUDE_DIRS})