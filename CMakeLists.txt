cmake_minimum_required(VERSION 3.18)

set(CMAKE_SYSTEM_NAME Generic)
set(CMAKE_SYSTEM_PROCESSOR aarch64)

set(CMAKE_TRY_COMPILE_TARGET_TYPE STATIC_LIBRARY)

set(CMAKE_C_COMPILER aarch64-none-elf-gcc)
set(CMAKE_CXX_COMPILER aarch64-none-elf-g++)


# export AS="$USERPROFILE/Downloads/xpack-aarch64-none-elf-gcc-13.2.1-1.1-win32-x64/xpack-aarch64-none-elf-gcc-13.2.1-1.1/bin/aarch64-none-elf-as.exe"
# export CC="$USERPROFILE/Downloads/xpack-aarch64-none-elf-gcc-13.2.1-1.1-win32-x64/xpack-aarch64-none-elf-gcc-13.2.1-1.1/bin/aarch64-none-elf-gcc.exe"
# export LD="$USERPROFILE/Downloads/xpack-aarch64-none-elf-gcc-13.2.1-1.1-win32-x64/xpack-aarch64-none-elf-gcc-13.2.1-1.1/bin/aarch64-none-elf-ld.exe"

project("cpp-arm64-baremetal-playground")

# find_package(portaudio 19 EXACT REQUIRED) # PATHS "P:\\Downloads\\cpp-libraries\\portaudio\\build\\cmake\\portaudio")

# if(portaudio_FOUND)
#     message(STATUS "YES")
# else()
#     message(STATUS "NO")
# endif()

add_executable(${PROJECT_NAME}
    "src/main.cpp"
)

# target_link_libraries(${PROJECT_NAME} portaudio_static)
# target_link_options(${PROJECT_NAME} PRIVATE "-static")
