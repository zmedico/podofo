ADD_EXECUTABLE(podofogc podofogc.cpp)

TARGET_LINK_LIBRARIES(podofogc ${PODOFO_LIB})
SET_TARGET_PROPERTIES(podofogc PROPERTIES COMPILE_FLAGS "${PODOFO_CFLAGS}")
ADD_DEPENDENCIES(podofogc ${PODOFO_DEPEND_TARGET})
INSTALL(TARGETS podofogc
	RUNTIME DESTINATION "bin")
