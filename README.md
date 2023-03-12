# libsundaowen_lzma457lib_src

## example

### git

```Shell
git submodule add -- "https://github.com/dnasdw/libsundaowen_lzma457lib_src.git" "dep/lzma457lib"
git submodule update --init --recursive "dep/lzma457lib"
```

### cmake

```CMake
#...
set(ROOT_SOURCE_DIR "${PROJECT_SOURCE_DIR}")
#...
include_directories("${ROOT_SOURCE_DIR}/dep/lzma457lib")
#...
add_subdirectory("${ROOT_SOURCE_DIR}/dep/lzma457lib" lzma457lib)
#...
set(src "${src}" "${sdw_lzma457lib_src}")
#...
if(UNIX OR MINGW)
  add_definitions("${sdw_lzma457lib_add_definitions_UNIX_OR_MINGW}")
endif()
#...
add_executable(app "${src}")
#...
```
