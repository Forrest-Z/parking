# parking
此程序用于学习自动泊车，主要使用混合A*算法和数值优化的方法做自动停车

程序目前只关注一个周期的轨迹规划

1.参考apllo的混合A*算法生存初始路径

2.根据湖南大学李柏教授的行车隧道思想编写行车隧道算法

3.利用IPOPT 和ADOLC对优化问题进行求解

4.所有的数据通过matplotcpp进行图形绘制

此程序增加了cmakelists文件，但没有经过调试，等待后期调试
