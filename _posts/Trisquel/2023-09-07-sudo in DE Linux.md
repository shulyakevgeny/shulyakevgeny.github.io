---
layout: post
title:   sudo для Linux
category: Trisquel
---

**sudo in Linux**

$ su

\# nano /etc/sudoers

В указанном файле отыскивается строка

\# WHEEL_USERS ALL=(ALL) ALL

С коей и снимается символ комментария. 

При желании совсем облегчить себе жизнь та же процедура проделывается со строкой

\# WHEEL_USERS ALL=(ALL) ALL NOPASSWD: ALL