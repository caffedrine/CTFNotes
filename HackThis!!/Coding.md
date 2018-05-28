### Coding Level 1
```
var strings = $('textarea').text();
var strArr = strings.split(', ').sort();
var output = strArr.join(', ');
$('textarea[name=answer]').text(output);
```


### Coding Level 2