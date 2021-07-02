## dual boot (windows & ubuntu)

### step: 01 | (installation type: something else)
```
EXAMPLE:

/dev/sbd
  /dev/sbd1 ntfs (system reserve)
  /dev/sbd2 ntfs
  
  /dev/sbd3 swap
  /dev/sbd4 ext4 /
  
 ----------------------
 boot loader: /dev/sbd4
```

### step 02 | (don't show os select option)
```
01) open default os: (windows)
02) install: EasyBCD
03) following this instruction:
    link: https://www.linuxandubuntu.com/home/how-to-dual-boot-windows-7-and-ubuntu
```

#### the end
