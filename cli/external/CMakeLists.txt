Include(FetchContent)

cmake_policy(SET CMP0077 NEW)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

FetchContent_Declare(
    Catch2
    GIT_SHALLOW    TRUE
    GIT_REPOSITORY https://github.com/catchorg/Catch2.git
    GIT_TAG        v3.5.3
)

set(SOCKPP_BUILD_SHARED OFF)
set(SOCKPP_BUILD_STATIC ON)

FetchContent_Declare(
    sockpp
    GIT_SHALLOW    TRUE
	GIT_REPOSITORY https://github.com/fpagliughi/sockpp.git
    GIT_TAG        v0.8.1
)

FetchContent_Declare(
	strong_type
	GIT_SHALLOW		TRUE
	GIT_REPOSITORY	https://github.com/rollbear/strong_type.git
	GIT_TAG			v14
)

FetchContent_Declare(
    libassert
    GIT_SHALLOW     FALSE
    GIT_REPOSITORY  https://github.com/jeremy-rifkin/libassert.git
 #   GIT_TAG         v2.0.0-alpha
    GIT_TAG         e7e3c35b415761e11c268436e6d1659d5a3fdbf5
)

FetchContent_MakeAvailable(Catch2 sockpp strong_type libassert)
