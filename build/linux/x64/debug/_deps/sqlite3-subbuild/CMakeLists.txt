# Distributed under the OSI-approved BSD 3-Clause License.  See accompanying
# file Copyright.txt or https://cmake.org/licensing for details.

cmake_minimum_required(VERSION 3.20.5)

# We name the project and the target for the ExternalProject_Add() call
# to something that will highlight to the user what we are working on if
# something goes wrong and an error message is produced.

project(sqlite3-populate NONE)



include(ExternalProject)
ExternalProject_Add(sqlite3-populate
                     "UPDATE_DISCONNECTED" "False" "URL" "https://sqlite.org/2023/sqlite-autoconf-3430000.tar.gz"
                    SOURCE_DIR          "/home/ec2-user/environment/budget_tracker/build/linux/x64/debug/_deps/sqlite3-src"
                    BINARY_DIR          "/home/ec2-user/environment/budget_tracker/build/linux/x64/debug/_deps/sqlite3-build"
                    CONFIGURE_COMMAND   ""
                    BUILD_COMMAND       ""
                    INSTALL_COMMAND     ""
                    TEST_COMMAND        ""
                    USES_TERMINAL_DOWNLOAD  YES
                    USES_TERMINAL_UPDATE    YES
)


