# Ajax
- 什么是Ajax
	Asynchronous JavaScript and XML（异步JavaScript和XML) 
	节省用户操作，时间，提高用户体验，减少数据请求
传输获取数据
使用Ajax
使用ajax获取某一文本文件的内容
Ajax过程详解
创建对象XMLHttpRequest()
Date()对象
ActiveXObject(‘Microsoft.XMLHTTP’)

Open方法
三个参数的含义
1、提交方式 Form-method
2、提交地址 Form-action
3、异步（同步）
Send方法
发送数据请求，相当于Form的submit

请求状态监控
onreadystatechange事件
readyState属性：请求状态
- 0	（未初始化）还没有调用open()方法
- 1	（载入）已调用send()方法，正在发送请求
- 2	（载入完成）send()方法完成，已收到全部响应内容
- 3	（解析）正在解析响应内容
- 4	（完成）响应内容解析完成，可以在客户端调用了
status属性：服务器(请求资源)的状态
返回的内容
responseText：返回以文本形式存放的内容
responseXML：返回XML形式的内容

发送请求(get和post的区别)
send(要发送的数据)：发送请求
中文编码
缓存
POST：setRequestHeader(类型, 内容)：设置请求头
"Content-Type","application/x-www-form-urlencoded”
数据类型(返回数据的处理)
服务器返回给咱们的真正数据
XML、HTML、JSON
JSON的写法
Eval解析JSON的时候需要注意的地方
JSON.parse() : 字符串解析成对象
