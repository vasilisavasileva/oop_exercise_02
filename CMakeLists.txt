cmake_minimum_required(VERSION 2.8) # Проверка версии CMake.
# Если версия установленой программы
# старее указаной, произойдёт аварийный выход.

project(2lab) # Название проекта

set(SOURCE_EXE main.cpp) # Установка переменной со списком исходников для исполняемого файла

set(SOURCE_LIB Bitstring.cpp) # Тоже самое, но для библиотеки

add_library(bitstring STATIC ${SOURCE_LIB}) # Создание статической библиотеки с именем foo

add_executable(main ${SOURCE_EXE}) # Создает исполняемый файл с именем main

target_link_libraries(main bitstring)