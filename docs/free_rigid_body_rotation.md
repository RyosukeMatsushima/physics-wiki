# 自由剛体の回転運動

自由剛体（外力のかからない剛体）の回転は、オイラー方程式と保存則から完全に記述できる。
本稿では、オイラー方程式の導出から始め、エネルギー楕円体・角運動量球による幾何的解釈、
主軸まわりの安定性、対称剛体の歳差運動、そしてポアンソーの定理までを体系的に解説する。

---

## 1. オイラー方程式の導出

### 慣性系と剛体系の時間微分の関係

慣性系（lab frame）で観測したベクトル $\boldsymbol{A}$ の時間微分と、
剛体に固定された座標系（body frame）での時間微分の間には次の関係がある。

$$
\left(\frac{d\boldsymbol{A}}{dt}\right)_{\!\text{lab}}
= \left(\frac{d\boldsymbol{A}}{dt}\right)_{\!\text{body}} + \boldsymbol{\omega} \times \boldsymbol{A}
$$

ここで $\boldsymbol{\omega}$ は剛体の角速度ベクトルである。

### 角運動方程式

角運動量 $\boldsymbol{L}$ に対して、慣性系でのニュートンの第二法則は

$$
\left(\frac{d\boldsymbol{L}}{dt}\right)_{\!\text{lab}} = \boldsymbol{N}
$$

自由剛体（$\boldsymbol{N} = \boldsymbol{0}$）では、これに上の変換則を適用すると

$$
\left(\frac{d\boldsymbol{L}}{dt}\right)_{\!\text{body}} + \boldsymbol{\omega} \times \boldsymbol{L} = \boldsymbol{0}
$$

### 主軸座標での展開

慣性主軸を座標軸にとり、主慣性モーメントを $I_1, I_2, I_3$、
対応する角速度成分を $\omega_1, \omega_2, \omega_3$ とすれば $L_i = I_i \omega_i$（$i=1,2,3$）。
これを成分ごとに書き下すと**オイラー方程式**が得られる。

$$
\boxed{
\begin{aligned}
I_1 \dot{\omega}_1 &= (I_2 - I_3)\,\omega_2\,\omega_3 \\
I_2 \dot{\omega}_2 &= (I_3 - I_1)\,\omega_3\,\omega_1 \\
I_3 \dot{\omega}_3 &= (I_1 - I_2)\,\omega_1\,\omega_2
\end{aligned}
}
$$

---

## 2. 保存量と不変量

自由剛体では外力も外トルクもないため、以下の二つの量が時間的に不変である。

**運動エネルギー**

$$
T = \frac{1}{2}\sum_{i=1}^{3} I_i \omega_i^2 = \text{const}
$$

**角運動量の大きさの二乗**

$$
L^2 = |\boldsymbol{L}|^2 = \sum_{i=1}^{3} (I_i \omega_i)^2 = \text{const}
$$

慣性系では $\boldsymbol{L}$ そのもの（方向も含めて）が保存される。

---

## 3. $\omega$ 空間と $L$ 空間

### $\omega$ 空間での幾何的意味

$(\omega_1, \omega_2, \omega_3)$ を座標とする空間では、二つの保存条件は

$$
\frac{\omega_1^2}{2T/I_1} + \frac{\omega_2^2}{2T/I_2} + \frac{\omega_3^2}{2T/I_3} = 1
\quad (\text{エネルギー楕円体})
$$

$$
I_1^2\,\omega_1^2 + I_2^2\,\omega_2^2 + I_3^2\,\omega_3^2 = L^2
\quad (\text{角運動量楕円体})
$$

$\omega$ の先端はこれら二楕円体の交線上を動く。
ただし $\omega$ 空間では、慣性モーメントが軸ごとに異なるため二つとも楕円体となり、
直感的な球との交線という簡明な描像が得られない。

### $L$ 空間への変換

$L_i = I_i\,\omega_i$ によって $\omega$ 空間から $L$ 空間 $(L_1, L_2, L_3)$ へ移る。
保存条件を $L_i$ で書き直すと

$$
\frac{L_1^2}{2T\,I_1} + \frac{L_2^2}{2T\,I_2} + \frac{L_3^2}{2T\,I_3} = 1
\quad (\text{エネルギー楕円体})
$$

$$
L_1^2 + L_2^2 + L_3^2 = L^2
\quad (\text{角運動量球})
$$

$L$ 空間では角運動量保存が**完全な球**として現れる。
これにより「球と楕円体の交線」という非常に見通しのよい幾何的描像が得られる。

---

## 4. $L$ 空間における角運動量球とエネルギー楕円体

$I_1 \geq I_2 \geq I_3 > 0$ と仮定する。

### エネルギー楕円体の半軸

$$
a_i = \sqrt{2T\,I_i}
\quad (i = 1, 2, 3)
\quad \Longrightarrow \quad
a_1 \geq a_2 \geq a_3
$$

### 角運動量球との整合条件

与えられた $T$ と $L$ が運動を許すためには、球がエネルギー楕円体と交わる必要がある。
$L^2$ が取り得る範囲は

$$
2T\,I_3 \leq L^2 \leq 2T\,I_1
$$

- $L^2 = 2T\,I_1$：球がエネルギー楕円体の最長軸端点に接触 → $L_1$ 軸上の点のみ（軸まわりの純粋回転）
- $L^2 = 2T\,I_3$：球がエネルギー楕円体の最短軸端点に接触 → $L_3$ 軸上の点のみ（軸まわりの純粋回転）
- 中間値：球と楕円体が閉じた交線（曲線）で交わる → 一般の歳差運動

$\boldsymbol{L}$ の先端はこの交線上を動き、剛体の運動は幾何学的にこの交線として完全に記述される。

---

## 5. 主慣性軸まわりの回転の安定性

$L$ 空間での「球とエネルギー楕円体の交線」の形状から、
各主軸まわりの回転安定性が幾何的に読み取れる。

### 最大慣性モーメント軸（$I_1$ 軸）まわりの回転

$L \approx \sqrt{2T I_1}$ のとき、球は楕円体の最長軸端点付近で交わる。
交線は端点を囲む小さな閉曲線となる。
→ **安定**（初期の微小ずれは閉じた軌道を描き発散しない）

### 最小慣性モーメント軸（$I_3$ 軸）まわりの回転

$L \approx \sqrt{2T I_3}$ のとき、球は楕円体の最短軸端点付近で交わる。
交線も同様に小さな閉曲線となる。
→ **安定**

### 中間慣性モーメント軸（$I_2$ 軸）まわりの回転

$L = \sqrt{2T I_2}$ のとき、球と楕円体は端点ではなく
「くびれた曲線」で交わる。$L_2$ 軸上の交点付近での交線は
分岐点（鞍部）に対応し、軌道は端点をつなぐセパラトリックス（8 の字曲線）に近い形となる。
→ **不安定**（初期の微小ずれが指数的に増大）

この不安定性は「テニスラケットの定理（Intermediate Axis Theorem）」として知られる。

---

## 6. 対称剛体における歳差運動

### 設定

対称剛体：$I_1 = I_2 \equiv I_\perp \neq I_3$（$3$ 軸が対称軸）

### オイラー方程式の単純化

オイラー方程式に $I_1 = I_2 = I_\perp$ を代入すると

$$
I_\perp \dot{\omega}_1 = (I_\perp - I_3)\,\omega_2\,\omega_3
$$

$$
I_\perp \dot{\omega}_2 = (I_3 - I_\perp)\,\omega_3\,\omega_1
$$

$$
I_3 \dot{\omega}_3 = 0 \quad \Longrightarrow \quad \omega_3 = \text{const}
$$

### 歳差角速度

定数

$$
\Omega \equiv \frac{(I_3 - I_\perp)}{I_\perp}\,\omega_3
$$

を用いると

$$
\dot{\omega}_1 = -\Omega\,\omega_2, \qquad \dot{\omega}_2 = \Omega\,\omega_1
$$

解は

$$
\omega_1(t) = \omega_\perp \cos(\Omega t + \phi_0), \qquad
\omega_2(t) = \omega_\perp \sin(\Omega t + \phi_0)
$$

$\omega_\perp = \sqrt{\omega_1^2 + \omega_2^2} = \text{const}$ は初期条件で決まる定数。

### 幾何的意味

- 剛体系（body frame）では、角速度ベクトル $\boldsymbol{\omega}$ が対称軸（$3$ 軸）まわりを
  角速度 $|\Omega|$ で円錐状に歳差する（**ボディコーン**）。
- 慣性系（space frame）では $\boldsymbol{L}$ が固定されており、
  $\boldsymbol{\omega}$ は $\boldsymbol{L}$ まわりを歳差する（**スペースコーン**）。
- ボディコーンがスペースコーンの上を転がる描像がポアンソーの定理へとつながる。

---

## 7. ポアンソーの定理

### 慣性楕円体の定義

剛体の重心を原点とする剛体系において、**慣性楕円体**（Poinsot の楕円体）を

$$
f(\boldsymbol{r}) \equiv I_1 r_1^2 + I_2 r_2^2 + I_3 r_3^2 = 1
$$

と定義する。この楕円体は剛体に固定されており、剛体と共に回転する。

### 接点の定義

角速度ベクトルを

$$
\boldsymbol{p} = \frac{\boldsymbol{\omega}}{\sqrt{2T}}
$$

と正規化すれば

$$
f(\boldsymbol{p}) = \frac{I_1\omega_1^2 + I_2\omega_2^2 + I_3\omega_3^2}{2T} = \frac{2T}{2T} = 1
$$

よって $\boldsymbol{p}$ は慣性楕円体上の点である。
すなわち**正規化角速度 $\boldsymbol{p}$ が慣性楕円体と $\boldsymbol{\omega}$ 方向で交わる点**が接点となる。

### 不変平面（Invariable Plane）の定義

**不変平面**とは、角運動量ベクトル $\boldsymbol{L}$ に垂直で、かつ原点から距離 $h$ の平面である。
この距離は

$$
h = \boldsymbol{p} \cdot \hat{\boldsymbol{L}} = \frac{\boldsymbol{\omega} \cdot \boldsymbol{L}}{|\boldsymbol{L}|\sqrt{2T}} = \frac{2T}{|\boldsymbol{L}|\sqrt{2T}} = \frac{\sqrt{2T}}{|\boldsymbol{L}|}
$$

$T$ と $|\boldsymbol{L}|$ はともに定数なので $h = \text{const}$。
また $\boldsymbol{L}$ の方向も慣性系で固定されている。
したがって**この平面は慣性系で完全に固定**されている。

### 接点条件（勾配条件）

慣性楕円体 $f(\boldsymbol{r}) = 1$ の点 $\boldsymbol{p}$ における法線方向（勾配）は

$$
\nabla f(\boldsymbol{p}) = 2(I_1 p_1,\, I_2 p_2,\, I_3 p_3) = \frac{2}{\sqrt{2T}}(L_1, L_2, L_3) = \frac{2\boldsymbol{L}}{\sqrt{2T}}
$$

これは $\boldsymbol{L}$ の方向に平行である。すなわち

$$
\boldsymbol{L} \perp \text{（慣性楕円体の接平面（at }\boldsymbol{p}\text{）)}
$$

が成り立つ。接平面の法線が $\boldsymbol{L}$ に平行ということは、
**この接平面が不変平面と一致する**ことを意味する。

まとめると：慣性楕円体は常に点 $\boldsymbol{p}$ で不変平面に接している。

### 「滑りなし転がり」の証明

接点 $\boldsymbol{p}$ の速度を求める。剛体に固定された点 $\boldsymbol{p}$ の慣性系での速度は

$$
\boldsymbol{v}_p = \boldsymbol{\omega} \times \boldsymbol{p} = \boldsymbol{\omega} \times \frac{\boldsymbol{\omega}}{\sqrt{2T}} = \frac{\boldsymbol{\omega} \times \boldsymbol{\omega}}{\sqrt{2T}} = \boldsymbol{0}
$$

接点 $\boldsymbol{p}$ の速度はゼロである。
これは**慣性楕円体が不変平面上を滑りなしで転がる**ことを意味する。

**ポアンソーの定理（まとめ）**：
> 自由剛体の運動は、重心を通る不変平面（角運動量に垂直な固定平面）上を、
> 重心を原点とする慣性楕円体が滑りなしに転がる運動として記述される。

---

## 8. ポリホードとヘルポリホード

### ポリホード（Polhode）

**ポリホード**は、接点 $\boldsymbol{p}$ が**慣性楕円体上**（剛体系）に描く曲線である。

$\boldsymbol{p} = \boldsymbol{\omega}/\sqrt{2T}$ であるから、ポリホードは次の二つの楕円体の交線に対応する。

$$
I_1 r_1^2 + I_2 r_2^2 + I_3 r_3^2 = 1 \quad (\text{慣性楕円体})
$$

$$
I_1^2 r_1^2 + I_2^2 r_2^2 + I_3^2 r_3^2 = \frac{L^2}{2T} \quad (\text{角運動量保存条件})
$$

二つの楕円体の交線は閉曲線（または退化して点や 8 の字）となり、
これが $\omega$ 空間（あるいは $L$ 空間）での軌道と対応する。

### ヘルポリホード（Herpolhode）

**ヘルポリホード**は、同じ接点 $\boldsymbol{p}$ が**不変平面上**（慣性系）に描く曲線である。

ポリホードが剛体に固定された内在的な軌跡であるのに対し、
ヘルポリホードは慣性系の固定平面上に描かれる外在的な軌跡である。

### 二者の関係

| | ポリホード | ヘルポリホード |
|---|---|---|
| 観測系 | 剛体系（body frame） | 慣性系（space frame） |
| 描かれる面 | 慣性楕円体の表面 | 不変平面 |
| 曲線の形 | 必ず閉曲線（周期的） | 一般に閉じない（非周期的） |

ポアンソーの描像では、剛体の運動は「ポリホードをヘルポリホード上で転がす」操作として
完全に可視化される。

---

## 参考文献

- H. Goldstein, C. Poole, J. Safko, *Classical Mechanics*, 3rd ed., Addison-Wesley (2002)
- L. D. Landau, E. M. Lifshitz, *Mechanics*, 3rd ed., Butterworth-Heinemann (1976)
- V. I. Arnold, *Mathematical Methods of Classical Mechanics*, Springer (1989)
- 原島鮮, 『力学』, 裳華房 (1981)
