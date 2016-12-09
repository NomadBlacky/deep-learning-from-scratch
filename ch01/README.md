# Python 入門

## クラス

```python
class Hoge:
	def __init__(self, arg1, arg2):  # コンストラクタ
		# Initialize
	def method1(self, arg1):  # メソッド
		# Do anything
```

+ Pythonではメソッドの第一引数に自分自身を表す self を明示的に書くのが特徴。

## ライブラリのインポート

```python
import numpy as np
```

+ NumPy ライブラリを読み込んでいる。
+ 以降は np としてメソッドを参照できる。

## NumPy の算術演算

```python
import numpy as np
x = np.array([1.0, 2.0, 3.0])
y = np.array([2.0, 4.0, 6.0])

x + y  # array([ 3.,  6.,  9.])
x - y  # array([-1., -2., -3.])
x * y  # array([  2.,   8.,  18.])
x / y  # array([ 0.5,  0.5,  0.5])

# ブロードキャスト
x + z  # array([ 3.,  4.,  5.])
x - z  # array([-1.,  0.,  1.])
x * z  # array([ 2.,  4.,  6.])
x / z  # array([ 0.5,  1. ,  1.5])
```

+ 各要素ごとに四則演算を行っている。
+ 要素数が同じということに注意する。
+ 「要素ごと」という言葉は英語で element-wise という。
	+ 「要素ごとの積」 ... element-wise product
+ 単一の値(スカラ値)とも演算が可能で、これを「ブロードキャスト」という。

