# Copyright (C) 2022 The Qt Company Ltd.
# SPDX-License-Identifier: BSD-3-Clause

if(NOT QT_BUILD_STANDALONE_TESTS AND NOT QT_BUILDING_QT)
    cmake_minimum_required(VERSION 3.16)
    project(quickcontrols2 LANGUAGES CXX)
    find_package(Qt6BuildInternals REQUIRED COMPONENTS STANDALONE_TEST)
endif()

# Generated from quickcontrols2.pro.

#####################################################################
## quickcontrols2 Binary:
#####################################################################

qt_internal_add_manual_test(quickcontrols2
    GUI
    SOURCES
        main.cpp
    LIBRARIES
        Qt::Gui
        Qt::Qml
        Qt::Quick
)

# Resources:
set(main_resource_files
    "main.qml"
)

qt_internal_add_resource(quickcontrols2 "main"
    PREFIX
        "/"
    FILES
        ${main_resource_files}
)


#### Keys ignored in scope 1:.:.:quickcontrols2.pro:<TRUE>:
# QML_IMPORT_PATH = <EMPTY>
