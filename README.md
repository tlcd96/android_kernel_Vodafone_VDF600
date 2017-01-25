# VDF600_kernel
#build:
export ARCH=arm
export SUBARCH=arm
export CROSS_COMPILE=~/android/kernel_source/toolchains/arm-linux-androideabi-4.8/bin/arm-linux-androideabi-
export PATH=$PATH:~/android/kernel_source/toolchains/arm-eabi-linaro-4.6.2/arm-eabi/bin


#1st build
#----------------------------
make msm8909-1gb_P809V50_defconfig
#make menuconfig
make -j4


export TARGET_PREBUILT_KERNEL=:~/android/kernel_source/arch/arm/boot/zImage-dtb



RE-builds
----------------------------
make clean
make oldconfig
make -j4
