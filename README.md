使用方法
========

打 patch，编译

    patch -p1 -d tmk_keyboard/ < patches/001_gh60_new.patch
    ( cd tmk_keyboard/keyboard/gh60 && make clean && make all KYEMAP=hhkb )
    rsync -av tmk_keyboard/keyboard/gh60/gh60_lufa.hex tkg-toolkit/common/firmware/gh60-reva_b_c.hex

tkg-toolkit/linux/setup.sh 选择:

    Name:      GH60 RevA/B/C
    MCU:      atmega32u4
    Bootloader:  lufa_dfu
    Firmware:   gh60-reva_b_c.hex

刷机

    sudo tkg-toolkit/linux/reflash.sh
