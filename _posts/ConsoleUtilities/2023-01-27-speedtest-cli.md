---
layout: post
title: Узнать скорость интернета
category: ConsoleUtilities
---

*Узнать скорость интернета не выходя из терминала можно узнать командой:*

- speedtest-cli

*Установить:*

- sudo dnf install speedtest-cli

*Запустить в терминале:*

- user@rosa ~$  speedtest-cli

*Вывод:*
              
        Retrieving speedtest.net configuration...
        
        Testing from Rostelecom (00.00.00.00)...
        
        Retrieving speedtest.net server list...
        
        Selecting best server based on ping...
        
        Hosted by Pautina-LLC (Khabarovsk) [1723.19 km]: 56.33 ms
        
        Testing download speed................................................................................
        
        Download: 50.98 Mbit/s
        
        Testing upload speed......................................................................................................
        
        Upload: 50.30 Mbit/s

## Вы можете посмотреть результат проверки в байтах, а не в битах:

- speedtest-cli --bytes        

## Если хотите поделиться результатом с друзьями, можно попросить программу создать изображение:

- speedtest-cli --share

## Для получения информации только о ping, скорости загрузки и отдачи:

- speedtest-cli --simple

## Чтобы вывести версию утилиты выполните:

- speedtest-cli --version
