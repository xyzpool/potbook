# Select Case When 

Mysql的Select When Case有按照值和表达式的两种使用方式:

### 第一种 按值区分：

```mysql
        CASE case_value
            WHEN when_value THEN statement_list
            [WHEN when_value THEN statement_list] ...
            [ELSE statement_list]
        END CASE

ex:
		CASE sex
			WHEN '1' THEN '男'
			WHEN '2' THEN '女'
			ELSE '其他' 
		END
```
### 第二种 按表达式区分：

```mysql
        CASE
            WHEN search_condition THEN statement_list
            [WHEN search_condition THEN statement_list] ...
            [ELSE statement_list]
        END CASE

ex:
		CASE 
	   		WHEN sex is null THEN '其他'  
			WHEN sex = '1' THEN '男' 
			WHEN sex = '2' THEN '女' 
			ELSE '不男不女' 
		END as sex 

```
