# Study-gcode  

### index  

- 60x60.gcode // example gcode  

- 5 // rhino5 ghx  
  - grid-ver1.ghx // 中心点からの距離に応じて変化量の変わるグリッド、線形での移動なのであまり可愛くない  
  - ~~Write-gcode-ver1.ghx // 普通の四角形、G93 E0 の部分 Python 側で反映なかったXXX~~  
  - Write-gcode-ver2.ghx // 普通の四角形、E0 修正  
  - Write-gcode-ver3.ghx // ずらした四角形  

  // cf.  
  // アトラクタで膨らむグリッドを使って、真ん中がやわらかい感じ？  
  ![photo](grid.png)  
  // GH: GRID SPREADING  
  [http://formularch.blogspot.com/2012/06/gh-grid-spreading.html](http://formularch.blogspot.com/2012/06/gh-grid-spreading.html)  



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


### gh-PointList to gcode  

Write-gcode-ver2.ghx までは、2次元パスに、ループ処理でZ座標を足しているんですけど、途中でカタチを変えてくのとかだと、2次元パスが単一ではないので、この方法は変えたほうがいい。  

現状（上の状態から）、3次元に配列したパスから gcode に変換、に設計し直す  
これからはパスの方で3次元情報も与えて（2次元のパスを）書く方法に。

造形物の可視化もできるので一石二鳥  




---


### Ref.  

G-code(RepRap community Wiki) // 本家（英語）  
[https://reprap.org/wiki/G-code](https://reprap.org/wiki/G-code)  

G-code(RepRap community Wiki) // 日本語版   
[https://reprap.org/wiki/G-code/ja](https://reprap.org/wiki/G-code/ja)
