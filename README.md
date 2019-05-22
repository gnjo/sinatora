# sinatora
script lang

# target
```
- simple
- 3word command
```

# target code
```
lib fn https://gnjo.github.io/function.js 
set x fn.load('z.jpg')
set st1 'hi,there'
---
lbl #back
put x
mes textdemo${st1}
key flg1
mov flg1===a #xyz
mov flg1===b #zzz
mov flg1===* #back
---
lbl #xyz

mes ${flg1}
wai 1000
mov https://gnjo.github.io/xxxx.sin
```
