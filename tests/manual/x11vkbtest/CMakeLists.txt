# Copyright (C) 2022 The Qt Company Ltd.
# SPDX-License-Identifier: BSD-3-Clause

if(NOT QT_BUILD_STANDALONE_TESTS AND NOT QT_BUILDING_QT)
    cmake_minimum_required(VERSION 3.16)
    project(x11vkbtest LANGUAGES CXX)
    find_package(Qt6BuildInternals REQUIRED COMPONENTS STANDALONE_TEST)
endif()

# Generated from x11vkbtest.pro.

#####################################################################
## x11vkbtest Binary:
#####################################################################

find_package(Qt6 ${PROJECT_VERSION} QUIET CONFIG OPTIONAL_COMPONENTS Charts)
if(NOT TARGET Qt::Charts)
    message("Manual test x11vkbtest won't be built, because Qt::Charts was not found.")
    return()
endif()

qt_internal_add_manual_test(x11vkbtest
    GUI
    SOURCES
        colors.h
        filehelper.cpp filehelper.h
        main.cpp
        memorymonitor.cpp memorymonitor.h
        mousesimulator.cpp mousesimulator.h
        processhandler.cpp processhandler.h
        startclose.cpp startclose.h
        testbase.cpp testbase.h
        testenglishletters.cpp testenglishletters.h
        testlanguagechange.cpp testlanguagechange.h
        testreporter.cpp testreporter.h
        testthread.cpp testthread.h
        windowhelper.cpp windowhelper.h
    DEFINES
        QT_DEPRECATED_WARNINGS
    LIBRARIES
        Qt::Charts
        Qt::Gui
        X11::X11
        Xtst
        xdo
)
