# parking
此程序用于学习自动泊车，主要使用混合A*算法和数值优化的方法做自动停车

程序目前只关注一个周期的轨迹规划

1.参考apllo的混合A*算法生成初始路径

2.根据行车隧道思想编写行车隧道算法

3.利用IPOPT 和ADOLC对优化问题进行求解

4.所有的数据通过matplotcpp进行图形绘制

5.程序经过初步调试，测试结果如下图所示：

![HybirdAstarAndNLP](https://user-images.githubusercontent.com/54465004/196306792-24c2b755-c23c-45a7-90ae-dac78567ebb3.png)

![HybirdAstarAndNLP-侧方停车](https://user-images.githubusercontent.com/54465004/198972564-0e770c82-38e7-4df6-8041-97ff2d2fa62b.png)
![HybirdAstarAndNLP-倒车入库](https://user-images.githubusercontent.com/54465004/198972574-2d754c6a-8e1a-4065-80cb-222c39f0344f.png)

有待进一步研究：
1.混合A*的速度加速度信息的计算，目前使用的普通的计算方法，apollo的piecewise_jer_speed的速度优化方法暂未研究测试
2.没有和apollo对偶约束优化的方法进行对比
3.搭建ros的测试环境，封装为ros包，以增强其通用性
4.参数对曲线的影响有待进行调参测试
5.此方法是将对混合A*的所有点进行优化，需要对采用关键路标点，点与点之间使用曲线连接，对曲线优化的方法进行研究对比。


参考借鉴百度apollo 湖南大学李柏《自动驾驶决策规划技术理论与实践》的思想 浙江大学高飞移动机器人运动规划的知识 仅仅作为个人学习使用
