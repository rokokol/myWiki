---
tags:
  - "#y2025"
  - "#умф"
  - кфу
  - семинары
master: "[[Матфизика Hub (практика)|Матфизика Hub (практика)]]"
aliases: 
icon: LiRemoveFormatting
---

## С переменными коэффициентами

### 75
$(1+x^{2})^{2}u_{xx}+u_{yy}+2x(1+x^{2})u_{x}=0$
Характеристическое уравнение:
$$
\begin{align}
(1+x^{2})^{2}dy^{2}+dx^{2} =0  \\
(1+x^{2})^{2}y'^{2}+1 =0  \\
dy=\pm \frac{i\sqrt{ 4(1+x^{2})^{2} }}{2(1+x^{2})^{2}} \\
y+C=\pm i\arctan x \\
y\pm i\arctan x=C \\
\end{align}
$$
Тогда делаем замену:
$$
\begin{cases}
\xi=y \\
\eta=\arctan x
\end{cases}\implies \begin{cases}
u_{x}=u_{\eta} \frac{1}{1+x^{2}}\\
u_{y}=u_{\xi}
\end{cases} \implies \begin{cases}
u_{xx}=u_{\eta \eta}\left( \frac{1}{1+x^{2}} \right)^{2}-u_{\eta} \frac{2x}{(1+x^{2})^{2}} \\
u_{yy}=u_{\xi \xi}
\end{cases}
$$
Подставляя в исходное уравнение, получаем:
$$
\boxed{ u_{\eta \eta}+u_{\xi \xi}=0 }
$$

## ДЗ
### 76
![[76 умф|2048]]
### 77
![[77 умф|2048]]
### 78
$$ (1 + x^2)u_{xx} + (1 + y^2)u_{yy} + xu_x + yu_y - 2u = 0 $$
$$ (1 + x^2)\left(\dfrac{dy}{dx}\right)^2 + (1 + y^2) = 0 $$
$$ D = -4(1 + x^2)(1 + y^2) $$
$$ \dfrac{dy}{dx} = \dfrac{0 \pm \sqrt{-4(1 + x^2)(1 + y^2)}}{2(1 + x^2)} $$
$$ dy = \pm \dfrac{i \sqrt{1 + y^2}}{\sqrt{1 + x^2}} dx $$
$$ \int \dfrac{1}{\sqrt{1 + y^2}} dy = \pm i \int \dfrac{1}{\sqrt{1 + x^2}} dx $$
$$ \ln |y + \sqrt{y^2 + 1}| = \pm i \ln |x + \sqrt{x^2 + 1}| + C $$
$$ \begin{cases}
        \xi = \ln (y + \sqrt{y^2 + 1}) + \ln (x + \sqrt{x^2 + 1})  \\
        \eta = \ln (y + \sqrt{y^2 + 1}) - \ln (x + \sqrt{x^2 + 1}) \\
    \end{cases} $$
$$ \begin{cases}
        \xi_x = \dfrac{1}{\sqrt{x^2 + 1}}    \\
        \xi_y = \dfrac{1}{\sqrt{y^2 + 1}}    \\
        \eta_x = - \dfrac{1}{\sqrt{x^2 + 1}} \\
        \eta_y = \dfrac{1}{\sqrt{y^2 + 1}}   \\
    \end{cases} \Rightarrow \begin{cases}
        u_x = \dfrac{u_\xi - u_\eta}{\sqrt{x^2 + 1}} \\
        u_y = \dfrac{u_\xi + u_\eta}{\sqrt{y^2 + 1}} \\
    \end{cases}  $$
$$ \begin{cases}
        u_{xx} = \dfrac{u_{\xi\xi} - 2 u_{\xi\eta} + u_{\eta\eta}}{x^2 + 1} - x (x^2 + 1)^{-3/2} (u_\xi - u_\eta) \\
        u_{yy} = \dfrac{u_{\xi\xi} + 2 u_{\xi\eta} + u_{\eta\eta}}{y^2 + 1} - y (y^2 + 1)^{-3/2} (u_\xi + u_\eta)
    \end{cases} $$
$$ u_{\xi\xi} + u_{\eta\eta} = u $$
