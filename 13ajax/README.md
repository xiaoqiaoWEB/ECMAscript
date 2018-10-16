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

---------------------------------------
#get 和 post 区别
- 1、Get是用来从服务器上获得数据，而Post是用来向服务器上传递数据。  
- 2、Get将表单中数据的按照variable=value的形式，添加到action所指向的URL后面，并且两者使用“?”连接，而各个变量之间使用 “&”连接；
	Post是将表单中的数据放在form的数据体中，按照变量和值相对应的方式，传递到action所指向URL。  
- 3、 Get是不安全的，因为在传输过程，数据被放在请求的URL中，而如今现有的很多服务器、代理服务器或者用户代理都会将请求URL记录到日志文件中，然后 放在某个地方，这样就可能会有一些隐私的信息被第三方看到。另外，用户也可以在浏览器上直接看到提交的数据，一些系统内部消息将会一同显示在用户面前。 Post的所有操作对用户来说都是不可见的。  
- 4、Get传输的数据量小，这主要是因为受URL长度限制；而Post可以传输大量的数据，所以在上传文件只能使用Post（当然还有一个原因，将在后面的提到）。  
- 5、Get限制Form表单的数据集的值必须为ASCII字符；而Post支持整个ISO10646字符集。  
- 6、Get是Form的默认方法。

#post和get传输的最大容量
- POST 根据你php.ini文件配置   
- GET的话 大小限制在2KB

 从理论上讲取决于浏览器和php.ini里的设置
 从实际上讲还要取决于网速和PHP超时时间

 ------------------------------------

 #Server-Sent 事件允许网页从服务器获得更新
var source = new EventSource("demo_sse.php");
source.onmessage = function(event) {
    document.getElementById("result").innerHTML += event.data + "<br>";
};

例子解释：
创建一个新的 EventSource 对象，然后规定发送更新的页面的 URL（本例中是 "demo_sse.php"）
每当接收到一次更新，就会发生 onmessage 事件
当 onmessage 事件发生时，把已接收的数据推入 id 为 "result" 的元素中
