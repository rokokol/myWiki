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

## Занятие №3 

### 79
 ![[умф 79.excalidraw|2048]]   

### 80
![[умф 80.excalidraw|2048]]

### 81
![[умф 81.excalidraw|2048]]

### 82
$$ e^{2x} u_{xx} + 2e^{x + y} u_{xy} + e^{2y} u_{yy} - xu = 0 $$
$$ e^{2x} \left(\dfrac{dy}{dx}\right)^2 - 2e^{x+y} \left(\dfrac{dy}{dx}\right) + e^{2y} = 0 $$
$$ D = 4e^{2(x+y)} - 4e^{2x + 2y} = 0 $$
$$ dy = \dfrac{2e^{x + y}}{2e^{2x}} \Rightarrow dy = e^{-x + y} $$

$$ y - e^{-x+y} = C $$
$$ \begin{cases}
\xi = y - e^{-x + y}  \\
\eta = x \\
\end{cases} \Rightarrow \begin{cases}
u_{x} = u_{\xi} e^{-x + y} + u_{\eta}  \\
u_{y} = u_{\xi} (1 - e^{-x + y}) \\
\end{cases} $$
$$\begin{cases}
u_{xx} = u_{\xi \xi} \cdot e^{-2(x-y)} - u_{\xi} \cdot e^{-x+y} + 2u_{\xi \eta} \cdot e^{-x + y} + u_{\eta \eta} \\
u_{yy} = u_{\xi \xi} (1 - e^{-x + y})^2 + u_{\xi} \cdot e^{-x + y}  \\
u_{xy} = u_{\xi \xi} (1 - e^{-x + y}) \cdot e^{-x + y} + u_{\xi} \cdot e^{-x+y} + u_{\xi \eta} (1 - e^{-x + y})
\end{cases}$$
$$ 3e^{2y} \cdot u_{\xi \xi} + 2 e^{x + y} \cdot u_{\xi \eta } + e^{2x} \cdot u_{\eta \eta} - xu = 0 $$


