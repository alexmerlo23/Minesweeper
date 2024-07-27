cmake_minimum_required(VERSION 3.24)
project(minesweeperTest)

set(CMAKE_CXX_STANDARD 14)

add_executable(minesweeperTest src/main.cpp src/Board.cpp src/Board.h src/Tile.cpp src/Tile.h src/TextureManager.cpp src/TextureManager.h src/Helpers.cpp src/Helpers.h src/Random.cpp src/Random.h)

set(SFML_STATIC_LIBRARIES TRUE)
set(SFML_DIR C:/SFML/lib/cmake/SFML)
find_package(SFML COMPONENTS system window graphics audio network REQUIRED)

include_directories(c:/SFML/include/SFML)
target_link_libraries(minesweeperTest sfml-system sfml-window sfml-graphics sfml-audio)