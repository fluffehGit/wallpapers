#!/bin/bash

TOTALPICS=$(ls $HOME/Pictures/Wallpapers/*.jpg | wc --lines);
PIC=$(ls $HOME/Pictures/Wallpapers/*.jpg | awk "NR==$(( $RANDOM % ${TOTALPICS} + 1 )) {print}");

echo $PIC;

sed --in-place "s#=.*.jpg#=${PIC}#g" $HOME/.config/nitrogen/bg-saved.cfg;

nitrogen --restore;
