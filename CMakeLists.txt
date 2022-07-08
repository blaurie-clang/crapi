cmake_minimum_required(VERSION 3.14)

project(crapi
        VERSION 0.0.1
        DESCRIPTION ""
        HOMEPAGE_URL ""
        LANGUAGES C)

#
# Options
#


#
# Fetch Modules
#


#
# Configuration
#
set(CMAKE_C_STANDARD 99)

if (MSVC)
    add_compile_options(/W4 /WX)
else()
    add_compile_options(-Wall -Wextra -pedantic -Werror -Wstrict-aliasing -fno-omit-frame-pointer)
endif()

#
# Targets
#
add_executable(crapi
        src/main.c)