---
layout: post
title: 「数学建模简易教程」Matlab基础
date: 2019-03-17
categories: 技术
---

这个系列文章主要围绕数学建模这一主题去学习，主要目的是五一数学建模大赛

## Matlab语法基础

#### 基础语法

1. 常用命令
   * `clear` - 清除工作空间变量
   * `clc` - 清除窗口内容
   * `figure` - 打开图形窗口
2. 创建数组
   * `a1 = [1,2,3,4]`
   * `a2 = 1:1:4` -参数分别为起始值，公差和结束值
   * `a3 = linspace(1,1,4)`
3. 创建矩阵
   * `A = [1 2 3;5 9 6]`
   * `B = zeros(m,n)` - 创建m*n零矩阵
4. 数值格式化
   * `format short e` - 以5位有效数字加e+00的科学记数法表示
   * `format long e` - 以15位有效数字加e+00的科学记数法表示
   * `format rat` - 以分数表示
   * `format hex` - 以十六进制表示
   * `format bank` - 以元角分的方式定点表示

#### 绘图基础

1. 绘制二维图形

   `plot(x,y,'s')`

2. 绘制三维图形

   `plot3(x,y,z,'s')`

3. 多图绘制

   `subplot(m,n,k)` - 将窗口分割成n*m个绘图区域并选取第k个

#### 程序基础

1. 创建Matlab函数

   * 打开编辑窗口并建立M函数文件

   * 编写函数代码

     ```c
     function y = jie(x)
       y = 3*x+2*x^2+x+20;
     end
     ```

     

#### 工具箱

#### 参考资料

* 「数学实验与数学模型」
* 赛氪网
* 数学中国网

## Matlab应用基础