# 文件说明

a和b静态页面是演示 在同一个域中 a页面调用b页面的方法

# 跨域调用函数事件

>需求: 在a内面调用和a不在同一个域中的b页面的方法

方案一:在b的域下创建一个页面c,c页面里面调用b中方法,如果有多个事件,可以在iframe中src路径品入参数
详情见 a1,b1,c页面示例

方案二,使用h5中的postMessage()方法
在a页面中使用postMessage(msg,url)发送到b页面
在b页面window.addEventListener('message',function(){})添加message监听事件
根据不同消息值做出相应的函数调用
