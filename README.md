# nodejs_test
这是一个使用node.js上传JPG文件并显示在浏览器中的例子
运行命令
node index.js
可能存在的疑问，当在浏览器中输入http://localhost:8888/ 时，可以看到文件上传页面，这时实际上调用了start方法
那么是谁在调用upload方法呢？ 注意到start中form表单有一个action属性，其值为/upload 
另外show又是怎么调用的呢 ?upload中有一个src="/show" 依据http协议当浏览器发现网页中存在img文件时，会在发起一次连接请求此文件，此时show方法的得到调用
