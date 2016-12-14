# 本章内容
1. 先复习了Servlet接口
2. HttpServer1
	+ 概述：将请求分为两部分，servlet请求与静态文件请求
	+ 主要内容：就是创建URLClassLoader，生成Servlet对象，并调用service方法
3. HttpServer2
	+ 概述：HttpServer1中存在一个问题，就是将Request于Response对象向上转型为ServletRequest与ServletResponse对象。
	+ 知道该实现，就可以在service中将对象强制转型为Request与Response，然后调用共有方法如request.parse与response.sendStaticResource
	+ 解决方法1：将方法的访问权限控制为默认类型，不是该包的程序不能调用
	+ 解决方法2：使用facade设计模式

# 需要解决问题
+ HttpServer1中的漏洞如何使用，举个例子