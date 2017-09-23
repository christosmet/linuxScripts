#!/bin/bash

if [ -z "$1" ];then
    if [ "$(xset -q | sed 's/[0-9][0-9]: /\n/g' | grep 'Scroll Lock' | awk '{print $3}')" = "off" ];then
        xset led named "Scroll Lock"
    else
        xset -led named "Scroll Lock"
    fi

elif [ "$1" = "on" ];then
    xset led named "Scroll Lock"
elif [ "$1" = "off" ];then
    xset -led named "Scroll Lock"
elif [ "$1" = "-q" ];then
    xset -q | sed 's/[0-9][0-9]: /\n/g' | grep 'Scroll Lock' | awk '{print $3}'
else
    me="$(basename $0)"
    echo "Usage:\n\t$me on \t Turn Scroll Lock on"
    echo "\t$me off\t Turn Scroll Lock off"
    echo "\t$me    \t Toggle Scroll Lock"
    echo "\t$me -q \t Print Scroll Lock LED status (on/off)"
fi
