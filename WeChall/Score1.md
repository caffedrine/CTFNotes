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


### Encodings: URL (Training, Encoding)
%59%69%70%70%65%68%21%20%59%6F%75%72%20%55%52%4C%20%69%73%20%63%68%61%6C%6C%65%6E%67%65%2F%74%72%61%69%6E%69%6E%67%2F%65%6E%63%6F%64%69%6E%67%73%2F%75%72%6C%2F%73%61%77%5F%6C%6F%74%69%6F%6E%2E%70%68%70%3F%70%3D%6E%64%62%72%6D%70%65%65%64%67%6F%63%26%63%69%64%3D%35%32%23%70%61%73%73%77%6F%72%64%3D%66%69%62%72%65%5F%6F%70%74%69%63%73%20%56%65%72%79%20%77%65%6C%6C%20%64%6F%6E%65%21
```js
var input = '%59%69%70%70%65%68%21%20%59%6F%75%72%20%55%52%4C%20%69%73%20%63%68%61%6C%6C%65%6E%67%65%2F%74%72%61%69%6E%69%6E%67%2F%65%6E%63%6F%64%69%6E%67%73%2F%75%72%6C%2F%73%61%77%5F%6C%6F%74%69%6F%6E%2E%70%68%70%3F%70%3D%6E%64%62%72%6D%70%65%65%64%67%6F%63%26%63%69%64%3D%35%32%23%70%61%73%73%77%6F%72%64%3D%66%69%62%72%65%5F%6F%70%74%69%63%73%20%56%65%72%79%20%77%65%6C%6C%20%64%6F%6E%65%21';
var output = decodeURIComponent(input);
"Yippeh! Your URL is challenge/training/encodings/url/saw_lotion.php?p=ndbrmpeedgoc&cid=52#password=fibre_optics Very well done!"
```
```
http://www.wechall.net/challenge/training/encodings/url/saw_lotion.php?p=ndbrmpeedgoc&cid=52#password=fibre_optics
```