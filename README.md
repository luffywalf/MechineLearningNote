
# MechineLearningNote


# this vedio
repeat until convergence:
θj:=θj−α∂∂θjJ(θ0,θ1)

讲了梯度下降的数学原理，attention point
1.上面公式中的该是减号，比如现在二维曲线是上升的，那么其斜率∂∂θj会是正值，这样θj就会减小，也就是像x轴反向移动，即向曲线下降的地方移动，以达到最小值。 
2.当θj达到最小值，那么斜率会是0，所以即使α学习率一直是固定的也没关系

'''
【插播：什么是Linear Regression Model】

自己的理解
就是 输入与输出值可以用线性多项式来刻画的模型，一般用最小二乘法最为其loss function求解
最小二乘几何意义就是 求一个到所有点的距离和最小的平面，图片及公式见链接 http://blog.csdn.net/xbinworld/article/details/43919445

'''

# this vedio
tell us about linear regression with gradient descent, attention point
1.视频中是分别对θ1和θ2进行梯度下降公式求解，也就是说要分别对每个参数GD
2.我理解是说 一般GD的结果是局部最优local optima 但是对于linear regression的loss function往往是convex function(bowl shape)所以具有global optima
3.难道是我以前的理解有误？这里说batch GD是所有样本点m都参与计算---查了下 此说法正确 你印象里的那个叫 mini-batch GD

# this vedio
n = number of features
m = how many rows
默认x_0 = 1

# this vedio
feature scaling & mean normalization 注意分母是max-min 大概是因为减掉的是均值吧

# this vedio
对于其他算法可能不行 针对linear regression可以，在1000特征一下,ng更喜欢选择normal equation直接求解 不用GD的方法

# this vedio
对于classification often linear regression isnt a good idea,比如 极端负例使得整条直线的斜率变化很大
logistic regression 就是套了一层sigmoid function的linear regression嘛
how to choose theta automatically-------use cost function and GD
logistic regression的cost function换了负的log那种的 具体课堂笔记里有
https://www.coursera.org/learn/machine-learning/supplement/0hpMl/simplified-cost-function-and-gradient-descent

advanced:"Conjugate gradient", "BFGS", and "L-BFGS" are more sophisticated, faster ways to optimize θ that can be used instead of gradient descent. 

# this vedio: multiclass classification
one-vs-all 比如要分k类 那就训练k个比如logistic的二分类器，也是one-vs-rest

so我现在能想到的从linear->logistic的好处就是 它不再只能线性分类，而是通过表示成概率的形式，既增加了可分类线的形状，又使得预测值控制在0-1之间，好看

So, with these visualizations, I hope that gives you a sense of what's the range of hypothesis functions we can represent using the representation that we have for logistic regression.
所以圆什么的h of theta也是可以用在logistic上面，甚至更复杂的x1*x2也行
hθ(x)=g(θTx)
z=θTx
g(z)=11+e−z
有关z可以替换成复杂写的圆方程x平方，椭圆x1*x2

# this vedio: overfitting
regularization
minθ 12m ∑mi=1(hθ(x(i))−y(i))2+λ ∑nj=1θ2j
因为如果不知道该取舍哪个θ 所以干脆都放上 其中的λ系数可以控制还是以前面fit data为主
比如 minθ 12m∑mi=1(hθ(x(i))−y(i))2+1000⋅θ23+1000⋅θ24这种情况下 在min整体时 因为θ前的1000很大，so θ就会变得很小啦






















