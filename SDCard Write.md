# 教程
    如何给树莓派的SD卡烧录img系统镜像
    https://jingyan.baidu.com/article/358570f6a2e0e7ce4724fc1e.html

    如何将操作系统烧录到SD卡中？
    https://blog.csdn.net/a2213086589/article/details/89351075

    Windows SD card Tools:
    SDFormatter #Format SD Card
    win32diskimager # Write image to SD Card

# 编程
    linux下SD卡烧录程序
    https://blog.csdn.net/lushoumin/article/details/81866094

    【Linux】制作U-Boot烧写镜像到SD卡的过程（上篇)
    https://blog.csdn.net/qq_38410730/article/details/90373733

# tools:
    dd command

    烧写到SD卡
    烧写到SD卡，一般采用的是dd命令：
    sudo dd iflag=dsync oflag=dsync if=u-boot.16k of=/dev/sdb seek=1
    前两个选项iflag和oflag表示采取异步的方式，if表示输入文件，of表示输出设备，seek表示从第几个扇区开始烧写。
    dev是设备（device）的英文缩写。/dev这个目录对所有的用户都十分重要。因为在这个目录中包含了所有Linux系统中使用的外部设备。
    但是这里并不是放的外部设备的驱动程序，这一点和windows、dos操作系统不一样。
    它实际上是一个访问这些外部设备的端口。我们可以非常方便地去访问这些外部设备，和访问一个文件、一个目录没有任何区别。
