
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
