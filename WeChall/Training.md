### Get Sourced (Training)
On browser click right mouse -> View page source
<!-- You are looking for this password: html_sourcecode -->  
```
html_sourcecode
```


### Stegano I (Training, Stegano)
http://www.wechall.net/challenge/training/stegano1/stegano1.bmp
hex it
Look what the hex-edit revealed: passwd:steganoI
```
steganoI
```


### Crypto - Caesar I
IWT FJXRZ QGDLC UDM YJBEH DKTG IWT APON SDV DU RPTHPG PCS NDJG JCXFJT HDAJIXDC XH WGBXSSVEABRU

https://cryptii.com/caesar-cipher

Shiff 11

the quick brown fox jumps over the lazy dog of caesar and your unique solution is hrmiddgplmcf
```
hrmiddgplmcf
```


### WWW-Robots (HTTP, Training)
see http://www.wechall.net/robots.txt
```
http://www.wechall.net/challenge/training/www/robots/T0PS3CR3T/
```


### ASCII (Encoding)
84, 104, 101, 32, 115, 111, 108, 117, 116, 105, 111, 110, 32, 105, 115, 58, 32, 105, 105, 108, 112, 104, 99, 114, 98, 101, 108, 112, 103
```js
var input = '84, 104, 101, 32, 115, 111, 108, 117, 116, 105, 111, 110, 32, 105, 115, 58, 32, 105, 105, 108, 112, 104, 99, 114, 98, 101, 108, 112, 103';
var output = input.split(',').map(function(int){
    return String.fromCharCode(int);
}).join('');
"The solution is: iilphcrbelpg"
```
```
iilphcrbelpg
```


### URL (Training, Encoding)
%59%69%70%70%65%68%21%20%59%6F%75%72%20%55%52%4C%20%69%73%20%63%68%61%6C%6C%65%6E%67%65%2F%74%72%61%69%6E%69%6E%67%2F%65%6E%63%6F%64%69%6E%67%73%2F%75%72%6C%2F%73%61%77%5F%6C%6F%74%69%6F%6E%2E%70%68%70%3F%70%3D%6E%64%62%72%6D%70%65%65%64%67%6F%63%26%63%69%64%3D%35%32%23%70%61%73%73%77%6F%72%64%3D%66%69%62%72%65%5F%6F%70%74%69%63%73%20%56%65%72%79%20%77%65%6C%6C%20%64%6F%6E%65%21
```js
var input = '%59%69%70%70%65%68%21%20%59%6F%75%72%20%55%52%4C%20%69%73%20%63%68%61%6C%6C%65%6E%67%65%2F%74%72%61%69%6E%69%6E%67%2F%65%6E%63%6F%64%69%6E%67%73%2F%75%72%6C%2F%73%61%77%5F%6C%6F%74%69%6F%6E%2E%70%68%70%3F%70%3D%6E%64%62%72%6D%70%65%65%64%67%6F%63%26%63%69%64%3D%35%32%23%70%61%73%73%77%6F%72%64%3D%66%69%62%72%65%5F%6F%70%74%69%63%73%20%56%65%72%79%20%77%65%6C%6C%20%64%6F%6E%65%21';
var output = decodeURIComponent(input);
"Yippeh! Your URL is challenge/training/encodings/url/saw_lotion.php?p=ndbrmpeedgoc&cid=52#password=fibre_optics Very well done!"
```
```
http://www.wechall.net/challenge/training/encodings/url/saw_lotion.php?p=ndbrmpeedgoc&cid=52#password=fibre_optics
```


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

hexCipher = """ #random
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