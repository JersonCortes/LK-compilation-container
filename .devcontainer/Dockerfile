FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

RUN sudo apt-get update && \
apt-get upgrade -y && \
sudo apt-get install -y \
clang \
rustc \
bindgen \
flex \
bison \
pahole \
kmod \
jfsutils \
reiserfsprogs \
xfsprogs \
squashfs-tools \
btrfs-progs \
pcmciautils \
quota \
ppp \
nfs-common \
udev \
iptables \
bc \
sphinx \
cpio \
global \
u-boot-tools \
#mcelog \
#grub \
gawk \
libelf \
zstd 


#RUN sudo apt-get install --no-install-recommends -y \
WORKDIR /workspace
