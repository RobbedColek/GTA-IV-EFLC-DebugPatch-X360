# GTA-IV-EFLC-DebugPatch-X360

This is just a simple patch for leaked **Grand Theft Auto IV - Episodes from Liberty City** debug .exe for Xbox 360.
This will only work with untouched **default_us.exe (Filetime:  4AC21D44 - Tue Sep 29 16:44:20 2009) [CRC32: 1257ADAC]**!

### How does it work?
The original .exe has dongle protection. Without dongle with file **root.sys** with proper contents on it, this build would just endlessly loop loading screen. This patch NOPs calls to that file and bypasses blocks that are responsible for checking it.

### How to use patch?
* Download xdelta from [here](https://github.com/jmacd/xdelta-gpl/releases).
* Download **default_us.exe.vcdiff** from this repo.
* Obtain untouched **default_us.exe (Filetime:  4AC21D44 - Tue Sep 29 16:44:20 2009) [CRC32: 1257ADAC]**.
* Put all files in one directory.
* Use command below to patch untouched .exe.
```sh
xdelta.exe -v -d -s "default_us.exe" "default_us.exe.vcdiff" "default_us_patched.xex"
```
* Put output **default_us_patched.xex** in directory with your GTA IV - EFLC retail files.
* Done!
* **NOTE:** If you're going to use it on RGH, you'll need to patch output .xex with xextool.

![Screen 1](https://i.postimg.cc/KvQJkXzd/Screenshot-2019-01-27-21-42-56.png)
![Screen 2](https://i.postimg.cc/63s0JtjG/Screenshot-2019-01-27-21-43-30.png)