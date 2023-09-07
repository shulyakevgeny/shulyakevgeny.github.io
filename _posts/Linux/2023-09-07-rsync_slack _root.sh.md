---
layout: post
title:  rsync для резервного копирования
category: Linux
---

#linux

#!/bin/sh

rsync -aAXvzh / --exclude={"/home/*","/dev/*","/proc/*","/sys/*","/tmp/*","/run/*","/mnt/*","/media/*","/lost+found"} /home/jenit/2022-08-13/

---

sudo rsync -aAXvzh / --exclude={"/home/*","/dev/*","/proc/*","/sys/*","/tmp/*","/run/*","/mnt/*","/media/*","/lost+found"} /home/jenit/2022-08-13/ 