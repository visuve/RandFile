cmake_minimum_required(VERSION 3.16)

project("fstrinkets")

set(CMAKE_CXX_STANDARD 20)
set(CXX_STANDARD_REQUIRED ON)

if(MSVC)
	add_compile_options(/W4 /WX /MP)
	#add_compile_options(
	#	$<$<CONFIG:>:/MT>
	#	$<$<CONFIG:Debug>:/MTd>
	#	$<$<CONFIG:Release>:/MT>
	#)
else()
	add_compile_options(-Wall -Wextra -pedantic -Werror)
endif()

add_subdirectory("dir_clean")
add_subdirectory("rand_file")
add_subdirectory("drive_info")
add_subdirectory("sloth_copy")
add_subdirectory("entropy_calc")
add_subdirectory("file_info")
add_subdirectory("bit_flipper")
add_subdirectory("file_watcher_simple")
add_subdirectory("file_watcher")
add_subdirectory("perus64")
add_subdirectory("file_search")
add_subdirectory("file_replace")

