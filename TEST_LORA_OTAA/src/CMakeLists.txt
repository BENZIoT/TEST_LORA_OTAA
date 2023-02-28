# This file was automatically generated for projects
# without default 'CMakeLists.txt' file.

FILE(GLOB_RECURSE app_sources ${CMAKE_SOURCE_DIR}/src/*.*)

# set(COMPONENT_SRCDIRS "src/aes src/hal src/lmic")
# set(COMPONENT_ADD_INCLUDEDIRS "include")
# register_component()

# set(COMPONENT_SRCDIRS
#     "src"
#     "src/aes"
#     "src/hal"
#     "src/lmic"
# )
# set(COMPONENT_ADD_INCLUDEDIRS
#     "include"
# )
# set(COMPONENT_REQUIRES
#     nvs_flash
#     mbedtls
#     driver
#     esp_event
#     esp_timer
# )

# register_component()

if (IDF_VER STRGREATER_EQUAL "v4.0")
target_compile_options(${COMPONENT_LIB} PRIVATE -Wno-expansion-to-defined)
endif()


idf_component_register(SRCS ${app_sources})
