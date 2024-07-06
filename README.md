<a name="readme-top"></a>

## About The Project

Apex Legends QEMU/KVM/DMA/Linux hack

This project is based on Chettoy apex_dma project.

Game version (Steam Only right now): v3.0.63.32

**Please delete the old offsets.ini after updating.**

## Execute the cheat

**apexsky_kvm:**

There are really only two steps:

1. Run the game on a windows guest in a kvm virtual machine.
2. Run the compiled apex_dma program on the Linux host.

    ```shell
    cd apex_kvm/build && ./apex_dma
    ```

Additional information:

1. Please put the overlay window on the top of the VM screen after start. For example, on top of the looking-glass window.
2. For a better experience, please passthrough your keyboard, mouse or controller into the VM.
3. Press Insert to open the Overlay menu. Press and hold the Insert key to temporarily interact with the overlay.
4. If you are using a resolution other than 1080p, save the configuration and then modify the `screen_width` and `screen_height` in *settings.toml* and reload the configuration.

## Build from source

**Requirements:**

* C++ toolchain
* Rust toolchain (Standard version)
* CMake
* Git

**Install Rust:**

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
Chose the first option to download the standard version (to get your cheat working, it is mandatory to use a standard version)

**Install Build Dependencies (Ubuntu):**

```bash
sudo apt install cmake clang protobuf-compiler libusb-1.0-0-dev libzstd-dev libglfw3-dev libfreetype6-dev libvulkan-dev libxrandr-dev libxinerama-dev libxcursor-dev libxi-dev libxext-dev wayland-protocols libwayland-dev libxkbcommon-dev
```

**Install Build Dependencies (Arch):**

```bash
sudo pacman -S cmake clang protobuf libusb zstd glfw-x11 freetype2 vulkan-headers libxrandr libxinerama libxcursor libxi libxext wayland-protocols wayland libxkbcommon imagemagick
```

**Build:**

```shell
git clone --recurse https://github.com/0x69pi/apexlegends_kvm
cd apexlegends_kvm/apex_kvm
git submodule update --init --recursive
cd apex_dma
./build.sh
```


## Acknowledgments

* [memflow](https://github.com/memflow/memflow)
* [ratatui](https://ratatui.rs)
* [tracel-ai/burn](https://github.com/tracel-ai/burn)
* [TheCruz's Apex Aimbot+ESP](https://www.unknowncheats.me/forum/apex-legends/369786-apex-directx-wallhack-smooth-aimbot-source.html)
* [h33p/vmread](https://github.com/h33p/vmread)
* [Y33Tcoder/EzApexDMAAimbot](https://github.com/Y33Tcoder/EzApexDMAAimbot)
* [MisterY52/apex_dma_kvm_pub](https://github.com/MisterY52/apex_dma_kvm_pub)
* [KrackerCo/apex_dma_kvm_pub](https://github.com/KrackerCo/apex_dma_kvm_pub)
* [CasualX/apexdream](https://github.com/CasualX/apexdream)
* [Nexilist/xap-client](https://github.com/Nexilist/xap-client)
* [Xnieno/ApexDreamForYou](https://github.com/Xnieno/ApexDreamForYou)

