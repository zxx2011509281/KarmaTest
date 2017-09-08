

前端自动化测试工具--使用karma进行javascript单元测试
1、参考：

http://www.cnblogs.com/greatluoluo/p/5680738.html


2、怎么运行：
	在文件夹karma_init下
karma start karma.conf.js


3、使用
页面 点击debug,新页面F12，查看console

查看覆盖率进入文件夹coverage

4、jasmineAPI
http://www.cnblogs.com/kbqncf/p/3795155.html
	describe(string,function)

	全局函数，接收两个参数

	string:函数的描述

	function:测试组函数

	It(string,function)

	一个测试specs,接收两个参数

	string:spces的名称

	function:spces函数

	beforeEach(function)

	定义在一个describe的所有it执行前做的操作

	afterEach(function)

	定义在一个describe的所有it执行后做的操作

	toBe

	等同于===，比较变量

	toEqual

	处理变量，数组，对象等等

	toMatch

	使用正则式进行匹配

	toBeDefined

	是否已声明且赋值

	toBeUndefined

	是否未声明

	toBeNull

	是否null

	toBeTruthy   

	如果转换为布尔值，是否为true

	toBeFalsy    
	
	如果转换为布尔值，是否为false

	toContain   

	数组中是否包含元素（值）。只能用于数组，不能用于对象

	toBeLessThan   

	数值比较，小于

	toBeGreaterThan   

	数值比较，大于

	toBeCloseTo   

	数值比较时定义精度，先四舍五入后再比较

	toThrow    

	检验一个函数是否会抛出一个错误



	栗子：
		it("toThrow检验一个函数是否会抛出一个错误", function() {
			var foo = function() {
			  return 1 + 2;
			};
			var bar = function() {
			  return a + 1;
			};
			expect(foo).not.toThrow();
			expect(bar).toThrow();
		});


5、其他：

Karma init 用window自带工具启动，用Git Bash报错


