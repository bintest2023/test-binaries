# Manual how to use BinTest

1) Copy and paste this code to yours main CmakeLists.txt

```
set(file_url "https://github.com/bintest2023/test-binaries/raw/main/user-cmake/CmakeLists.txt")

file(MAKE_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/Cmake_dowload_bintest)

set(target_path "${CMAKE_CURRENT_SOURCE_DIR}/Cmake_dowload_bintest/CmakeLists.txt")

file(DOWNLOAD ${file_url} ${target_path} STATUS status)

set(variables_list "Example" ) # list of tests wich you want to download 
set(USER_LIB "Example") # user input # directory with user source code

include(Cmake_dowload_bintest/CmakeLists.txt)

```
2) Select the names from this list : rational arrayd
3) Paste them into "variables_list"
4) Choose and write name of yours folder with code which one do you want to test in "USER_LIB"

# Warning

In yours folder whose name did you use in paragraph 4 you should have CmakeLists.txt with "add_subdirectory(...)", names (...) must be the same as the tests you have selected. 

CmakeLists.txt should be similar to this: 
 
```CmakeLists.txt 
add_subdirectory(rational)
add_subdirectory(arrayd)
```

If you have done all the points and paid attention to the warning, test it!



