+++
date = '2026-02-25T07:51:26Z'
draft = true
title = 'Mount_error_79'
+++

-> % sudo mount -a
mount error(79): Can not access a needed shared library
Refer to the mount.cifs(8) manual page (e.g. man mount.cifs) and kernel log messages (dmesg)

sudo apt install linux-modules-extra-$(uname -r)

-> % sudo mount -a

-> % df -Th|grep cifs
//u480294.your-storagebox.de/backup cifs   1.0T  711G  314G  70% /backup
