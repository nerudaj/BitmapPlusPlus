cmake_minimum_required( VERSION 3.10 )

include ( CPM.cmake )

CPMAddPackage ( "gh:nerudaj/BitmapPlusPlus#master" )

project ( demo )

add_executable( ${PROJECT_NAME}
    "${CMAKE_CURRENT_SOURCE_DIR}/../../examples/draw_primitives.cpp"
)

target_link_libraries( ${PROJECT_NAME} LINK_PRIVATE bpp::BitmapPlusPlus )
