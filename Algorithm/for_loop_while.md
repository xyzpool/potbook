#循环算法

##看待算法的两种视角：
	动态：算法由计算步骤组成
	静态：算法是由状态机的一系列快照的断言组成
	这两种视角相辅相承
	ex: max(a,b,c)

```flow
st=>start: 输入a,b,c三个参数,必须保证输入的参数是3个数字
e=>end: 返回max 保证返回的参数是a,b,c三个数字中最大的一个
op0=>operation: 动作1 m = a
op1=>condition: 动作2 m < b
op2=>operation: 动作3 m = b
op3=>condition: 动作4 m < c
op4=>operation: 动作5 m = c
state0=>operation: 状态1 max = max{a}
state1=>operation: 状态2 max = max{a,b}
state2=>operation: 状态3 max = max{a,b,c}

st->op0
op0->state0
state0->op1
op1(yes)->op2
op1(no)->state1
op2->state1
state1->op3
op3(yes)->op4
op4->state2
op3(no)->state2
state2->e
```

##循环算法的核心-循环不变式

##循环算法的结构

```
begin routine
		<pre-cond>	
		code(pre-loop) %Enstablish loop invariant
		loop
			<loop-invariant>
			exit when <exit-cond>
			code(loop) Make Progress while maintaining the loop invariant
		end loop
		code(post-loop) %Clean up loose ends
		<post-cond>
end routine
```

##循环算法的几个重点
###证明算法正确

###测量时间复杂度

###遵循思考范式
以你从家去上学作为例子

1. 算法目的
   需要从家去学校
2. 基本步骤
3. 可度量过程
4. 循环不变式
5. 主要步骤
6. 推进算法
7. 保持循环不变式
8. 使循环不变式成立
9. 循环不变式的退出条件
10. 返回结果
11. 算法完结和运行时长
12. 特殊情况
13. 编码和实现细节
14. 正式证明

------

例1:
查找最大值算法

1. 算法目的
2. 基本步骤
3. 可度量过程
4. 循环不变式
5. 主要步骤
6. 推进算法
7. 保持循环不变式
8. 使循环不变式成立
9. 循环不变式的退出条件
10. 返回结果
11. 算法完结和运行时长
12. 特殊情况
13. 编码和实现细节
14. 正式证明