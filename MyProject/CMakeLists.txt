cmake_minimum_required(VERSION 3.10)
project(MyProject)

# C++標準の設定
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# ヘッダーファイルのディレクトリを指定
include_directories(include)
include_directories(${CMAKE_SOURCE_DIR}/mylib/include)

# サブディレクトリの追加
add_subdirectory(mylib)

# 実行可能ファイルの指定
add_executable(MyProject src/main.cpp src/program.cpp)

# ライブラリをリンク
target_link_libraries(MyProject mylib)
