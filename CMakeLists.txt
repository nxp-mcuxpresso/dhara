#
# Copyright 2024 NXP
#
# SPDX-License-Identifier: ISC
#

if(CONFIG_MCUX_COMPONENT_middleware.dhara)
    mcux_component_version(2.0.0)
    mcux_add_source(
        SOURCES dhara/map.c
                dhara/map.h
                dhara/journal.c
                dhara/journal.h
                dhara/error.c
                dhara/error.h
                dhara/bytes.h
                dhara/nand.h
        BASE_PATH ${SdkRootDirPath}/middleware/dhara/
    )
    mcux_add_include(
        INCLUDES dhara
        BASE_PATH ${SdkRootDirPath}/middleware/dhara/
    )
endif()

if(CONFIG_MCUX_COMPONENT_middleware.dhara.dhara_ecc_bch)
    mcux_component_version(2.0.0)
    mcux_add_source(
        SOURCES ecc/bch.c
                ecc/bch.h
                ecc/gf13.c
                ecc/gf13.h
        BASE_PATH ${SdkRootDirPath}/middleware/dhara/
    )
    mcux_add_include(
        INCLUDES ecc
        BASE_PATH ${SdkRootDirPath}/middleware/dhara/
    )
endif()

if(CONFIG_MCUX_COMPONENT_middleware.dhara.dhara_ecc_hamming)
    mcux_component_version(2.0.0)
    mcux_add_source(
        SOURCES ecc/hamming.c
                ecc/hamming.h
        BASE_PATH ${SdkRootDirPath}/middleware/dhara/
    )
    mcux_add_include(
        INCLUDES ecc
        BASE_PATH ${SdkRootDirPath}/middleware/dhara/
    )
endif()
