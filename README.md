# Infra_linux

crontab 사진 옮기기 - 폰 갤러리


#crontab -e
* * * * * /usr/sh ~tommy/timelap.sh
#여기서 ~는 /home/ 을 뜻한다


#!/bin/bash
date >> ~tommy/log/timelap.log
echo "hello" >> ~tommy/log/timelap.log
#python3 /home/tommy/data_augmentation/gitsave/Python/client/client.py


tail -f timelap.log

sh ~tommy/tielap

/bin/sh



timelap.log

timelap.sh
이걸만든 이유는  python3 --- 을실험하기 위한것

crontab -e 에 등록하고싶은거지

timelap.sh을


점검했어 log파일을 통해 ->

crontab 쓸때 는 항상 log를 남겨야 한다

 

tcp/ip 기반 소스
