# tx2-camera-patches
Jetson TX2 Camera Patches Collection

The imx274 patches are to be used with the nvidia source for kernel and hardware. 

##Brief Overview of steps:

1.) Download the source bundle from the Jetson Download Center

2.) Unpack the "kernel" and "hardware" folders to /usr/src

3.) mkdir /home/work and chown to your username

4.) Change the permissions on /usr/src/kernel and /usr/src/hardware with chown

5.) Copy the patch files to this directory and apply with patch -p1 < {file_name}.patch

6.) Build the dtb and images with make -O.. tegra18_defconfig, make -O.. zImage make -O.. dtbs


The build output in /home/work can then be flashed with the ./flash.sh script found in the /Linux_for_Tegra folder (which can be downloaded from the Jetson Download Center).

##For detailed instructions, please refer to the Jetpack 3.3 L4T documentation provided by Nvidia.
