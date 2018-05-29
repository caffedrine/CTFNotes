### Coding Level 1
```
var strings = $('textarea').text();
var strArr = strings.split(', ').sort();
var output = strArr.join(', ');
$('textarea[name=answer]').text(output);
```


### Coding Level 2
```
var strings = $('textarea').text();
var strArr = strings.split(',');
var output = '';
var i;
for (i=0; i<strArr.length; i++) {
    if (" " == strArr[i]) {
        output += " ";
    } else {
        output += String.fromCharCode(158 - parseInt(strArr[i]));
    }
}
$('textarea[name=answer]').text(output);
```