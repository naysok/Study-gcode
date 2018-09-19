# Study-gcode  

### index  

- 60x60.gcode // example gcode  

- 5 // rhino5 ghx
  -

---  

---  



### gcode syntax  



G0 Xnn Ynn Znn Enn Fnn Snn : 高速直線移動  
G1 Xnn Ynn Znn Enn Fnn Snn : 直線移動  


Xnn X軸上における移動先の位置  
Ynn Y軸上における移動先の位置  
Znn Z軸上における移動先の位置  
Enn 開始地点と終了地点の間で押し出されるフィラメントの量  

```gcode
; ex
G1 X1.25 Y2.5 Z3.0

```





G92: 位置を指定する(Set Position)

```gcode
G92 E0
```



---


### Ref.  

G-code(RepRap community Wiki) // 本家（英語）  
[https://reprap.org/wiki/G-code](https://reprap.org/wiki/G-code)  

G-code(RepRap community Wiki) // 日本語版   
[https://reprap.org/wiki/G-code/ja](https://reprap.org/wiki/G-code/ja)
