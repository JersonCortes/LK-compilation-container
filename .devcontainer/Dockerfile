FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

#Commented software should already be included in the base image

RUN sudo apt-get update && \
apt-get upgrade -y && \
sudo apt-get install -y \
#Kernel compilation (Essential)
clang \
rustc \
bindgen \
flex \
bison \
pahole \
bc \
u-boot-tools \
#Non sure
libelf \
#Optional
global \
gawk \ 
#System utilities
kmod \
jfsutils \
reiserfsprogs \
xfsprogs \
squashfs-tools \
btrfs-progs \
pcmciautils \
quota \
udev \
#grub \
#Networking
ppp \
nfs-common \
iptables \
#mcelog \
#Documentation Generation
sphinx \
#Non-determined
zstd \ 
cpio 

WORKDIR /workspace
