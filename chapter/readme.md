##姓名：周一凡
##学号：2013301020017
###背景
习题3.4
>简谐振动的微分方程的一般形式加以拓展，即：![](https://raw.githubusercontent.com/fxdhi/computationalphysics_N2013301020017/master/chapter3/gif.latex.gif)

>对幂次分别为1和3时进行讨论,为了方便，k=1，其中$\alpha$=1时，对应简谐振动的情况，$\alpha$=3为非简谐振动的情况。探究两者振幅与周期的关系。


###正文
由于使用euler法会使每一步的系统能量不断增加，导致单方向累计的较大误差，故这里采用euler-cromer法对原有的算法做一点小小的修改，即在计算下一个时刻的位置是使用下一个时刻的速度，这样的改动可使每一步的误差得到控制。具体操作如下：

> - v[i+1]=v[i]-k*x[i]*dt
> - x[i+1]=x[i]+v[i+1]*dt
> - t[i+1]=t[i]+dt

在简谐振动中，所得图像为：
![](https://raw.githubusercontent.com/fxdhi/computationalphysics_N2013301020017/master/chapter3/exercise3.4.1.png)
在非简谐情况中，所得图像为：
![](https://raw.githubusercontent.com/fxdhi/computationalphysics_N2013301020017/master/chapter3/exercise3.4.2.png)
###结论
经过观察，可以发现，在简谐振动中，运动周期与振幅大小无关(此处振幅的大小取决于初速度)，而非简谐振动的情况下，振幅越小，振动周期越大，即两者是存在某种联系的。