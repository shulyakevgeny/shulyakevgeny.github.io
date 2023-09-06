#linux 

Поместить в ~./fluxbox/startup  (рабочий)
setxkbmap -layout "us,ru," -option "grp:ctrl_shift_toggle,grp_led:scroll"


перепробовал множество вариантов:

~./fluxbox/startup    (рабочий)
setxkbmap -layout "us,ru," -option "grp:ctrl_shift_toggle,grp_led:scroll"

sudo dpkg-reconfigure keyboard-configuration

setxkbmap -layout 'us,ru(winkeys)' -option 'grp:alt_shift_toggle'

xorg.conf:

Section "InputDevice"
Identifier "Generic Keyboard"
Driver "kbd"
Option "CoreKeyboard"
Option "XkbRules" "xorg"
Option "XkbModel" "pc105"
Option "XkbLayout" "us,ru(winkeys)"
Option "XkbVariant" ","
Option "XkbOptions" "grp:ctrl_shift_toggle,grp_led:scroll".