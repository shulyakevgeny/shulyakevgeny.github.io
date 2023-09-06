---
layout: post
title:   Install qemu,virt-manager
category: Trisquel
---

#qemu #virt-manager

## Команды:

- sudo pacman -S qemu-desktop libvirt virt-manager

- sudo systemctl enable libvirtd

- sudo systemctl start libvirtd

- sudo virsh net-autostart default

- sudo pacman -S dnsmasq

- sudo virsh net-start default
