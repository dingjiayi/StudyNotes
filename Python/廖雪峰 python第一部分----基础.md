# ----第一部分：python基础---- #
## 1.1 python数据类型 ##
### 1.1.1 整数 ###
#### (1)  ####
	用//表示地板除，只保留整数部分
### 1.1.2 浮点数 ###
#### (1) 表示方法：小数表示，科学计数法 ####
### 1.1.3 字符串 ###
#### (1)表示方法 ####
	单引号或者双引号，比如 'ABC'  和 '\u0041\u0042\u0043' 都表示字符串 ABC
#### (2)转义 ####
    print("\\\t\\")  输出 \    \
	print(r"\\\t\\") 输出 \\\t\\
#### (3)多行内容 ####
    print('''A      |输出格式和 print("A\nB\n\C") 相同
	...B			|
	...C''')		|
#### （4）编码值和char的转换 ####
	ord('A') 输出 65 chr('中') 输出 20013 
#### （5） 字符串和 bytes的转换 ####
	'ABC'.encode("ascii") 输出 b'ABC' b'ABC'.decode('ascii') 输出 'ABC'
	'中国'.encode("utf-8") 输出 b'\xe4\xb8\xad\xe5\x9b\xbd' b'\xe4\xb8\xad\xe5\x9b\xbd'.decode('utf-8') 输出'中国'
#### （6）格式化输出 ####
	str = "Hello %s" % "World"    print(str)   输出 Hello World
### （7）字符替换 ###
	比如 a = "aaa", b = a.replace('a', 'A') ， a = 'aaa', b = 'AAA'
### 1.1.4 布尔值 ###
	只有True和False两种值
### 1.1.5 空值 None ###
### 1.1.4 list ###
#### (1) 格式 ####
	classmates = [""程俊", "caodiaosi", "shuji"]
#### （2） 索引 ####
	从0开始，附属表示倒数 classmates[-1] = 'shuji'
#### （3）追加元素 ####
	尾部加：classmates.append("jiahui")
	指定索引位置加：classmates.insert(0, "wujianying")
#### （4）删除元素 ####
	尾部删：calssmates.pop()
	指定索引位置删：classmates.pop(0)   删除wujianying
#### （5）替换 ####
	classmates[0] = "xxx"  将索引位置为0的元素替换为 xxx
#### （6）list 元素数据类型 ####
	可以不同，可以嵌套list
#### （7）排序函数 ####
	classmates.sort(0
### 1.1.5 tuple ###
#### 表示方法 ####
	t = (1, 2, 3)  t = ()  注意：t = (1)不是tuple， 二是整数1， t(1,)才是 tuple
#### 元素的变化 ####
	t = (1, 2, [31,32])  t[2][0] = 331       t[2][1] = 332  
	t = (1, 2, [331, 332])
### 1.1.6 dict ###
#### （1）格式 ####
	score = {"wujianying":100, "jiahui":99, "hongyu":98}
#### 判断key是否在score ####
	方法1： "huihui" in score   值为 False  "wujianying" in score 值为 True
	方法2：score.get("huihui") 值为 None  score.get("wujianying") 值为 100
### 1.1.7 set ###
#### （1）初始化方式 ####
	name = set(["juejue", "zhangjuan", "anan"])  ==>  name = {"juejue", "zhangjuan", "anan"}
#### （2）添加元素 ####
	name.add("xiaoqiang")    name.add("xiaoqiang")  可以重复添加，但是只加了一个
#### （3）删除元素 ####
	name.remove("xiaoqiang")
#### 集合的交集、并集 ####
	s1 = set([1,2,3,4])    s2 = set([3,4,5,6])
	s1 & s2 = {3,4}    s1 | s2 = {1,2,3,4,5,6}
## 1.2 python 循环 ##
### 1.2.1 for ... in ###
### 1.2.2 while ###
### 1.2.3 range ###
	range(n)产生从0, 到n-1的数组， range(100) = 0, 1, 2, 3,...,99