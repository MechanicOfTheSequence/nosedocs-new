Prometheus has NOT been licensed.

Licensing Prometheus...

http://www.ollydbg.de/

-----

youtube-dl -f bestaudio


------

install ubuntu: https://www.microsoft.com/en-us/p/ubuntu/9nblggh4msv6
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
choco install qemu
choco install vcxsrv

---

export DISPLAY=$(cat /etc/resolv.conf | grep nameserver | awk '{print $2}'):0
git clone https://github.com/SerenityOS/serenity
cd serenity
cd Toolchain
./BuildIt.sh
cd ..
cd Build
rm -rf *
cmake .. -G Ninja
ninja
ninja install
ninja image
ninja run

sudo apt-get update
sudo apt install build-essential cmake curl libmpfr-dev libmpc-dev libgmp-dev e2fsprogs qemu-system-i386 qemu-utils
sudo apt install gcc-10 g++-10 ninja-build
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-10 900 --slave /usr/bin/g++ g++ /usr/bin/g++-10


export SERENITY_QEMU_BIN='/mnt/c/Program Files/qemu/qemu-system-i386.exe'
export SERENITY_DISK_IMAGE='\\wsl$\Ubuntu-20.04\home\mecha\serenity\Build\_disk_image'
make run
