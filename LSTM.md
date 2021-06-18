<a href="https://www.codecogs.com/eqnedit.php?latex=\Delta&space;W_{[u,&space;v]}&space;=&space;-&space;\eta&space;\frac{\partial&space;E}{\partial&space;W_{[u,&space;v]}}" target="_blank"><img src="https://latex.codecogs.com/svg.latex?\Delta&space;W_{[u,&space;v]}&space;=&space;-&space;\eta&space;\frac{\partial&space;E}{\partial&space;W_{[u,&space;v]}}" title="\Delta W_{[u, v]} = - \eta \frac{\partial E}{\partial W_{[u, v]}}" /></a>

1. 从output 到 hidden layer

<a href="https://www.codecogs.com/eqnedit.php?latex=\Delta&space;W_{[h,&space;o]}&space;=&space;-&space;\eta&space;\frac{\partial&space;E}{\partial&space;W_{[h,&space;o]}}&space;=&space;-\eta&space;\frac{\partial&space;E}{\partial&space;y_o}&space;\cdot\frac{\partial&space;y_o}{\partial&space;s_o}&space;\cdot&space;\frac{\partial&space;s_o}{\partial&space;W_{[h,&space;o]}}" target="_blank"><img src="https://latex.codecogs.com/svg.latex?\Delta&space;W_{[h,&space;o]}&space;=&space;-&space;\eta&space;\frac{\partial&space;E}{\partial&space;W_{[h,&space;o]}}&space;=&space;-\eta&space;\frac{\partial&space;E}{\partial&space;y_o}&space;\cdot\frac{\partial&space;y_o}{\partial&space;s_o}&space;\cdot&space;\frac{\partial&space;s_o}{\partial&space;W_{[h,&space;o]}}" title="\Delta W_{[h, o]} = - \eta \frac{\partial E}{\partial W_{[h, o]}} = -\eta \frac{\partial E}{\partial y_o} \cdot\frac{\partial y_o}{\partial s_o} \cdot \frac{\partial s_o}{\partial W_{[h, o]}}" /></a>


[comment]: <> (<a href="https://www.codecogs.com/eqnedit.php?latex=\begin{align*}&space;\Delta&space;W_{[h,&space;o]}&space;&=&space;-&space;\eta&space;\frac{\partial&space;E}{\partial&space;W_{[h,&space;o]}}&space;\\&space;&=&space;-&space;\eta&space;\frac{\partial&space;E}{\partial&space;y_o}&space;\frac{\partial&space;y_o}{\partial&space;s_o}&space;\frac{\partial&space;s_o}{\partial&space;W_{[h,&space;o]}}&space;\end{align*}" target="_blank"><img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;\Delta&space;W_{[h,&space;o]}&space;&=&space;-&space;\eta&space;\frac{\partial&space;E}{\partial&space;W_{[h,&space;o]}}&space;\\&space;&=&space;-&space;\eta&space;\frac{\partial&space;E}{\partial&space;y_o}&space;\frac{\partial&space;y_o}{\partial&space;s_o}&space;\frac{\partial&space;s_o}{\partial&space;W_{[h,&space;o]}}&space;\end{align*}" title="\begin{align*} \Delta W_{[h, o]} &= - \eta \frac{\partial E}{\partial W_{[h, o]}} \\ &= - \eta \frac{\partial E}{\partial y_o} \frac{\partial y_o}{\partial s_o} \frac{\partial s_o}{\partial W_{[h, o]}} \end{align*}" /></a>
)


下面分别计算每一项：

<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;E}{\partial&space;y_o}&space;=&space;\frac{\frac{1}{2}&space;\sum_{k\in&space;O}e_k^2}{\partial&space;y_o}&space;=&space;\frac{\frac{1}{2}e_o^2}{\partial&space;y_o}&space;=&space;e_o&space;\frac{e_o}{\partial&space;y_o}&space;=&space;-(d_o-y_o)" target="_blank"><img src="https://latex.codecogs.com/svg.latex?\frac{\partial&space;E}{\partial&space;y_o}&space;=&space;\frac{\frac{1}{2}&space;\sum_{k\in&space;O}e_k^2}{\partial&space;y_o}&space;=&space;\frac{\frac{1}{2}e_o^2}{\partial&space;y_o}&space;=&space;e_o&space;\frac{e_o}{\partial&space;y_o}&space;=&space;-(d_o-y_o)" title="\frac{\partial E}{\partial y_o} = \frac{\frac{1}{2} \sum_{k\in O}e_k^2}{\partial y_o} = \frac{\frac{1}{2}e_o^2}{\partial y_o} = e_o \frac{e_o}{\partial y_o} = -(d_o-y_o)" /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;y_o}{\partial&space;s_o}&space;=&space;y_o(1-y_o),&space;\quad&space;\because&space;y_o&space;=&space;\sigma(s_o),&space;\sigma'(x)&space;=&space;\sigma(x)(1-\sigma(x))" target="_blank"><img src="https://latex.codecogs.com/svg.latex?\frac{\partial&space;y_o}{\partial&space;s_o}&space;=&space;y_o(1-y_o),&space;\quad&space;\because&space;y_o&space;=&space;\sigma(s_o),&space;\sigma'(x)&space;=&space;\sigma(x)(1-\sigma(x))" title="\frac{\partial y_o}{\partial s_o} = y_o(1-y_o), \quad \because y_o = \sigma(s_o), \sigma'(x) = \sigma(x)(1-\sigma(x))" /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;s_o}{\partial&space;W_{[h,&space;o]}}&space;=&space;\frac{\partial&space;(\sum_v&space;W_{[v,&space;o]}y_v)}{\partial&space;W_{[h,o]}}&space;=&space;y_h" target="_blank"><img src="https://latex.codecogs.com/svg.latex?\frac{\partial&space;s_o}{\partial&space;W_{[h,&space;o]}}&space;=&space;\frac{\partial&space;(\sum_v&space;W_{[v,&space;o]}y_v)}{\partial&space;W_{[h,o]}}&space;=&space;y_h" title="\frac{\partial s_o}{\partial W_{[h, o]}} = \frac{\partial (\sum_v W_{[v, o]}y_v)}{\partial W_{[h,o]}} = y_h" /></a>

对output unit o 定义 error signal :

<a href="https://www.codecogs.com/eqnedit.php?latex=\vartheta_o&space;:=-\frac{\partial&space;E}{\partial&space;y_o}\frac{\partial&space;y_o}{\partial&space;s_o}&space;=&space;(d_o-y_o)y_o(1-y_o)" target="_blank"><img src="https://latex.codecogs.com/svg.latex?\vartheta_o&space;:=-\frac{\partial&space;E}{\partial&space;y_o}\frac{\partial&space;y_o}{\partial&space;s_o}&space;=&space;(d_o-y_o)y_o(1-y_o)" title="\vartheta_o :=-\frac{\partial E}{\partial y_o}\frac{\partial y_o}{\partial s_o} = (d_o-y_o)y_o(1-y_o)" /></a>

因此，可以基于下面公式更新hidden unit h 和 output unit o 之间的weight W

<a href="https://www.codecogs.com/eqnedit.php?latex=\Delta&space;W_{[h,&space;o]}&space;=&space;\eta&space;\vartheta_o&space;y_h" target="_blank"><img src="https://latex.codecogs.com/svg.latex?\Delta&space;W_{[h,&space;o]}&space;=&space;\eta&space;\vartheta_o&space;y_h" title="\Delta W_{[h, o]} = \eta \vartheta_o y_h" /></a>


2. 从hidden  到 hidden layer

<a href="https://www.codecogs.com/eqnedit.php?latex=\Delta&space;W_{[i,&space;h]}&space;=&space;-&space;\eta&space;\sum_o&space;\frac{\partial&space;E}{\partial&space;y_o}&space;\frac{\partial&space;y_o}{\partial&space;s_o}&space;\cdot&space;\frac{\partial&space;s_o}{\partial&space;y_h}&space;\cdot&space;\frac{\partial&space;y_h}{\partial&space;s_h}&space;\cdot&space;\frac{\partial&space;s_h}{\partial&space;W_{[i,h]}}&space;\quad&space;\text{with}&space;\&space;o&space;\in&space;\text{Suc}(h)" target="_blank"><img src="https://latex.codecogs.com/svg.latex?\Delta&space;W_{[i,&space;h]}&space;=&space;-&space;\eta&space;\sum_o&space;\frac{\partial&space;E}{\partial&space;y_o}&space;\frac{\partial&space;y_o}{\partial&space;s_o}&space;\cdot&space;\frac{\partial&space;s_o}{\partial&space;y_h}&space;\cdot&space;\frac{\partial&space;y_h}{\partial&space;s_h}&space;\cdot&space;\frac{\partial&space;s_h}{\partial&space;W_{[i,h]}}&space;\quad&space;\text{with}&space;\&space;o&space;\in&space;\text{Suc}(h)" title="\Delta W_{[i, h]} = - \eta \sum_o \frac{\partial E}{\partial y_o} \frac{\partial y_o}{\partial s_o} \cdot \frac{\partial s_o}{\partial y_h} \cdot \frac{\partial y_h}{\partial s_h} \cdot \frac{\partial s_h}{\partial W_{[i,h]}} \quad \text{with} \ o \in \text{Suc}(h)" /></a>

\Delta W_{[i, h]} = - \eta \sum_o  \frac{\partial E}{\partial  y_o}
\frac{\partial y_o}{\partial  s_o} 
\cdot \frac{\partial s_o}{\partial  y_h}
\cdot \frac{\partial y_h}{\partial  s_h} 
\cdot \frac{\partial s_h}{\partial W_{[i,h]}} 
\quad \text{with} \ o \in \text{Suc}(h)

