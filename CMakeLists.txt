cmake_minimum_required(VERSION 3.18)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_TOOLCHAIN_FILE "${CMAKE_CURRENT_SOURCE_DIR}\\cmake\\aarch64-none-elf.cmake")

# set(CMAKE_FIND_ROOT_PATH_MODE_PROGRAM NEVER)
# set(CMAKE_FIND_ROOT_PATH_MODE_LIBRARY ONLY)
# set(CMAKE_FIND_ROOT_PATH_MODE_INCLUDE ONLY)

message("CMAKE_TOOLCHAIN_FILE ${CMAKE_TOOLCHAIN_FILE}")

message("CMAKE_MAKE_PROGRAM ${CMAKE_MAKE_PROGRAM}")
message("CMAKE_C_COMPILER ${CMAKE_C_COMPILER}")
message("CMAKE_CXX_COMPILER ${CMAKE_CXX_COMPILER}")
message("CMAKE_AR ${CMAKE_AR}")
message("CMAKE_LINKER_TYPE ${CMAKE_LINKER_TYPE}")
message("CMAKE_C_COMPILER_LINKER ${CMAKE_C_COMPILER_LINKER}") # READ ONLY
message("CMAKE_CXX_COMPILER_LINKER ${CMAKE_CXX_COMPILER_LINKER}") # READ ONLY
message("CMAKE_SYSTEM_PROCESSOR ${CMAKE_SYSTEM_PROCESSOR}")

# $(PREFIX)ld --section-start=.text=0 -o $(TARGET).elf $(TARGET).o
# $(PREFIX)objdump -D $(TARGET).elf > $(TARGET).lst
# $(PREFIX)objcopy $(TARGET).elf -O binary $(TARGET).bin

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

# set_target_properties(${target} PROPERTIES LINK_DEPENDS ${_cur_link_deps})

add_executable(${PROJECT_NAME}
    "src/main.cpp"
)

# set(ldscript_path ${LD_DIR}/${ldscript})
# target_link_libraries(${target} PRIVATE -T ${ldscript_path})
# set_target_properties(${target} PROPERTIES LINK_DEPENDS ${ldscript_path})

# target_link_libraries(${PROJECT_NAME} portaudio_static)
# target_link_options(${PROJECT_NAME} PRIVATE "-static")
