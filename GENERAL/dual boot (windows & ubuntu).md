## dual boot (windows & ubuntu)

### step 01 (select boot loader)
```
case 01) if (windows & ubuntu is in same DRIVE)
==============================================
/dev/sbd
  /dev/sbd1 ntfs (system reserve)
  /dev/sbd2 ntfs
  /dev/sbd3 swap
  /dev/sbd4 ext4 /
 
/dev/sbad
  /dev/sbad1 ntfs
  /dev/sbad2 ntfs
===============================================
boot loader: /dev/sbd



case 02) if (windows & ubuntu is different DRIVE)
=================================================
/dev/sbd
  /dev/sbd1 ntfs (system reserve)
  /dev/sbd2 ntfs
 
/dev/sbad
  /dev/sbad1 ntfs
  /dev/sbad2 ntfs
  /dev/sbad3 swap
  /dev/sbad4 ext4 /
===============================================
boot loader: /dev/sbad4
AND FOLLOW: step 02 (if don't show os select option)
```

### step 02 | (don't show os select option)
```
01) open default os: (windows)
02) install: EasyBCD
03) following this instruction:
    link: https://www.linuxandubuntu.com/home/how-to-dual-boot-windows-7-and-ubuntu
```

#### the end
