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
```


### Towers of Hanoi (Java, Cracking)

```
http://www.wechall.net/challenge/Z/hanoi/index.php?solution=feb3a1f6e5e259f381f42a4e72aceaea204403fab7eec9a2d3d0bcff076a647be88f6f6caeeb1b6295aabba9807f1a2260b466f9f0512498fb50300703eb2552
```


### Enlightment (Encoding)

