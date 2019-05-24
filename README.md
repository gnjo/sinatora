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

# memory
```
$0...$9
```

# multi to single
```
--- param 0 is multi
set
$0 aaaa
---
mov
$0===1 #0
$0===2 #1
$0===3 #2
---
```

# cmd map
```
let cmdMap={}
cmdMap['lib']={before:(o,lines)=>{}, now:(o,line)=>{}, after:(o,line)=>{} }
...
```
```
let str='...'
,lines =m2s(str) //multi to single
Object.keys(cmdMap).filter(d=>cmdMap[d].before).map(d=>cmdMap[d].call(this,o,lines)
;
let walk=0
;
for(;walk<lines.length;walk++){
 let code=lines[walk]
 let cmd=code.split(' ').slice(0,1).pop()
 iscmd(cmd)? cmdMap[cmd].call(this,o,code):error(walk+':'+code)
}

```
# info
```
sinatra(...).compiler(...,info)

info.iserror=false
info.message=013| lib https://gnjo.github.io/use.js
info.walk=13
info.output=void 0
info.cmd='lib'
info.param=['https://gnjo.github.io/use.js']
info.code='lib https://gnjo.github.io/use.js'
```


