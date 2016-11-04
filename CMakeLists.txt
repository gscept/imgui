#-------------------------------------------------------------------------------
# imgui
#-------------------------------------------------------------------------------

INCLUDE_DIRECTORIES(./
					)
					
    set(SOURCES_files_imgui
		imconfig.h
		imgui_internal.h
		imgui.cpp
		imgui_draw.cpp
		imgui.h
		stb_textedit.h
		stb_truetype.h
		stb_rect_pack.h
    )
    source_group("imgui" FILES ${SOURCES_files_imgui})

    set(SOURCES_imgui
      ${SOURCES_files_imgui}
    )
    
	set(SOURCES_SRCS
	    ${SOURCES_imgui}
	)

add_library( imgui STATIC ${SOURCES_SRCS} )
SET_TARGET_PROPERTIES(imgui PROPERTIES FOLDER "extlibs")
N_SET_COMPILER_DEFAULTS(imgui)
