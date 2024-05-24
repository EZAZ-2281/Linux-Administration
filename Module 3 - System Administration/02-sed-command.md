# sed command

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd folder-one
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cat character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
cumilla burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed 's/cumilla/homwtown/g' character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
homwtown burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cat character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
cumilla burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed -i 's/cumilla/hometown/g' character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cat character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
hometown burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed 's/ahmed//g' character
rahim
karim
abdul
savar
golam kibria
tausif
bishal
dhaka bangladesh
hometown burichang
savar daffordil
karim
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cat character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
hometown burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed 's/ahmed/d' character
sed: -e expression #1, char 9: unterminated `s' command
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed '/ahmed/d' character
rahim
karim
abdul
savar
golam kibria
dhaka bangladesh
hometown burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ vi character
Then press i to move insert mode then give some space then esc > shift zz.
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cat character
rahim

karim
abdul

savar

golam kibria
tausif ahmed
bishal ahmed

dhaka bangladesh
hometown burichang

savar daffordil
karim
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed '/^$/d' character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
hometown burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed -i '/^$/d' character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cat character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
hometown burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed '/1d/' character
sed: -e expression #1, char 4: missing command
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed '1d' character
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
hometown burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed '1,2d' character
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
hometown burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ vi character
Then press i to move insert mode then give some tab > esc > shift zz. 
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cat character
rahim
karim
abdul
savar
golam   kibria
tausif  ahmed
bishal  ahmed
dhaka bangladesh
hometown burichang
savar daffordil
karim
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed 's/\t/ /g' character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
hometown burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cat character
rahim
karim
abdul
savar
golam   kibria
tausif  ahmed
bishal  ahmed
dhaka bangladesh
hometown burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed -i 's/\t/ /g' character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cat character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
hometown burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed -n 5,7p character
golam kibria
tausif ahmed
bishal ahmed
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed 5,7d character
rahim
karim
abdul
savar
dhaka bangladesh
hometown burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed g character











ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed G character
rahim

karim

abdul

savar

golam kibria

tausif ahmed

bishal ahmed

dhaka bangladesh

hometown burichang

savar daffordil

karim

```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cat character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
hometown burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed 's/ahmed/s/g' character
rahim
karim
abdul
savar
golam kibria
tausif s
bishal s
dhaka bangladesh
hometown burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sed '7!s/ahmed/s/g' character
rahim
karim
abdul
savar
golam kibria
tausif s
bishal ahmed
dhaka bangladesh
hometown burichang
savar daffordil
karim
ikibria@DESKTOP-OPJUB1R:~/folder-one$ exit
```
**[The End]**