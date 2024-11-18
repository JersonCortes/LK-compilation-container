#Linux Kernel compilation container

An easy way to compile the Linux Kernel in a Ubuntu container. The Dockerfile contains all minimal requirements for the compilation process as well as system utilities, networking and kernel documentation generation.

## Table of Contents
  - [Installation](#installation)
    - [Windows](#windows)
    - [macOS](#macos)
    - [Linux](#linux)
        - [Debian-based (e.g., Ubuntu)](#debian-based-ubuntu)
        - [RedHat-based (e.g., Fedora, CentOS)](#redhat-based-fedora-centos)
        - [Arch-based (e.g., Arch Linux, Manjaro)](#arch-based-arch-linux-manjaro)
  - [Usage](#usage)

## Installation

  First you must select your containerization tool. This example will make use of Podman which is OCI compliant but more examples will be added.
### Linux
#### Debian-based (e.g., Ubuntu)
  1. Open a terminal.
  2. Install dependencies:
    ```bash
    sudo apt-get update
    sudo apt-get -y install podman
  3. Clone this repository.
  ```bash
    git clone https://github.com/JersonCortes/LK-compilation-container.git
  ```   ```
#### RedHat-based (e.g., Fedora, CentOS)
  1. Open a terminal.
  2. Install dependencies:
    ```bash
    sudo dnf -y install podman
    ```
  3. Clone this repository.
  ```bash
    git clone https://github.com/JersonCortes/LK-compilation-container.git
  ```
#### Arch-based (e.g., Arch Linux, Manjaro)
  1. Open the terminal.
  2. Install dependencies:
  ```bash
    sudo pacman -S podman
  ```
  3. Clone this repository.
  ```bash
    git clone https://github.com/JersonCortes/LK-compilation-container.git
  ```
## Usage
Once you've installed the project, you can start using it. The primary functionality of the project is to have a container with the minimal requirements for a LK compilation. Below are some examples of how to use it.
###Podman
  1. Generate your LK compilation image:
  ```bash
    podman built -t [IMAGE NAME:VERSION] [PATH TO DOCKERFILE]
  ```
  2. Crate the container:
  ```bash
    podman create -it --name [CONTAINER NAME] -v [KERNEL PATH]: [PATH INSIDE CONTAINER] /bin/bash
  ```
  3. Start the container:
  ```bash
    podman start -a [CONTAINER NAME]
  ```
  4. Start compiling.
