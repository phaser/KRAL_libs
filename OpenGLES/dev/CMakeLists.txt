cmake_minimum_required (VERSION 2.8)

SET (PROJ_NAME "OpenGLES")
PROJECT (${PROJ_NAME})

IF (WIN32)
    export_library(${PROJ_NAME})
ELSE (WIN32)
	if (ANDROID)
        add_to_link_libs("GLESv2")
    endif (ANDROID)

    if (LINUX)
        add_to_link_libs("GL")
    endif (LINUX)
ENDIF (WIN32)


