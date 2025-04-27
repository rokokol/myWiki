---
tags:
  - "#y2025"
  - "#умф"
  - кфу
  - семинары
master: "[[Матфизика Hub (практика)|Матфизика Hub (практика)]]"
aliases: 
created: 2025-04-03
icon: 🔤
---

### 103
$u_{xy}+u_{xz}+u_{yz}-u_{x}+u_{y}=0$
$$
\mathcal{F}=\begin{pmatrix}
0 & \frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & 0 & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & 0
\end{pmatrix}
$$

Канонизируем ее:
$$
xy+xz+yz=0 \implies
$$
$$
\begin{cases}
x=t_{1} \\
y=t_{2}+t_{3} \\
z=t_{2}-t_{3}
\end{cases} \implies
\begin{pmatrix}
1 & 0 & 0  \\
0 & 1 & 1 \\
0 & 1 & -1
\end{pmatrix} = S_{1}
$$
$$
\begin{multline}
t_{1}t_{2}+\cancel{ t_{1}t_{3} }+t_{1}t_{2}-\cancel{ t_{1}t_{3} }+t_{2}^{2}-t_{3}^{2}=0 \implies \\
 2t_{1}t_{2}+t_{2}^{2}-t_{3}^{2}=0\implies(t_{1}^{2}+2t_{1}t_{2}+t_{2}^{2})-t_{3}^{2}-t_{1}^{2}=0 \implies \\
(t_{1}+t_{2})^{2}-t_{3}^{2}-t_{1}^{2}=0
\end{multline}
$$
$$
\begin{cases}
m_{1}=t_{1} \\
m_{2}=t_{1}+t_{2} \\
m_{3}=t_{3}
\end{cases}\implies
\begin{cases}
t_{1}=m_{1} \\
t_{2}=-m_{1}+m_{2}\\
t_{3}=m_{3}
\end{cases}\implies
\begin{pmatrix}
1 & 0 & 0 \\
-1 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} = S_{2}
$$
$$
\boxed{ -m_{1}^{2}+m_{2}^{2}-m_{3}^{2}=0 }
$$
$$
S_{1}S_{2}=\begin{pmatrix}
1 & 0 & 0 \\
-1 & 1 & 1  \\
-1 & 1 & -1
\end{pmatrix} = A \implies
A^{T}=\begin{pmatrix}
1 & -1 & -1 \\
0 & 1 & 1 \\
0 & 1 & -1
\end{pmatrix} \implies \eta=A^{T}\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}\implies
$$
Делаем замену:
$$
\begin{cases}
\eta=x-y-z \\
\xi=y+z \\
\mu=y-z
\end{cases}
$$

Теперь находим частные производные $u$ первого порядка:
$$
\begin{matrix}
u_{x}=u_{\eta} \\
u_{y}=-u_{\eta}+u_{\xi}+u_{\mu} \\
u_{z}=-u_{\eta}+u_{\xi}-u_{\mu}
\end{matrix}
$$

Следующий шаг — поиск $u_{xz},~u_{xy},~u_{yz}$:
$$
\begin{cases}
u_{xz}=-u_{\eta \eta}+u_{\eta\xi}-u_{\eta\mu} \\
u_{xy}=-u_{\eta \eta}+u_{\eta\xi}+u_{\eta\mu} \\
u_{yz}=u_{\eta \eta}-u_{\eta \xi}+u_{\eta \mu}-u_{\xi \eta}+u_{\xi \xi}-\cancel{ u_{\xi \mu} }+u_{\eta \mu}+\cancel{ u_{\mu \xi} }-u_{\mu \mu} = u_{\eta \eta}+u_{\xi \xi}-u_{\mu \mu}-2u_{\eta \xi}+2u_{\eta \mu}
\end{cases}
$$
Подставляем все это в исходное уравнение:
$$
\begin{multline}
-u_{\eta \eta}+\cancel{ u_{\eta\xi} }+\cancel{ u_{\eta\mu} }-u_{\eta \eta}+\cancel{ u_{\eta\xi} }-\cancel{ u_{\eta\mu} } \\
+u_{\eta \eta}+u_{\xi \xi}-u\cancel{ _{\mu \mu} }-\cancel{ 2u_{\eta \xi} }+2u_{\eta \mu}-u_{\eta}-u_{\eta}+u_{\xi}+u_{\mu}= \\
-u_{\eta \eta}+u_{\xi \xi}+u_{\xi}+u_{\mu}
\end{multline}
$$

## ДЗ
![[Сигнатуры матрицы.png]]

### 107
$2u_{xx}+5u_{yy}+2u_{zz}-6u_{xy}-4u_{xz}+6u_{yz}-3u+y-2z=0$
![[107 умф|2048]]
#### 106
![[106 умф|2048]]

### 102
Исходное уравнение:
$u_{xx}-4u_{xy}+2u_{xz}+u_{zz}+3u_{x}=0$

Канонизируем же его:
![[Pasted image 20250403140115.png]]
### 108
$3u_{yy}-2u_{xy}-2u_{yz}+4u=0$
Канонизируем уравнение:
$$
3yy-2xy-2yz=3y^{2}-2xy-2yz=0
$$
Сделаем замену:
$$
\begin{cases}
x=t_{1}+t_{2} \\
y=t_{1}-t_{2} \\
z=t_{3}
\end{cases}\implies
$$
Имеем:
$$
3t_{1}^{2}-6t_{1}t_{2}+3t_{2}^{2}-2t_{1}^{2}+t_{2}^{2}-2t_{1}t_{3}+2t_{2}t_{3}=0
$$

1. *Эллиптический* — все одного знака
2. *Параболический* — один из коэффициентов исчезат
3. *Гиперболический* — все разных знаков