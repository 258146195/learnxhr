## ajax同源http策略
### XMLHttpRequest对象
### 常用的方法open('GET','URL',true,用户名,密码)
			 send()
			 onreadystatechange事件
			 readystate 准备状态
			 status 	状态码
			 JSON.parse() 用于接受response数据，转换成string数据
			 JSON.stringify() 用于把string转换成JSON格式数据，发送给请求主题


			 回调函数和事件升级为es6中promise对象解决方案
			 Promise，简单说就是一个容器，里面保存着某个未来才会结束的事件（通常是一个异步操作）的结果
			 	对象的状态不受外界影响。Promise对象代表一个异步操作，有三种状态：pending（进行中）、fulfilled（已成功）和rejected（已失败）
			 	一旦状态改变，就不会再变，任何时候都可以得到这个结果。Promise对象的状态改变，只有两种可能：从pending变为fulfilled和从pending变为rejected。只要这两种情况发生，状态就凝固了，不会再变了，会一直保持这个结果，这时就称为 resolved（已定型）
			 	如果改变已经发生了，你再对Promise对象添加回调函数，也会立即得到这个结果
			 有了Promise对象，就可以将异步操作以同步操作的流程表达出来，避免了层层嵌套的回调函数。此外，Promise对象提供统一的接口，使得控制异步操作更加容易
			 	Promise构造函数接受一个函数作为参数，该函数的两个参数分别是resolve和reject。它们是两个函数，由 JavaScript 引擎提供，不用自己部署

			 	固定套路
			 	const promise =new Promise(function(resolve,reject){
			 		if(resolve){
			 			resole(value)
			 		}else{
			 			reject(error)
			 		}
			 	})

			 	then方法可以接受两个回调函数作为参数
			 	promise.then(function(value){

			 	},function(error){})


			 	