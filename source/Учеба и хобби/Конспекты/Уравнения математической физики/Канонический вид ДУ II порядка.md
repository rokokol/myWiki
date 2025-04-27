---
tags:
  - "#y2025"
  - умф
  - конспекты
  - учеба
  - кфу
master: "[[УМФ Hub (лекции)]]"
created: 2025-04-11
aliases: 
icon: LiSkull
---
# Классификация и приведение к каноническому виду ДУ II порядка
> [!note] Уравнение в частных производных II порядка
> Так называют уравнения вида
> $\sum\limits_{i,j=1}^{n}a_{ij}\frac{ \partial ^2u }{ \partial x_{i} \partial x_{j} } + \sum\limits_{i=1}^{n}b_{i}\frac{ \partial u }{ \partial x_{i} }+cu+f(x) = 0$
> Где
> $u=u(x_{1}, \dots,x_{n}), c=c(x_{1}, \dots,x_{n}), a_{ij}=a_{ij}(x_{1}, \dots,x_{n}), b_{i}=b_{i}(x_{1}, \dots,x_{n})$
> Если же 
> $u,c,a_{ij},b_{i}=\text{const} ~ \forall j,i$
> То гворят, что *уравнение имеет постоянные коэффициенты*

## Канонические ДУ II порядка (случай $n=2$)
Мы работаем с уравнениями вида
$$a_{11}(x, y)\frac{ \partial ^2u }{ \partial x^2 }+2a_{12}\frac{ \partial ^2u }{ \partial x \partial y }+a_{22}\frac{ \partial ^2u }{ \partial y^2 }+F\left( f(x,y), \frac{ \partial u }{ \partial x }, \frac{ \partial u }{ \partial y }, u \right)=0$$
> [!tip] Будем рассматривать только тот случай, когда функция $u(x,y) \in C^2$, благодаря чему ее смешанный производные второго порядка равны

> [!warning] Будем использовать следующие сокращения:
> $u_{x}=\frac{ \partial u }{ \partial x },u_{xx}=\frac{ \partial ^2u }{ \partial x^2 },u_{xy}=\frac{ \partial ^2u }{ \partial x \partial y }$

Исследуем как следует такие уравнения. Сделаем замену переменных:
$$\xi=\varphi(x,y), ~ \eta=\psi(x,y)$$
Причем эти функции должны быть линейно независимы:
$$\underbrace{ \mathfrak{J} }_{ \Large\text{Якобиан} }=
\begin{vmatrix}
\frac{ \partial \phi }{ \partial x } & \frac{ \partial \phi }{ \partial y }  \\
\frac{ \partial \psi }{ \partial x } & \frac{ \partial \psi }{ \partial y } 
\end{vmatrix} \neq 0$$

Выведем несколько полезных формул:
$$
u_{x}=u_{\xi}\xi_{x}+u_{\eta}\eta_{x}\implies
$$
$$\implies u_{xy}=u_{\xi \xi}\xi_{x}\xi_{y}+u_{\xi \eta}(\xi_{x}\eta_{y}+\xi_{y}\eta_{x})+u_{\eta \eta}\eta_{x}\eta_{y}+u_{\eta}\eta_{xy}+u_{\xi}\xi_{xy}$$
Или, частный случай
$$u_{xx}=u_{\xi \xi}(\xi_{x})^2+2u_{\xi \eta}\xi_{x}\eta_{x}+u_{\eta \eta}(\eta_{x})^2+u_{\xi}\xi_{xx}+u_{\eta}\eta_{xx}$$

Подставляя это в исходное уравнение получаем:
$$
\begin{multline}
u_{\xi \xi} \overbrace{[a_{11}(\xi_x)^2 + a_{12} \xi_x \xi_y + a_{22} (\xi_y)^2]}^{\tilde{a}_{11}} 
+ u_{\eta \eta} \overbrace{[a_{11} (\eta_x)^2 + 2a_{12} \eta_x \eta_y + a_{22} (\eta_y)^2]}^{\tilde{a}_{22}} + \\
+ u_{\eta \xi} \underbrace{[2a_{11} \xi_x \eta_x + 2a_{22}\xi_y \eta_y + 2a_{12} (\xi_x \eta_y + \xi_y \eta_x)]}_{\tilde{a}_{12}} 
+ \tilde{F} (\xi, \eta, u, u_\xi, u_\eta) = 0
\end{multline}
$$
> [!success] Благодаря этой замене мы можем примести любое ДУ II порядка к каноническому виду
> $u_{\xi \xi}\tilde{a}_{11}+2u_{\xi \eta}\tilde{a}_{12}+u_{\eta \eta}\tilde{a}_{22}+ \tilde{F} (\xi, \eta, u, u_\xi, u_\eta) = 0$

### Подберем функцию $\xi=\varphi(x,y)$ ($\eta=\psi(x,y)$) так, так, чтобы $\tilde{a}_{11}=0$ ($\tilde{a}_{22}=0$)
$$
\begin{align}
a_{11} (\xi_x)^2 + 2 a_{12} \xi_x \xi_y + a_{22} (\xi_y)^2=0 \implies \\
\implies a_{11} \left(\dfrac{\xi_x}{\xi_y}\right)^2 + 2 a_{12} \left(\dfrac{\xi_x}{\xi_y}\right) + a_{22} = 0 
\end{align}
$$

Положим $\xi(x, y) = \text{const}$, выразим тогда $y = y(x)$. Отсюда получаем $d\xi = \xi_x dx + \xi_y dy \implies \dfrac{dy}{dx} = -\dfrac{\xi_x}{\xi_y}$ (как по теореме о неявной функции)
Значит имеем:
$$a_{11} \left(\dfrac{dy}{dx}\right)^2 - 2a_{12} \left(\dfrac{dy}{dx}\right) + a_{22} = 0$$

Потом можно получить характеристическое уравнение:
> [!tip] Характеристическое уравнение исходного выражения
$a_{11} (dy)^2 - 2 a_{12} dy dx + a_{22} (dx)^2 = 0$ 

Далее выразим $\frac{dy}{dx}$:
$$\dfrac{dy}{dx} = \dfrac{a_{12} \pm \overbrace{\sqrt{(a_{12})^2 - a_{11} a_{22}}}^{D}}{a_{11}}$$

В зависимости от $D$ определяется тип ДУ
> [!note] Виды канонических ДУ II порядка
> - $D > 0$ — *гиперболический* тип
> - $D = 0$ — *параболический* тип
> - $D < 0$ — *эллиптический* тип

Для каждого из них определен свой порядок действий:
1. $D>0\implies$ Делаем замену $\xi=\varphi(x,y)=\text{const},~\eta=\psi(x,y)=\text{const}$ 
2. $D=0\implies$ У нас единственное решение $\xi=\varphi(x,y)=\text{const}$. Тогда вводим вторую, линейно независимую с $\varphi(x,y)$ функцию $\eta=\psi(x,y)=\text{const}$
3. $D<0\implies$ У нас будет пара сопряженных комплексных чисел $\underbrace{ {\varphi(x,y)} }_{ \xi(x,y) }\pm i \underbrace{ \psi(x,y) }_{ \eta(x,y) }=\text{const}$

> [!warning] Где $\varphi(x,y)$ и $\psi(x,y)$ — первые интегралы системы

#### Рассмотрим каждый из них по отдельности детальнее
##### $D>0$ (гиперболический)
Тогда $\xi=\frac{\varphi+\psi}{2}$, $\eta=\frac{\varphi-\psi}{2}$, а исходное уравнение имеет вид $2\tilde{a}_{12}u_{\xi \eta}+\tilde{F}=0$

##### $D=0$ (параболический)
Тогда $\xi=\varphi(x,y)$, $\eta=\psi(x,y)$, а $D=a_{12}^{2}-a_{11}a_{22}=0\implies a_{12}=\sqrt{ a_{11}a_{22} }$

Собирая полные квадраты получаем:
$$
\begin{matrix}
\tilde{a}_{11}=(\sqrt{ a_{11} }\xi_{x}+\sqrt{ a_{22} }\xi_{y})^{2}=(-\sqrt{ a_{22} }\xi_{y}+\sqrt{ a_{22} }\xi_{y})=0  \\
\tilde{a}_{12}=\sqrt{ a_{11} }\xi_{x}(\sqrt{ a_{11} }\eta_{x}+\sqrt{ a_{22} }\eta_{y})+\sqrt{ a_{22} }\xi_{y}(\sqrt{ a_{11} }\eta_{x}+\sqrt{ a_{22} }\eta_{y})= \\
=(\sqrt{ a_{11} }\xi_{x}+\sqrt{ a_{22} }\xi_{y})(\sqrt{ a_{11} }\eta_{x}+\sqrt{ a_{22} }\eta_{y})
\end{matrix}
$$


##### $D<0$ (эллиптический)
Тогда $\xi=\varphi+i\psi$, $\eta=\varphi-i\psi$, а $D=a_{12}^{2}-a_{11}a_{22}<0$
Для исследования уравнений этого типа введем следующие переменные:
$$
\begin{cases}
\alpha=\frac{\xi+\eta}{2} \\
\beta=\frac{\xi-\eta}{2i}
\end{cases}
\implies
\begin{matrix}
\xi=\alpha+i\beta=\xi(\alpha(x,y),\beta(x,y)) \\
\eta=\alpha-i\beta=\eta(\alpha(x,y),\beta(x,y))
\end{matrix}
$$

Найдем тогда $\tilde{a}_{11}:$
 $\tilde{a}_{11}=a_{11}(\alpha_{x}+i\beta_{x})^{2}+2a_{12}(\alpha_{x}+i\beta_{x})(\alpha_{y}+i\beta_{y})+a_{22}(\alpha_{y}+i\beta_{y})^{2}=0\implies$
$$
\implies \begin{cases}
\alpha \colon a_{11}(\alpha_{x})^{2}+2a_{12}\alpha_{x}\alpha_{y}+a_{22}(\alpha_{y})^{2} \\
\beta \colon a_{11}(\beta_{x})^{2}+2a_{12}\beta_{x}\beta_{y}+a_{22}(\beta_{y})^{2} \\
i\colon 2i[a_{11}\alpha_{x}\beta_{x}+a_{12}(\alpha_{x}\beta_{y}+\beta_{x}\alpha_{y})+a_{22}\alpha_{y}\beta_{y}]
\end{cases}
$$
**А это достигается тогда, когда $\tilde{a}_{11}=\tilde{a}_{22}$, а $\tilde{a}_{12}=0$**, если положить в формулах $\tilde{a}$ члены $\xi$ и $\eta$ равными соответствующими $\alpha$ и $\beta$

> [!faq] Приведем к канонической форме уравнение $x^{4}u_{xx}-y^{4}u_{yy}=0$
> Для начала составим характеристическое уравнение: 
> $x^{4}(dy)^2 - y^{4}(dx)^2 = 0$ 
> Тогда $D=2y^{2}>0\implies$ *гиперболический тип*
> $\left( \frac{dy}{dx} \right)^{2}-\Bigl( \frac{y}{x} \Bigr)^{4}=0\implies$
> $\implies \frac{dy}{dx}=\pm\left( \frac{y}{x} \right)^{2}$
> Решив ДУ мы получаем 2 корня:
> - $\xi=\frac{1}{y}+\frac{1}{x}=С=\text{const}$
> - $\eta=\frac{1}{y}-\frac{1}{x}=C=\text{const}$
> 
> Далее находим
>  $u_{xx}=\left( u_{\xi}\left( \overbrace{ -\frac{1}{x^{2}} }^{ \text{Производная } \xi \text{ по } x } \right)+u_{\eta}\left( \overbrace{ \frac{1}{x^{2}} }^{ \text{Производная } \eta \text{ по } x } \right) \right)_{x}'=\frac{1}{x^4} \bigl( u_{\xi\xi} - 2 u_{\xi\eta} + u_{\eta\eta} \bigr) + \frac{2}{x^3} (u_\xi - u_\eta)$ 
> и
>   $u_{yy}=\left( u_{\xi}\left( \overbrace{ -\frac{1}{y^{2}} }^{ \text{Производная } \xi \text{ по } y } \right)+u_{\eta}\left( \overbrace{ -\frac{1}{y^{2}} }^{ \text{Производная } \eta \text{ по } y } \right) \right)_{x}'=\frac{1}{y^4} \bigl( u_{\xi\xi} + 2 u_{\xi\eta} + u_{\eta\eta} \bigr)+\frac{2}{y^3} (u_\xi + u_\eta)$
> 
> Следующим шагом вычисляем $x^{4}u_{xx}-y^{4}u_{yy}$ и получаем следующее выражение
> $x^4 u_{xx} - y^4 u_{yy} =\dots= - 4 u_{\xi\eta} + 2 (x - y) u_{\xi} - 2 (x + y) u_{\eta}$
> 
> После, исходя из формул $\xi$ и $\eta$ выражаем $x+y$ и $x-y$ через $\xi$ и $\eta$:
> - $x-y=4 \frac{\eta}{\xi^{2}-\eta^{2}}$
> - $x+y=4 \frac{\xi}{\xi^{2}-\eta^{2}}$
> 
> *Осталось лишь подставить $x+y$ и $x-y$ и получить уравнение, записанное в канонической форме, зависящее лишь от $\xi$ и $\eta$:*
> $-\frac{8\eta}{\xi^2 - \eta^2} u_\xi - 4 u_{\xi\eta} - \frac{8\xi}{\xi^2 - \eta^2} u_\eta = 0$

> [!warning] На линейной алгебре было нечто подобное для уравнений с постоянными коэффициентами. Наш же способ работает и в том случае, но не наоборот


### Случай с постоянными коэффициентами

##### $D>0$ (гиперболический)
Решая уравнение, и, после интегрируя обе части, получаем 
$$
y_{1,2}=\frac{a_{12}\pm\sqrt{ a_{12}^{2}-a_{11}a_{22} }}{a_{11}}x + C
$$
Тогда наши первые интегралы системы имеют вид:
$$
\begin{cases}
\xi=y-\frac{a_{12}+\sqrt{ a_{12}^{2}-a_{11}a_{22} }}{a_{11}}x \\
\underbrace{ \eta=y-\frac{a_{12}-\sqrt{ a_{12}^{2}-a_{11}a_{22} }}{a_{11}}x }_{ \text{Они должны равняться константе }С }
\end{cases}
$$

В таком случае каноническая форма будет иметь следующий вид:
$$
2\tilde{c}a_{12}u_{\xi \eta}+\tilde{F}(\xi, \eta, u)=0
$$

##### $D=0$ (параболический)
Имеем уравнение:
$$
dy=\frac{a_{12}}{a_{11}}dx
$$
Отсюда делаем, соответственно, следующую замену:
$$
\xi=y-\frac{a_{12}}{a_{11}}x
$$
При этом $\eta$ мы выбираем сами. Например, для удобства **возьмем $\eta=y$**
В таком случае каноническая форма будет иметь следующий вид:
$$
u_{\xi \xi}+\tilde{c_{1}}u_{\xi}+\tilde{c_{2}}u_{\eta}+\tilde{F}(\xi,\eta,n)=0
$$

##### $D<0$ (эллиптический)
Тогда будем иметь уравнение
$$
y=\frac{a_{12}\pm i\sqrt{ a_{12}^{2} - a_{11}2_{22} }}{a_{11}}x + C
$$

Таким образом, разделяя на мнимую и вещественную часть, мы получаем следующую замену:
$$
\begin{cases}
\xi=y-\frac{a_{12}}{a_{11}}x \\
\eta=\frac{\sqrt{ a_{12}^{2} -a_{11}a_{22}}}{a_{11}}x
\end{cases}
$$

В таком случае каноническая форма будет иметь следующий вид:
$$
u_{\xi \xi}+u_{\eta \eta}+\tilde{F}(\xi, \eta, u, u_{\xi}, u_{\eta})=0
$$

#### Примеры
> [!warning] **$\overbrace{ 36 }^{ a_{11} }u_{xx}\overbrace{ -12 }^{ 2a_{12} }u_{xy}+\overbrace{ 1 }^{ a_{22} }u_{yy}+18u_{x}-3u_{y}=0$**
> После замены и нахождения $u_{xx}, u_{xy}, u_{yy},u_{x}, u_{y}$ получаем **ответ: $u_{\eta \eta}+\frac{1}{2}u_{\xi}=0$**

> [!warning] **$\overbrace{ 5 }^{ a_{11} }u_{xx}+\overbrace{ 4 }^{ 2a_{12} \implies a_{12}=2 }u_{xy}+\overbrace{ 1 }^{ a_{22} }u_{yy}+u_{x}+u_{y}=0$**
> Снова делаем замену, находим те же $u_{xx}, u_{xy}, u_{yy},u_{x}, u_{y}$ и после подстановки получаем **ответ $u_{\xi \xi}+u_{\eta \eta}+\frac{3}{5}u_{\xi}+\frac{1}{5}u_{\eta}=0$**

# 
