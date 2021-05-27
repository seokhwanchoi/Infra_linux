# Infra_linux

crontab 사진 옮기기 - 폰 갤러리


#crontab -e
* * * * * /usr/sh ~tommy/timelap.sh
#여기서 ~는 /home/ 을 뜻한다


#!/bin/bash
date >> ~tommy/log/timelap.log   
echo "hello" >> ~tommy/log/timelap.log
#python3 -u /home/tommy/data_augmentation/gitsave/Python/client/client.py >> ~tommy/log/timelap.log 2>&1

-u     : unbuffered binary stdout and stderr; also PYTHONUNBUFFERED=x
         see man page for details on internal buffering relating to '-u'
         
         https://stackoverflow.com/questions/14258500/python-significance-of-u-option

2>&1 는 표준에러를 표준출력으로 redirection 하라는 의미입니다.
리다이렉션 : 출력의 방향을 바꾸는 것

0 : 표준입력

1 : 표준출력

2 : 표준에러

리다이렉션이란,
말 그대로 출력의 방향을 바꾸는 것을 말한다. 예를 들어서 일반 컴퓨터의 표준 출력 장치는 모니터이고 표준 입력 장치는 키보드이다. 출력의 방향을 바꾼다는 것은 모니터로 출력 되어야 할 내용을 파일로 저장을 시킨다든지 또는 다른 장치, 즉 통신 포트나 프린터로 출력의 방향을 바꿀 수 있다.




처음 "> /dev/null" 은 표준출력을 /dev/null로 보내고 (즉, 버린다는 뜻)이고 두번째 부분인 "2>&1"은 표준에러를 표준출력이 보내진 곳과 동일한 곳으로 보낸다는 뜻이다.


<     filename   입력 방향을 바꾼다.
>     filename   출력 방향을 바꾼다.
>>   filename   출력에 덧붙인다.
2>   filename   오류의 방향을 바꾼다.
2>> filename   오류의 방향을 바꾸고 덧붙인다.
&>  filename   출력과 오류를 리다이렉션 한다.
>&  filename   오류와 출력을 리다이렉션 한다.
1>&2             출력을 오류로 내보낸다.
2>&1             오류를 출력으로 내보낸다.
>|                출력을 리다이렉션 할 때 NOCLOBBER 설정을 무시한다
<>  filename  장치 파일(/dev)이면, 표준 출력, 표준 입력 등에 모두 사용한다.


출처: https://sinpk.tistory.com/entry/21-의미 [IT]


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


(모바텀) vim 편집기 

윈도우에서 리눅스로 붙여넣기 shift insert
ctrl insert , ctrl shift c , ctrl shift v

h, j, k, l - 좌,하,상,우 커서이동

i - 현재 커서 위치에 Insert 하기
I - 현재 줄 맨앞에 Insert 하기
a - 현재 커서 다음칸에 Insert 하기
A - 현재 줄 맨뒤에 Insert 하기
O - 윗줄에 Insert 하기
o - 아랫줄에 Insert 하기

w - 단어 첫글자로 이동하기
W - 화이트스페이스 단위로 다음 글자로 이동하기
b - 백워드 방향으로 단어의 첫글자로 이동하기
B- 백워드 방향으로 화이트스페이스 단위로 다음 글자로 이동하기
e - 단어의 마지막 글자로 이동하기
ge - 백워드 방향으로 단어의 마지막 글자로 이동하기
gg - 문서 맨 앞으로 이동
G - 문서 맨끝으로 이동
^ - 문장 맨 앞으로 이동
0 - 라인 맨 앞으로 이동
$ - 문장 맨 뒤로 이동
f문자 - 문자의 위치로 이동 ; 를 누르면 계속 이동
F문자 - 백워드로 문자의 위치로 이동
t문자 - 문자의 앞위치로 이동
T문자 - 백워드방향으로 문자의 앞위치로 이동

/단어 - 문서에서 단어 찾기 n이나 N으로 다음/이전 찾기
* - 현재 단어를 포워드 방향으로 찾기
# - 현재 단어를 백워드 방향으로 찾기

Ctrl + f - 다음 페이지 이동
Ctrl + b - 이전 페이지 이동
Ctrl + u - 페이지절반만큼 다음으로 이동
Ctrl + d - 페이지절반만큼 이전으로 이동
H - 현재 화면의 맨 위라인으로 이동
M - 현재 화면의 중간 라인으로 이동
L - 현재 화면의 마지막 라인으로 이동

]] - 포워드 방향으로 여는 컬리 블레이스( { )로 이동
[[ - 백워드 방향으로 여는 컬리 블레이스( { )로 이동
][ - 포워드 방향으로 닫는 컬리 블레이스( { )로 이동
[] - 백워드 방향으로 닫는 컬리 블레이스( { )로 이동
% - {}나 ()에서 현재 괄호의 짝으로 이동

dd - 현재 줄 잘라내기
dw - 단어 잘라내기
yy - 현재 줄 복사하기
p - 붙혀넣기
r - 현재 글자 교체하기
u - Undo
Ctrl + R : Redo
x - 현재 글자 지우기
X - 앞의 글자 지우기
> - 들여쓰기
< - 내어쓰기
. - 이전 명령어를 다시 실행

v - 비쥬얼모드(비쥬얼 모드에서 커서 이동해서 블럭지정 가능)
y - 복사하기
c - 잘라내기
cw - 단어 잘라내기
J - 다음 라인을 현재 줄의 끝으로 이어 붙힘
~ : 선택 문자 대소문자 변경
Ctrl + A : 숫자를 증가시키기
Ctrl + X : 숫자를 감소시키기

:w - 문서 저장하기
:q - 현재 문서 닫기
:q! - 저장하지 않고 닫기
:wq - 저장하고 닫기
:숫자 - 지정한 라인넘버로 이동

:new - 가로로 분할된 창 열기
:vs - 세로로 분할된 창 열기
Ctrl + w - 분할창 간에 이동하기
:tabnew - 새로운 탭 열기
:gt - 다음 탭으로 이동하기
:gT - 이전 탭으로 이동하기
:e ./ - 현재 탭에 오픈할 파일 탐색하기( ./ 는 현재위치에서 탐색 시작)
:colorscheme 스키마명 - VIM의 칼라스키마를 변경함(blue, desert, evening 등.. 스키마명에서 탭누르면 자동완성됨)

zc - 코드 접기(fold)
zo - 접힌 코드 펼치기
zd - fold 지우기
zR - 접힌 코드 모두 펼치기
zM - 코드 모두 접기
zD - 모든 fold 지우기

:buffers - 현재 Vim에서 여러 파일을 열었을때 버퍼에 있는 목록 확인
:buffer 숫자 - 버퍼 목록에 나온 숫자를 입력하면 해당 파일을 오픈함 ( :buffer 대신 :b 도 가능)
:bnext - 버퍼에 있는 다음 파일로 이동 ( :bn 도 가능)
:bprevious - 버퍼에 있는 이전 파일로 이동 ( :bp 도 가능)
:ball - 버퍼 목록에 있는 파일들이 가로로 분할된 창에 열림


http://json.parser.online.fr/


encoding과 encryption 차이
encoding은 특정 방식으로 데이터를 변환하는 것


직렬화 : 바이트(byte) 형태로 데이터 변환하는 기술

인코딩: 공개적으로 사용 가능한 방법을 통해 데이터를 변환하는 것. 다른 시스템에서의 데이터 유용성을 높이고 저장에 필요한 공간을 줄이려는 의도로 이룰어진다. 예를 들어 문자 'A'는 아스키코드 65번으로 표시된다. 인코딩 된 데이터는 표준방법을 사용하여 쉽게 디코딩할 수 있다.

 

암호화: 데이터를 비밀로 유지하려는 의도로 데이터를 변환하는 것. 암호 알고리즘을 이용해 데이터를 암호화하고 특수 키를 사용하여 암호를 해독한다. 예를 들어 대칭키, 공개키 방식.



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

