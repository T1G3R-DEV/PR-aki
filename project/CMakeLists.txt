# CMakeList.txt: CMake-Projekt für "PR-aki". Schließen Sie die Quelle ein, und definieren Sie
# projektspezifische Logik hier.
#


#https://medium.com/@RileyEntertainmentGameDev/sfml-as-a-dependency-in-a-cmake-project-a37be848243e 




cmake_minimum_required (VERSION 3.8)

project ("PR-aki")

set(BUILD_SHARED_LIBS OFF)

include(FetchContent)
set(BUILD_SHARED_LIBS OFF)
FetchContent_Declare(
 SFML
 GIT_REPOSITORY https://github.com/SFML/SFML.git
 GIT_TAG 2.5.1
)
FetchContent_MakeAvailable(SFML)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED true)


# Fügen Sie der ausführbaren Datei dieses Projekts eine Quelle hinzu.
add_executable (PR-aki "Main.cpp" )

target_link_libraries(
 PR-aki
 sfml-graphics
)
# TODO: Fügen Sie bei Bedarf Tests hinzu, und installieren Sie Ziele.
