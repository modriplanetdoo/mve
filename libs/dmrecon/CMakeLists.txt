file (GLOB HEADERS "*.h")
file (GLOB SOURCES "[^_]*.cc")

add_library(mve_dmrecon STATIC ${SOURCES} ${HEADERS})
set_target_properties(mve_dmrecon PROPERTIES DEBUG_POSTFIX ${MVE_LIBS_DEBUG_POSTFIX})

install(TARGETS mve_dmrecon DESTINATION lib)
install(FILES ${HEADERS} DESTINATION include/mve/dmrecon)
