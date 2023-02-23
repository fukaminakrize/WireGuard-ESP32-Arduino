idf_component_register(SRC_DIRS "src" "src/crypto/refc"
                    INCLUDE_DIRS "src" "src/crypto/refc"
                    REQUIRES mbedtls esp_netif)

if(${IDF_VERSION_MAJOR} STREQUAL 5)
    set_source_files_properties(src/crypto/refc/x25519.c
            PROPERTIES COMPILE_FLAGS
            -Wno-error=stringop-overread)
endif()