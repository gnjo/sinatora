# sinatra
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

# first code
lib value url

def cmd script
```
def set (a,b)=>{ sinatora.data[a]=void 0; sinatora.data[a]=b }
def mov (a,b)=>{ }
def key (a,b)=>{ sinatora.frame.oninput=()=>{ ... } }
def clr ()=>{ }
```

# choice
```
mes
1:xyz
2:ddd
3:ppp
4:qqq
---
key flg
mov 
flg===1 #go1
flg===2 #go2
flg===3 #go3
flg===4 #go4
flg===flg #other
---
```

# error message
stock the buffer
```
010| flg===1 #go1
011| flg=2 #go2
012| flg===3 #go3
```

# compile
```js
sinatra('#app')
 .compile(str,(e)=>{ console.log(e.error,e.message,e.calc) }) 
```







