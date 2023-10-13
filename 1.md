### 光纤（信息的损耗）

### 损耗：

* 来源：

  * 即使在理想的光纤中有损耗，称为<b>本征损耗</b>。

  * 吸收损耗：$SiO_2$中的分子会吸收本身的能量，将其转化为分子运动的能量。$$\begin{cases} 若吸收的分子是SiO_2 则为本征吸收损耗 \\ 若吸收的分子为杂志，则为非本征吸收损耗\end{cases}$$

  * 散射损耗：折射率的分布不均匀（*不同方向上的光会导致能量的逸散，使得最终目的地的光能量减少*）$$\begin{cases} 1.瑞利散射：由于分子运动带来的折射率的分布不均匀导致的，无法克服（决定了光纤最终的性能） \\ 2.波导散射：物理空间上折射率的不同，比如说纤芯和包层不完备等等，可以克服  \end{cases}$$

  * 弯曲损耗（非线性）：$$\begin{cases} 1.宏弯损耗：光纤本身发生弯折 \\ 2.微损耗弯：光纤成缆时受到的应力不同等等  \end{cases}$$

#### 吸收损耗：

* 度量：
  * **损耗系数（重要）**：$\alpha$ 损耗系数，单位有两种：$$\begin{cases} dB/km \\ 1/km ,国际单位制 \end{cases}$$，换算关系$\alpha (dB/km) = 4.343 \alpha(1/km)$
  * 损耗的主要方面在于散射损耗的瑞利散射，其一般发生在短波长***反比于波长的4次方***。也就是说，当我们考虑损耗系数的时候，光波的损耗系数也随着改变。$\frac{\alpha_1}{\alpha_2}= (\frac{\lambda_2}{\lambda_1})^4$.

* 光通信的三个通信窗口和三个波段：

  <center class='half'>
      <img src="https://cdn.jsdelivr.net/gh/ClearOVOsky/Image_typora@main/img/image-20231012133654340.png" alt="image-20231012133654340" style="zoom: 25%;" title ="光纤"/>  
      <img src="https://cdn.jsdelivr.net/gh/ClearOVOsky/Image_typora@main/img/image-20231012152630434.png" alt="image-20200927095842317" style="zoom:43%;" />
  </center>
  

* 损耗补偿：使用光放大器进行放大，从而对光纤损耗进行补偿。

#### 色散损耗：(将不同波长的光散开，本质是不同的波长在介质中的传播速度不一样,导致脉冲展宽)

<img src="https://cdn.jsdelivr.net/gh/ClearOVOsky/Image_typora@main/img/image-20231012160120999.png" alt="image-20231012160120999" style="zoom: 50%;" />

色散和三个因素有关：光纤本身的长度（传播距离），延时量（不同波长光波的传播速度之间的差异），波长差（所有光波的种类）

***色散系数***：表示的是色散的程度，$D=\frac{\triangle t}{\triangle \lambda \cdot L}$ ,单位$ps/nm/km$.

* 种类：模间色散（出现在多模光纤）和 **模内色散**（出现在单模光纤）以及偏振模色散。
  * 膜内色散$$ \begin{cases} 材料色散（materials）：相同材料对不同波长的光波传输速率不同\\ 波导色散（waveguide）：处于纤芯和包层的光的传播速度不同\end{cases}$$
  * 单模光纤的能量80%在纤芯，20%在包层。
* <font color = red>**群速度色散(GVD):**</font> 只有模内色散才叫群速度色散。
* 色散的计算及其对于传输容量的影响：

<center class='half'>
    <img src="https://cdn.jsdelivr.net/gh/ClearOVOsky/Image_typora@main/img/image-20231012180454095.png" alt="image-20231012180454095" style="zoom:50%;" />
    <img src="https://cdn.jsdelivr.net/gh/ClearOVOsky/Image_typora@main/img/image-20231012180548698.png" alt="image-20231012180548698" style="zoom:50%;" />
</center>

<center class='half'>
    <img src="https://cdn.jsdelivr.net/gh/ClearOVOsky/Image_typora@main/img/image-20231012181235675.png" alt="image-20231012181235675" style="zoom:50%;" />
    <img src="C:\Users\32860\AppData\Roaming\Typora\typora-user-images\image-20231013141313112.png" alt="image-20231013141313112" style="zoom:50%;" />
</center>




* 色散的优化设计：




#### 非线性损耗（非线性效应）：

##### 分类：

1. 非弹性散射：发生非弹性碰撞，能量转移到了另一个波长的光波上。

   两者的区别在于波长（$\lambda$）= $$\begin{cases} 受激布里渊散射（SBS） \\ 受激拉曼散射（SRS） \end{cases}$$

2. 非线性折射率（Kerr 效应）:光强随着时间变化，而折射率跟随着发生变化。

​		$$\begin{cases} 自相位调制（SPM）\\ 交叉相位调制（XPM）\\四波混频（FWM）  \end{cases}$$

##### 有效长度

* 假设传输过程中，传输的功率不变的话，光波的传输距离称为有效长度。

##### 有效面积

* 

#### 非弹性散射：

1. ***受激拉曼散射：***

   * 阈值功率：散射光功率等于入射光功率的一半时对一个的入射光功率。

   * $g_R P_{th} L_{eff} / A_{eff} \approx 16$

   * 特点：
     * 有前向散射，有后向散射
     * 增益范围达~30THz(约125nm)
     * SRS效应随着光功率的增加呈指数级别增长。

#### 非线性折射率：

1. 自相位调制（SPM）: