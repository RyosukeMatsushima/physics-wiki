# シュレディンガー方程式の求め方

時間発展演算子
$$
|\alpha, t_0; t \rangle (t > t_0)
$$

$|\alpha, t_0 \rangle$ の状態から時間$t$に移動したということ。
($|\alpha, t_0; t \rangle$ は $t_0$のときに$|\alpha \rangle$だった)

$$
\lim_{t \to t_0} |\alpha, t_0; t \rangle = |\alpha, t_0 \rangle
$$

この極限は、時間発展演算子が$t_0$において元の状態$|\alpha, t_0 \rangle$に戻ることを示しています。

$$
|\alpha, t_0; t_0 \rangle = |\alpha, t_0 \rangle
$$

時間演算子$\mathcal{U}(t_0, t)$

$$
|\alpha, t_0; t \rangle = \mathcal{U}(t_0, t) |\alpha, t_0 \rangle
$$

$\mathcal{U}(t_0, t)$はユニタリ的。。。。

## ユニタリ的とは、

ユニタリ的（ユニタリー）とは、演算子がユニタリ演算子であることを意味します。  
ユニタリ演算子$\mathcal{U}$は、$\mathcal{U}^\dagger \mathcal{U} = \mathcal{U} \mathcal{U}^\dagger = I$を満たし、  
量子力学では時間発展演算子がユニタリであることで、状態のノルム（確率）が保存されます。


