+++
date = '2026-02-16T11:44:59Z'
draft = true
title = 'Debian13 Dhcpd Apparmor'
+++
  101  cat /sys/module/apparmor/parameters/enabled
  102  sudo aa-status
  103  ps auxZ | grep -v '^unconfined'
  104  ls /usr/share/apparmor/extra-profiles/
  105  sudo ls /usr/share/apparmor/extra-profiles/
  106  apt-cache search apparmor
  107  sudo apt install apparmor-profiles-extra
  108  sudo ls /usr/share/apparmor/extra-profiles/
  109  ls -ltr /etc/apparmor.d
  110  apt-cache search apparmor
  111  sudo apt install apparmor-profiles
  112  sudo ls /usr/share/apparmor/extra-profiles/
  113  cat /usr/share/apparmor/extra-profiles/usr.sbin.dhcpd
  114  sudo dmesg|tail
  115  sudo cp /usr/share/apparmor/extra-profiles/usr.sbin.dhcpd /etc/apparmor.d
  116  sudo aa-complain /etc/apparmor.d/usr.sbin.dhcpd
  117  sudo apt install apparmor-utils
  118  sudo aa-complain /etc/apparmor.d/usr.sbin.dhcpd
  119  sudo dmesg|tail
