cpp-arm64-baremetal-playground
==============================

From https://github.com/dirkarnez/qemu-cortex-a7-baremetal

### TODOs
- [ ] delete CMake?
- [ ] remove direct referencing to startup.o inside `link_script.ld`, which CMake cannot do directly

### NOTES
- CMake is totally not embedded-friendly

### Tutorials
- https://github.com/whzinformatik/baremetal-arm/blob/master/doc/05_cmake.md?plain=1
- **[adafruit/tinyuf2: UF2 bootloader based on TinyUSB for embedded devices such as ESP32S2, STM32F4 and iMX RT10xx](https://github.com/adafruit/tinyuf2/tree/master)**