# CMakeList.txt: проект CMake для CMakeProject1; включите исходный код и определения,
# укажите здесь логику для конкретного проекта.
#
cmake_minimum_required (VERSION 3.8)

# Добавьте источник в исполняемый файл этого проекта.
add_executable (CMakeProject1  "morph.h" "geometricTool.h" "Utility.h" "Utility.cpp" "geometricTool.cpp")
find_package(ImageMagick)
find_package(ImageMagick COMPONENTS Magick++)
find_package(ImageMagick COMPONENTS convert)
find_package(ImageMagick COMPONENTS Magick++ convert)

include_directories(${ImageMagick_INCLUDE_DIRS})
target_link_libraries(CMakeProject1 ${ImageMagick_LIBRARIES})
# TODO: Добавьте тесты и целевые объекты, если это необходимо.
