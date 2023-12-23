# ライブラリのためのCMakeLists.txt

# ヘッダファイルのディレクトリを指定
include_directories(include)

# ライブラリの生成
add_library(mylib src/mylib.cpp)
