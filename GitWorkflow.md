Git Workflow
Git工作流是由Vincent Driessen在2010年提出的Git协同工作的一个比较理想模型.
总流程图如下：
![Alt text](./1533793942970.png)

开发期中:
1.开发没有版本的概念，只分特性( feature )和开发主干( develop ).
	a. 特性针对于某一个与其他功能低耦合的功能点,开发期中所有的commit都提交到这个分支上.
	b. 开发主干分支用于合并已经开发完成的功能分支.
	//c. 特性分支的开发需要每天将develop最新的代码合并到本地（merge/rebase)
2.特性独立于版本