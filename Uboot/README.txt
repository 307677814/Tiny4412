uboot_tiny4412-master.zip
    友善之臂提供的uboot-2010.12,包含了制作sd卡的工具

    uboot写入SD卡的步骤
        1 cd uboot_tiny4412-master
        2 make tiny4412_config
        3 make
        4 cd uboot_tiny4412-master/sd_fuse
        5 make
        6 cd uboot_tiny4412-master/sd_fuse/tiny4412
        7 sudo dd if=/dev/zero of=/dev/mmcblk0 bs=1024 count=10240
        8 sudo ./sd_fusing.sh  /dev/mmcblk0 

uboot_kernel_4.4_device_tree.patch
    支持kernel-4.4 设备树功能的patch

uboot_for_kernel_4_4
    支持4.4内核设备树配置的uboot 
        1 ce uboot_for_kernel_4_4
        2 make tiny4412_config
        3 make
        4 cd uboot_tiny4412-master/sd_fuse
        5 make
        6 cd uboot_tiny4412-master/sd_fuse/tiny4412
        7 sudo dd if=/dev/zero of=/dev/mmcblk0 bs=1024 count=10240
        8 sudo ./sd_fusing.sh  /dev/mmcblk0 
