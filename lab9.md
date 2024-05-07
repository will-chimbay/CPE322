# Lab 9 - Data Analysis

Ran:
- sudo apt install libxml2-dev libxslt1-dev
- sudo pip3 install -U lxml pyang
- cp ~/iot/lesson9/intrusiondetection.yang ~/demo
- cd ~/demo
- cat intrusiondetection.yang
- pyang -f yin -o intrusiondetection.yin intrusiondetection.yang
- cat intrusiondetection.yin
- pyang -f uml -o intrusiondetection.uml intrusiondetection.yang --uml-no=stereotypes,annotation,typedef
- cat intrusiondetection.uml

ALongside corresponding setup for pinta and gump -

PINTA: 

<img width="737" alt="image" src="https://github.com/will-chimbay/CPE322/assets/123396327/ac18261a-dec8-4712-8236-b3db33920f54">

GUMP:

<img width="797" alt="image" src="https://github.com/will-chimbay/CPE322/assets/123396327/87cc9fcb-2094-4ab0-905d-17bd3be73a00">
