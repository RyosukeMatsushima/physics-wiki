# 運動量と角運動量

運動量と角運動量は、力学における最も基本的な保存量である。
本稿では、それぞれの定義・単位・次元を整理し、運動エネルギーとの関係を導く。

---

## 1. 運動量（Linear Momentum）

### 定義

質量 $m$、速度 $\boldsymbol{v}$ を持つ質点の**運動量** $\boldsymbol{p}$ は

$$
\boldsymbol{p} = m\boldsymbol{v}
$$

と定義される。ニュートンの第二法則は運動量を用いて

$$
\boldsymbol{F} = \frac{d\boldsymbol{p}}{dt}
$$

と書ける。外力が働かない系では $\boldsymbol{p}$ は保存される（運動量保存則）。

### 単位と次元

| 量 | 記号 | SI 単位 | 次元 |
|---|---|---|---|
| 質量 | $m$ | kg | $[\mathrm{M}]$ |
| 速度 | $v$ | m/s | $[\mathrm{L}\,\mathrm{T}^{-1}]$ |
| 運動量 | $p$ | kg·m/s | $[\mathrm{M}\,\mathrm{L}\,\mathrm{T}^{-1}]$ |

単位の等価表現：

$$
\boxed{[\boldsymbol{p}] = \mathrm{kg \cdot m/s} = \mathrm{N \cdot s}}
$$

$\mathrm{N \cdot s}$（ニュートン秒）は力積（impulse）の単位と一致する。

---

## 2. 角運動量（Angular Momentum）

### 定義

原点から位置 $\boldsymbol{r}$ にある質点の**角運動量** $\boldsymbol{L}$ は

$$
\boldsymbol{L} = \boldsymbol{r} \times \boldsymbol{p} = \boldsymbol{r} \times (m\boldsymbol{v})
$$

と定義される。角運動量の時間変化はトルク $\boldsymbol{N}$ と等しい。

$$
\boldsymbol{N} = \frac{d\boldsymbol{L}}{dt}
$$

外トルクが働かない系では $\boldsymbol{L}$ は保存される（角運動量保存則）。

剛体の回転に対しては、慣性モーメント $I$ と角速度 $\boldsymbol{\omega}$ を用いて

$$
L = I\omega
$$

と書ける（主軸成分については $L_i = I_i \omega_i$）。

### 単位と次元

| 量 | 記号 | SI 単位 | 次元 |
|---|---|---|---|
| 位置 | $r$ | m | $[\mathrm{L}]$ |
| 運動量 | $p$ | kg·m/s | $[\mathrm{M}\,\mathrm{L}\,\mathrm{T}^{-1}]$ |
| 角運動量 | $L$ | kg·m²/s | $[\mathrm{M}\,\mathrm{L}^{2}\,\mathrm{T}^{-1}]$ |

単位の等価表現：

$$
\boxed{[\boldsymbol{L}] = \mathrm{kg \cdot m^2/s} = \mathrm{J \cdot s} = \mathrm{N \cdot m \cdot s}}
$$

$\mathrm{J \cdot s}$（ジュール秒）は**作用（action）**の単位と同じであり、プランク定数 $\hbar$ の単位でもある。

### 運動量との次元比較

$$
[\boldsymbol{L}] = [\boldsymbol{r}][\boldsymbol{p}] = \mathrm{m} \cdot \mathrm{kg \cdot m/s} = \mathrm{kg \cdot m^2/s}
$$

角運動量の単位は運動量の単位に「長さ（m）」を掛けたものになっている。これは $\boldsymbol{L} = \boldsymbol{r} \times \boldsymbol{p}$ という定義を反映している。

---

## 3. 運動エネルギーとの関係

### 並進運動エネルギーと運動量

質量 $m$ の質点の並進運動エネルギー $K$ は

$$
K = \frac{1}{2}mv^2 = \frac{p^2}{2m}
$$

と書ける。この式から、運動量 $p$ を固定したとき質量が大きいほどエネルギーは小さく、
エネルギー $K$ を固定したとき運動量は質量の平方根に比例することがわかる。

$$
\boxed{K = \frac{p^2}{2m}, \qquad p = \sqrt{2mK}}
$$

### 回転運動エネルギーと角運動量

慣性モーメント $I$ の剛体の回転運動エネルギー $T$ は

$$
T = \frac{1}{2}I\omega^2 = \frac{L^2}{2I}
$$

と書ける。並進の場合と対応して、$m \to I$、$p \to L$ と置き換えた形になっている。

$$
\boxed{T = \frac{L^2}{2I}, \qquad L = \sqrt{2IT}}
$$

### 並進と回転の対応関係まとめ

| 並進運動 | 回転運動 |
|---|---|
| 質量 $m$ | 慣性モーメント $I$ |
| 速度 $v$ | 角速度 $\omega$ |
| 運動量 $p = mv$ | 角運動量 $L = I\omega$ |
| 運動エネルギー $K = \dfrac{p^2}{2m}$ | 回転エネルギー $T = \dfrac{L^2}{2I}$ |
| 力 $F = \dot{p}$ | トルク $N = \dot{L}$ |
| 単位：kg·m/s | 単位：kg·m²/s |

---

## 4. 作用・プランク定数との関係

角運動量の単位 $\mathrm{J \cdot s}$ は**作用（action）**の次元と一致する。
ラグランジアン $\mathcal{L}$ を時間で積分した量

$$
S = \int \mathcal{L}\, dt
$$

は作用と呼ばれ、$[\mathrm{J \cdot s}] = [\mathrm{kg \cdot m^2/s}]$ の次元を持つ。

プランク定数 $h$ および換算プランク定数 $\hbar$ も同じ次元を持つ。

$$
h \approx 6.626 \times 10^{-34}\ \mathrm{J \cdot s}, \qquad \hbar = \frac{h}{2\pi} \approx 1.055 \times 10^{-34}\ \mathrm{J \cdot s}
$$

量子力学では角運動量は $\hbar$ の整数倍（または半整数倍）に量子化される。

---

## 参考文献

- 原島鮮, 『力学』, 裳華房 (1981)
- H. Goldstein, C. Poole, J. Safko, *Classical Mechanics*, 3rd ed., Addison-Wesley (2002)
- 小出昭一郎, 『量子力学（I）』, 裳華房 (1990)
