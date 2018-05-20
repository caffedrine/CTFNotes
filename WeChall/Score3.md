### Connect the Dots (Stegano)
The Braille Alphabet

thesolutionisskunk
```
skunk
```


### hi (Math)
(17591026060782 + 2) * 17591026060781 / 2
 
```
154722098935564539692256152
```


### Stegano Woman (Stegano)
In stegano_woman.zip -> keyword: "Stegano"

Appearing a lot of 0x09(tab) and 0x20(space)

Transcoding to 1 and 0

```python
with open("stegano_woman.zip", "rb") as f:
    data = f.read()
index = data.find('Stegano')

binText = ''
for i in range(index, len(data)):
    if "\x20" == data[i]:
        binText += '1'
    elif "\x09" == data[i]:
        binText += '0'

ans = ''
for j in range(len(binText) / 8):
    ans += chr(int(binText[j*8:j*8+8], 2))

print ans
```

The solution is "dangerous life".

```
dangerous life
```


### Flow Over Astronomy (Coding, Math)
```py
import requests

COOKIE = {'WC': '*******'}
BASE10 = '0123456789'


def convert(number, fromBase, toBase):
    value = 0
    for digit in str(number):
        value = value * len(fromBase) + fromBase.index(digit)

    output = ""
    while value > 0:
        digit = value % len(toBase)
        output = toBase[digit] + output
        value /= len(toBase)

    return output


def parseInput(keyword, data):
    start = data.index(keyword + ': ')
    end = data.find('<br/>', start)
    return data[start + len(keyword) + 2 : end]


def parseEquation(data):
    start = data.index('Equation')
    realStart = data.find('<div class="box_c">', start)
    end = data.find('<br/></div>', realStart)
    equation = data[(realStart + len('<div class="box_c">')) : end]
    return equation.replace('<br/>', '')


r = requests.get('http://www.wechall.net/challenge/anto/FlowOverAstronomy/index.php', cookies=COOKIE)
data = r.text

charset = parseInput('Charset', data)
inputBase = parseInput('Input Base', data)
solutionBase = parseInput('Solution Base', data)
equation = parseEquation(data)

print 'Charset: ' + charset
print len(charset)
print 'Input Base: ', inputBase
print 'Solution Base: ', solutionBase
print 'Equation:' + equation

inputMap = charset[0 : int(inputBase)]
outputMap = charset[0 : int(solutionBase)]

equationList = equation.split(' ')
equationBase10List = []

for i in equationList:
    if i == '*' or i == '+':
        equationBase10List.append(i)
    else:
        digitBase10 = convert(i, inputMap, BASE10)
        equationBase10List.append(digitBase10)

equationBase10 = " ".join(equationBase10List)
anwserBase10 = eval(equationBase10)
answer = convert(anwserBase10, BASE10, outputMap)
postData = {'answer': answer, 'action': 'Submit'}
r = requests.post('http://www.wechall.net/challenge/anto/FlowOverAstronomy/index.php', cookies=COOKIE, data=postData)

print answer
```


### Towers of Hanoi (Java, Cracking)
```py
#!/usr/bin/env python
from hashlib import sha512

solution = ''


def hanoi(n, A, C, B):
    global solution
    if n > 0:
        hanoi(n - 1, A, B, C)
        map = {
            'ab':'we',
            'ac':'ch',
            'bc':'al',
            'ba':'lr',
            'ca':'ul',
            'cb':'z!'
        }
        solution += map[A + C]
        hanoi(n - 1, B, C, A)


hanoi(10, "a", "c", "b")
print sha512(solution).hexdigest()
```

```
http://www.wechall.net/challenge/Z/hanoi/index.php?solution=feb3a1f6e5e259f381f42a4e72aceaea204403fab7eec9a2d3d0bcff076a647be88f6f6caeeb1b6295aabba9807f1a2260b466f9f0512498fb50300703eb2552
```


### Enlightment (Encoding)
http://www.cnblogs.com/zhurb/p/5856678.html
```
Gimme_Da_Light
```

### Simply Red (Stegano, Image)
"No sacrifice is too great in the service of freedom." - Optimus Prime

Prime

```python
from PIL import Image

def isPrime(n):
    for i in range(3, n):
        if n % i == 0:
            return False
    return True

im = Image.open('op.png').convert('RGB')
w, h = im.size

data = []
for y in range(w):
    for x in range(h):
        r, g, b = im.getpixel((x, y))

        if isPrime(r):
            data.append((r, 0, 0))
        else:
            data.append((0, 0, 0))

out = Image.new("RGB", im.size)
out.putdata(data)
out.save('out.png')
```
```
PrimalOffset
```


### htmlspecialchars (Exploit, PHP, XSS)
add "ENT_QUOTES" parameter for htmlspecialchars()

```
echo "<a href='http://".htmlspecialchars(Common::getPost('input'), ENT_QUOTES)."'>Exploit Me</a>";
```


### Impossible n'est pas français (Exploit)
The keywords are Exploit and Impossible, so you need to try to do something different

```py
import requests

COOKIE = {'WC': '********'}


def getCsrf(data):
    start = data.index('gwf3_csrf') + len('gwf3_csrf" value="')
    end = data.find('" /></td>', start)
    return data[start: end]


r = requests.get('http://www.wechall.net/challenge/impossible/index.php', cookies=COOKIE)
params = {'request': 'new_number'}
r2 = requests.get('http://www.wechall.net/challenge/impossible/index.php', cookies=COOKIE, params=params)
data = r.text

params = {'solution': 123, 'cmd': 'Send', 'gwf3_csrf': getCsrf(data)}
r = requests.post('http://www.wechall.net/challenge/impossible/index.php', cookies=COOKIE, params=params)
data = r.text

start = data.index('Correct would have been') + len('Correct would have been &quot;')
end = data.find('&quot;', start)
answer = data[start:end]

params = {'solution': answer, 'cmd': 'Send', 'gwf3_csrf': getCsrf(data)}
r = requests.post('http://www.wechall.net/challenge/impossible/index.php', cookies=COOKIE, params=params)

print answer
print r.text
```


### PHP 0815 (Exploit, PHP)
```
-0
```


### Guesswork (Exploit)
```
wechallbot
```


### No Escape (Exploit, PHP, MySQL)
Source Code: Line 72

Try $who = "bill`= 111,`george`= `george"

```
http://www.wechall.net/challenge/no_escape/index.php?vote_for=bill%60%3D%20111%2C%60george%60%3D%20%60george
```


### Training: Crypto - Substitution II (Crypto, Training)
keyword: congratulations!

Congratulations. This one was harderq but you got it. very well done fellow hacker. The problem with this cipher is that the key is pretty long. I will come up with a better encryption sheme any soon. Your solution is: ************


```
hmbgfpiiglhm
```


### Training: WWW-Rewrites (HTTP, Training)
```python
from BaseHTTPServer import BaseHTTPRequestHandler
import re


class GetHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        try:
            m = re.match('/Ranger/(\d+)_mul_(\d+)\.html', self.path)
        except:
            m = None

        message = ''
        if m:
            n1 = m.group(1)
            n2 = m.group(2)
            message = int(n1) * int(n2)

        self.send_response(200)
        self.end_headers()
        self.wfile.write(message)


if __name__ == '__main__':
    from BaseHTTPServer import HTTPServer
    server = HTTPServer(('localhost', 8080), GetHandler)
    print 'Starting server at http://localhost:8080'
    server.serve_forever()
```


### Stegano Attachment (Stegano, Image, Training)
attachment.php = jpg + zip

jpg = ffd8 ... ffd9

zip = PK0304 ...

dd if=attachment.php of=solution.zip skip=20230 bs=1 count=136

```
AABSHFCLBRHNPK
```


### Zebra (Training, Encoding, Stegano)
painter first

https://online-barcode-reader.inliteresearch.com/

The answer is saFFari

```
saFFari
```


### Pimitive Encryption (Crypto, Logic)
ZIP Archive (MAGIC DWORD 0x504B0304)

pimitive.zip: 0x63653230

=> 0x63653230 xor 0x504B0304 = 0x332e3134 ascii(3.14)

pi file: http://pi2e.ch/blog/wp-content/uploads/2017/03/pi_dec_1m.txt

unzip: netforce33.bmp

```
Botterbloom
```


### Vermeer (Logic, Image, Stegano)
charset.replace(/[ox\d]/g,'')

Sadly, this is nt the message yu are lking fr :( Try further!

They are coordinate ! 25x10 => (25, 10)


```
HACKING
```


### Stop us (Exploit, PHP)
Before reducing your balance, close the connection...


### PHP 0818 (Exploit, PHP)
POST a number, each digit is not between 1 and 9, and it also equal("==") "3735929054"

```
0xdeadc0de
```


### Are you serial (PHP)
insecure.inc.php => spl_autoload_register('my_autoloader');

code.php => $user = unserialize(Common::getCookie('serial_user', ''))


```curl
curl -b cookie.file -c cookie.file -X POST -d "username=Ranger" -d "password=********" -d "login=Login" https://www.wechall.net/login

curl -b cookie.file -c cookie.file --cookie "serial_user=O:15:\"SERIAL_Solution\":0:{}" -X POST http://www.wechall.net/challenge/are_you_serial/code.php
```


### SSH... Z is sleeping (Linux, Exploit, Warchall)
/home/level/8/backups/authorized_keys.backup

https://plus.google.com/+RicterZheng/posts/3pR5MEsD1Vi

ssh-keygen -l -E md5 -f key

2048 MD5:2b:cd:07:a7:01:e9:4a:04:74:d7:7e:e4:d6:d0:f8:06 no comment (RSA)

https://github.com/g0tmi1k/debian-ssh/blob/master/common_keys/debian_ssh_dsa_1024_x86.tar.bz2

ssh -i 2bcd07a701e94a0474d77ee4d6d0f806-23669 -p 19198 level8@warchall.net

Your solution to level 8 is: PrivateKeysAreGold

```
PrivateKeysAreGold
```


### Chessy Hawks (Crypto, Logic)
chess's position can be expressed as hex

yellow's op is sub, blue's op is add

|color|Y|Y|Y|Y|Y|Y|B|Y|Y|B|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|pos|8a|8e|7c|6c|6d|6f|5b|4a|3e|2d|
|val|24|3C|49|39|1D|8|13|19|B|2D|
|hex|66|52|33|33|50|77|6E|31|33|5A|
|ans|f|R|3|3|P|w|n|1|3|Z|

```
fR33Pwn13Z
```


### eXtract Me (Encoding, Stegano)
zip password: L0LYouThInkiTSh0uldB3SoEasY?

```
598afa8b4d6c470b0e64f2dc9bde2694
```


### PHP 0819 (PHP)
```
http://www.wechall.net/challenge/space/php0819/index.php?eval=<<<s%0a1337%0as;%0a
```


### Illuminati (Stegano)
http://www.wechall.net/challenge/illuminati/sometimes.ttf

Use fontForge open it

```
ILLUMOSATMO
```

### Britcoin (Coding)
5DAEE0CF0AF9ADCDB38F3B8F10F93E0486E4C3CB1596D255BA9A88E1AE5634436F052B276143B303E85C71342B76461448C154220CF2078A26DD751F9232A80D

