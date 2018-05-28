### Javascript Level 1
```
$(function() {
    $('.level-form').submit(function(e) {
        e.preventDefault();
        if (document.getElementById('pass').value == correct) {
            document.location = '?pass=' + correct;
        } else {
            alert('Incorrect password')
        }
    })
})

var correct = 'jrules'
```
```
jrules
```


### Javascript Level 2
```
$(function() {
    $('.level-form').submit(function(e) {
        e.preventDefault();
        if ($('.level-form #pass')[0].value.length == length) {
            document.location = "2?x=" + length;
        } else {
            alert('Incorrect Password');
        }
    });
});
// length = 9
```
```
123456789
```


### Javascript Level 3
```
var thecode = 'code123';
$(function() {
    $('.level-form').submit(function(e) {
        e.preventDefault();
        if ($('.level-form #pass')[0].value == thecode) {
            document.location = "?pass=" + thecode;
        } else {
            alert('Incorrect Password');
        }
    });
});

// but thecode = "getinthere"
```
```
getinthere
```


### Javascript Level 4
view-source:https://www.hackthis.co.uk/levels/javascript/4

```
smellthecheese
```


### Javascript Level 5
https://www.hackthis.co.uk/files/js/min/extra_48d468a93b.js?1510507123
```
a = window.location.host + "";
b = a.length;
c = 4 + ((5 * 10) * 2);
d = String.fromCharCode(c, -(41 - Math.floor(1806 / 13)), Math.sqrt(b - 2) * 29, (b * 8) - 29);
```
```
hats
```