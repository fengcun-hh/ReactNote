### React

![image](2CFFBDA91ADB4349B0DAC3C60E5A1641)

![image](24C2A555EC8A45C098694F39FED74063)

![image](707E5DFFCB554F3D9862899F1E54E74A)

![image](C0677BE3D8374A83A7735E48EBAC4098)

![image](BE279852F2204267B2455BF7286607E3)

---

### hello_react案例

先引入库文件。

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			
		</script>
	</body>
	</body>
</html>
```

React使用。

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 创建虚拟DOM
			const VDOM = <h1>hello react</h1>
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```
注意,重复渲染虚拟DOM时无效的。

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 创建虚拟DOM
			const VDOM1 = <h1>hello react</h1>
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));

			// 创建虚拟DOM
			const VDOM2 = <h1>hello react.</h1>
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM2, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

---

### JSX语法

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/javascript">
			// 创建虚拟DOM
			// 第一种方式创建虚拟DOM
			const VDOM1 = React.createElement("h1", {id: 'title'}, "hello react.")
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));

		</script>
	</body>
	</body>
</html>
```
JSX语法创建虚拟DOM更简单。
```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 创建虚拟DOM
			// 第二种方式创建虚拟DOM
			const VDOM1 = <h1>hello react.</h1>
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));

		</script>
	</body>
	</body>
</html>
```

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 创建虚拟DOM
			// 第二种方式创建虚拟DOM
			const VDOM1 = (
				<h1 id="title">
					<span>hello react.</span>
				</h1>
			)
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));

		</script>
	</body>
	</body>
</html>
```

---

### 虚拟DOM与真实DOM

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 创建虚拟DOM
			// 第二种方式创建虚拟DOM
			const VDOM1 = (
				<h1 id="title">
					<span>hello react.</span>
				</h1>
			)
			// 打印虚拟DOM
			console.log(VDOM1)
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));

		</script>
	</body>
	</body>
</html>
```

![image](97CACBE3C948401C951118F52F62F90E)

虚拟DOM本质是一个对象。

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 创建虚拟DOM
			// 第二种方式创建虚拟DOM
			const VDOM1 = (
				<h1 id="title">
					<span>hello react.</span>
				</h1>
			)
			// 打印虚拟DOM
			console.log(VDOM1)
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));
			// 打印真实DOM
			console.log(document.getElementById("test"))

		</script>
	</body>
	</body>
</html>
```

真实DOM是一个HTML元素。

![image](A58A4DDA51FA4F8F8B522140673F9825)

![image](713351568CC847AF9487914CC8238A47)

---

### JSX语法规则

![image](FE86F68F71CD46749FC1EB139298584B)

1、
```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			const VDOM = (
				<h1 id="title">
					<span>hello react.</span>
				</h1>
			)
			
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));
			

		</script>
	</body>
	</body>
</html>
```

2、
```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 定义变量
			const MyId = "react"
			const MyData = "hello react."
			// 插值语法
			const VDOM1 = (
				<h1 id={MyId}>
					<span>{MyData}</span>
				</h1>
			)
			
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));
			

		</script>
	</body>
	</body>
</html>
```

![image](5DADBA5766EE4411AF8264CD628C4F1A)

3、
```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			.title {
				color: red;
			}
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 定义变量
			const MyId = "react"
			const MyData = "hello react."
			// 插值语法
			const VDOM1 = (
				// 使用样式，增加class属性
				<h1 class="title" id={MyId}>
					<span>{MyData}</span>
				</h1>
			)
			
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));
			

		</script>
	</body>
	</body>
</html>
```

4、
```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			.title {
				color: red;
			}
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 定义变量
			const MyId = "react"
			const MyData = "hello react."
			// 插值语法
			const VDOM1 = (
				// 使用样式，增加class属性,需要写成className="类名"
				<h1 className="title" id={MyId}>
					<span>{MyData}</span>
				</h1>
			)
			
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));
			

		</script>
	</body>
	</body>
</html>
```

5、
```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 定义变量
			const MyId = "react"
			const MyData = "hello react."

			// span中使用style属性，后面的值必须这样写
			const VDOM1 = (
				<h1 id={MyId}>
					<span style={{color: "red", fontSize: '29px'}}>{MyData}</span>
				</h1>
			)
			
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

6、
```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 定义变量
			const MyId = "react"
			const MyData = "hello react."

			// VDOM中只能有一个根元素
			const VDOM1 = (
				<h1 id={MyId}>
					<span style={{color: "red", fontSize: '29px'}}>{MyData}</span>
				</h1>
				<input type="text">
			)
			
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

6、
```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 定义变量
			const MyId = "react"
			const MyData = "hello react."

			// VDOM中只能有一个根元素
			const VDOM1 = (
				<div>
					<h1 id={MyId}>
						<span style={{color: "red", fontSize: '29px'}}>{MyData}</span>
					</h1>
					<h1 id={MyId}>
						<span style={{color: "red", fontSize: '29px'}}>{MyData}</span>
					</h1>
				</div>

			)
			
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

7、
```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 定义变量
			const MyId = "react"
			const MyData = "hello react."

			// 虚拟DOM必须闭合
			const VDOM1 = (
				<div>
					<h1 id={MyId}>
						<span style={{color: "red", fontSize: '29px'}}>{MyData}</span>
					</h1>
					<h1 id={MyId}>
						<span style={{color: "red", fontSize: '29px'}}>{MyData}</span>
					</h1>
			)
			
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

8、
```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 定义变量
			const MyId = "react"
			const MyData = "hello react."

			// 不要书写未定义的标签
			const VDOM1 = (
				<div>
					<h1 id={MyId}>
						<span style={{color: "red", fontSize: '29px'}}>{MyData}</span>
					</h1>
					<h1 id={MyId}>
						<span style={{color: "red", fontSize: '29px'}}>{MyData}</span>
					</h1>
					<Good>123</Good>
			)
			
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

![image](8E41EED3078E4F61AECFC5E0956086A2)

总结：

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .sss{
            color: red;
        }
    </style>
</head>
<body>
    <!-- 准备好容器 -->
    <div id="test">
        
    </div>
</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>
<!--这里使用了js来创建虚拟DOM-->
<script type="text/babel">
        const MyId = "title";
        const MyData = "Cyk";
        // 1.创建虚拟DOM[在这使用了js的语法]React.createElement(标签,标签属性,内容)
        const VDOM = (
            <h1 id = {MyId.toLocaleUpperCase()}>
                <span className = "sss" style = {{fontSize:'50px'}}>sss</span>   
                
            </h1>
        )
        // 2.渲染，如果有多个渲染同一个容器，后面的会将前面的覆盖掉
        ReactDOM.render(VDOM,document.getElementById("test"));
        
        /*
        JS表达式：返回一个值，可以放在任何一个需要值的地方  a  a+b  demo(a)  arr.map() function text(){}
        JS语句：if(){} for(){} while(){} swith(){} 不会返回一个值
        */

        //1.定义虚拟DOM，不能使用“”
        //2.标签中混入JS表达式的时候使用{}
        //3.样式的类名指定不要使用class，使用className
        //4.内敛样式要使用style={{样式:"值"}}
        //5.不能有多个根标签，只能有一个跟标签
        //6.标签必须闭合
        //7.如果小写字母开头，就将标签转化为html同名元素，如果html中无该标签对应的元素，就报错
        // 如果是大写字母开头，react就去渲染对应的组件，如果没有就报错
</script>

</html>
```

---

### JSX练习

列表渲染。

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 不要书写未定义的标签
			const VDOM1 = (
				<div>
					<h1>前端</h1>
					<ul>
						<li>Angular</li>
						<li>React</li>
						<li>Vue</li>
					</ul>
				</div>
			)
			
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			const obj = ['Angular', 'React', 'Vue']
			// 不要书写未定义的标签
			const VDOM1 = (
				<div>
					<h1>前端</h1>
					<ul>
						{obj}
					</ul>
				</div>
			)
			
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

![image](C235138386044D79B4811BF18DC48527)

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			const obj = ['Angular', 'React', 'Vue']
			// 注意React的{}中只能写JS表达式，不可以是JS语句
			const VDOM1 = (
				<div>
					<h1>前端</h1>
					<ul>
						{
							if() {
								
							}
						}
					</ul>
				</div>
			)
			
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

![image](37A27752B5444EDE876C99427684E427)

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			const obj = ['Angular', 'React', 'Vue']
			// 注意React的{}中只能写JS表达式，不可以是JS语句
			const VDOM1 = (
				<div>
					<h1>前端</h1>
					<ul>
						{
							obj.map((item, index) => {
								return <li key={index}>{item}</li>
							})
						}
					</ul>
				</div>
			)
			
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(VDOM1, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

---

### 模块与组件

![image](09B4F8F39BA244868D1F0D918B72ED6A)

为什么需要组件？

复用代码，简化页面复杂度。

---

### 面向组件编程-函数式组件

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 定义函数式组件
			function demo() {
				return <h2>hello react.</h2>
			}		
			
			// 将虚拟DOM渲染到页面上
			// demo()这种写法对的
			// 也可以使用<demo/>这种写法
			ReactDOM.render(demo(), document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

注意：遇到<Demo/>时，由于不是浏览器定义的标签，因此，会把Demo标签看作一个组件，因此，回去执行Demo函数，返回虚拟DOM。

react开发者工具的可视化节目。

![image](468955533C5B4DD7B6A8DB12045C6F80)

![image](72D8DEB57C62403087AFC4620C60D0D4)

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 定义函数式组件
			// 1、是一个函数
			// 2、react帮我们调用的
			function Demo() {
				return <h2>hello react.</h2>
			}		
			
			// 将虚拟DOM渲染到页面上
			ReactDOM.render(<Demo/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 准备好容器 -->
    <div id="test">

    </div>
</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js" type="text/javascript"></script>


<!--这里使用了babel用来解析jsx语法-->
<script type="text/babel">
        // 1.创建类式组件 [必须继承React.Component]
        class MyComponent extends React.Component{
            render(){
                //render是放在原型对象上的，供实例对象使用
                //render的this，MyComponent的实例对象【组件实例对象】
                return <h1>这个是类组件</h1>
            }
        }
        
        //2.渲染组件
        ReactDOM.render(<MyComponent />,document.getElementById("test"))

       

       //执行过程：
       //1.React解析组件标签，找到相应的组件
       //2.发现组件是类定义的，随后new出来的类的实例，并通过该实例调用到原型上的render方法
       //3.将render返回的虚拟DOM转化为真实的DOM,随后呈现在页面中


       //复杂组件：有状态的
       //简单组件：没有状态的
       //组件的状态里面保存着数据 state
</script>
</html>
```

函数组件实例：

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .show{
            font-size: 50px;
        }
    </style>
</head>
<body>
    <!-- 准备好容器 -->
    <div id="test">

    </div>
</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js" type="text/javascript"></script>


<!--这里使用了babel用来解析jsx语法-->
<script type="text/babel">

        function Did(){
            return <div>
                        这是个输入框：<input value = "我是你爹" className = "show" readOnly/>
                    </div>
        }
        //2.渲染组件
        ReactDOM.render(<Did />,document.getElementById("test"))

</script>
</html>
```

---

### 面向对象复习

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <script>
        
      class Person {
        constructor(name, age) {
          this.name = name;
          this.age = age;
        }
        speak() {
          console.log(this.name + "speak" + this.age);
        }
      }

      let p1 = new Person("tom", 12);
      p1.speak();
      console.log(p1);

      let p2 = new Person("jack", 18);
      p2.speak();
      console.log(p2);
    </script>
  </body>
</html>
```

继承

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <script>
      class Person {
        constructor(name, age) {
          this.name = name;
          this.age = age;
        }
        speak() {
          console.log(this.name + "speak" + this.age);
        }
      }

      // 继承
      class student extends Person {
        constructor(name, age, className) {
          super(name, age);
          this.className = className;
        }
        study() {
          console.log("study");
        }
      }

      let p1 = new student("tom", 12, "高一");
      p1.speak();
      p1.study();
      console.log(p1);

      let p2 = new student("jack", 18, "高二");
      p2.speak();
      p2.study();
      console.log(p2);
    </script>
  </body>
</html>
```



![image](8D650E7533F94CB386369942550B8090)

---

### 类式组件

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 类组件
			// 1、render函数在类的原型对象，让实例使用
			class MyComponent extends React.Component {
				render() {
				    console.log(this)
					return <h2>hello react.</h2>
				}
			}
			
			// 将虚拟DOM渲染到页面上
			// React自动new MyComponent()并调用render函数
			ReactDOM.render(<MyComponent/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

![image](F9B04FD6526B423F8BD5FB22A6F6B74D)

实例

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 准备好容器 -->
    <div id="test">

    </div>
</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js" type="text/javascript"></script>


<!--这里使用了babel用来解析jsx语法-->
<script type="text/babel">
        // 1.创建类式组件 [必须继承React.Component]
        class MyComponent extends React.Component{
            render(){
                //render是放在原型对象上的，供实例对象使用
                //render的this，MyComponent的实例对象【组件实例对象】
                return <h1>这个是类组件</h1>
            }
        }
        
        //2.渲染组件
        ReactDOM.render(<MyComponent />,document.getElementById("test"))

       

       //执行过程：
       //1.React解析组件标签，找到相应的组件
       //2.发现组件是类定义的，随后new出来的类的实例，并通过该实例调用到原型上的render方法
       //3.将render返回的虚拟DOM转化为真实的DOM,随后呈现在页面中


       //复杂组件：有状态的
       //简单组件：没有状态的
       //组件的状态里面保存着数据 state
</script>
</html>
```

嵌套组件的使用

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 准备好容器 -->
    <div id="test">

    </div>
</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js" type="text/javascript"></script>


<!--这里使用了babel用来解析jsx语法-->
<script type="text/babel">

        //创建一个组件<li>
        function GetLi(props){      
            return <li>{props.value}</li>
        };

        // 1.创建类式组件<ul>
        class MyComponent extends React.Component{
            render(){
                console.log(this.props.arr);
                let com = this.props.arr.map((item,index)=>
                        <GetLi value={item} key = {index} />
                    );
                console.log(com);
                return <ul>{com}</ul>
            }
        }
        
        let num = [1,2,3,4]
        //2.渲染组件
        ReactDOM.render(<MyComponent  arr={num}/>,document.getElementById("test"))

    
</script>
</html>
```

---

### state理解

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 类组件
			// 1、render函数在类的原型对象，让实例使用
			class MyComponent extends React.Component {
				constructor(props) {
					super(props);
					// 初始化state状态
					this.state = {isHot: true};
				}
				render() {
					return <h2>今天天气{this.state.isHot ? '炎热' : '凉爽'}</h2>
				}
			}
			
			// 将虚拟DOM渲染到页面上
			// React自动new MyComponent()并调用render函数
			ReactDOM.render(<MyComponent/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

---

### 事件绑定

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 类组件
			// 1、render函数在类的原型对象，让实例使用
			class MyComponent extends React.Component {
				constructor(props) {
					super(props);
					// 初始化state状态
					this.state = {isHot: true};
				}
				render() {
					return <h2 id="title">今天天气{this.state.isHot ? '炎热' : '凉爽'}</h2>
				}
			}
			
			// 将虚拟DOM渲染到页面上
			// React自动new MyComponent()并调用render函数
			ReactDOM.render(<MyComponent/>, document.getElementById("test"));

			const title = document.getElementById("title");
			title.addEventListener("click", () => {
				console.log("很凉爽")
			})
		</script>
	</body>
	</body>
</html>
```

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 类组件
			// 1、render函数在类的原型对象，让实例使用
			class MyComponent extends React.Component {
				constructor(props) {
					super(props);
					// 初始化state状态
					this.state = {isHot: true};
				}
				render() {
					return <h2 id="title" onClick={demo}>今天天气{this.state.isHot ? '炎热' : '凉爽'}</h2>
				}
			}
			function demo() {
				console.log("hello react.")
			}
			
			// 将虚拟DOM渲染到页面上
			// React自动new MyComponent()并调用render函数
			ReactDOM.render(<MyComponent/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

---

### 类中方法的this

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			// 类组件
			// 1、render函数在类的原型对象，让实例使用
			class MyComponent extends React.Component {
				constructor(props) {
					super(props);
					// 初始化state状态
					this.state = {isHot: true};
				}
				render() {
					return <h2 id="title" onClick={demo}>今天天气{this.state.isHot ? '炎热' : '凉爽'}</h2>
				}
			}
			function demo() {
				console.log("hello react.")
				console.log(this) // undefined
			}
			
			// 将虚拟DOM渲染到页面上
			// React自动new MyComponent()并调用render函数
			ReactDOM.render(<MyComponent/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
		    // 获取实例对象
			let that;
			class MyComponent extends React.Component {
				constructor(props) {
					super(props);
					// 初始化state状态
					this.state = {isHot: true};
					that = this
				}
				render() {
					return <h2 id="title" onClick={demo}>今天天气{this.state.isHot ? '炎热' : '凉爽'}</h2>
				}

			}
			function demo() {
				console.log(that.state.isHot)
				// 直接修改state，但此时页面不会更新
				that.state.isHot = !that.state.isHot
			}
			
			// 将虚拟DOM渲染到页面上
			// React自动new MyComponent()并调用render函数
			ReactDOM.render(<MyComponent/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			class MyComponent extends React.Component {
				constructor(props) {
					super(props);
					// 初始化state状态
					this.state = {isHot: true};
					// 绑定this
					this.changeWeather = this.changeWeather.bind(this)
				}
				render() {
					return <h2 id="title" onClick={this.changeWeather}>今天天气{this.state.isHot ? '炎热' : '凉爽'}</h2>
				}
				changeWeather() {
					// changeWeather不是通过实例调用,而是直接changeWeather()这样进行调用
					console.log(this)
				}
			}

			
			// 将虚拟DOM渲染到页面上
			// React自动new MyComponent()并调用render函数
			ReactDOM.render(<MyComponent/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

---

### setState使用

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			class MyComponent extends React.Component {
				constructor(props) {
					super(props);
					// 初始化state状态
					this.state = {isHot: true};
					// 绑定this
					this.changeWeather = this.changeWeather.bind(this)
				}
				render() {
					return <h2 id="title" onClick={this.changeWeather}>今天天气{this.state.isHot ? '炎热' : '凉爽'}</h2>
				}
				changeWeather() {
					// 改变state，但是页面无法更新
					const isHot = this.state.isHot;
					this.state.isHot = !isHot;
				}
			}

			
			// 将虚拟DOM渲染到页面上
			// React自动new MyComponent()并调用render函数
			ReactDOM.render(<MyComponent/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			class MyComponent extends React.Component {
				constructor(props) {
					super(props);
					// 初始化state状态
					this.state = {isHot: true};
					// 绑定this
					this.changeWeather = this.changeWeather.bind(this)
				}
				render() {
					return <h2 id="title" onClick={this.changeWeather}>今天天气{this.state.isHot ? '炎热' : '凉爽'}</h2>
				}
				changeWeather() {
					const isHot = this.state.isHot;
					// 更新state
					this.setState({isHot: !isHot})
					// state更新重新执行render函数
				}
			}

			
			// 将虚拟DOM渲染到页面上
			// React自动new MyComponent()并调用render函数
			ReactDOM.render(<MyComponent/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

https://www.bilibili.com/video/BV1wy4y1D7JT?p=17

---

### state简写形式

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			class MyComponent extends React.Component {
				constructor(props) {
					super(props);
				}
				// 初始化状态
				// 这样实例对象上有state属性
				state = {isHot: true};
				render() {
					return <h2 id="title" onClick={this.changeWeather}>今天天气{this.state.isHot ? '炎热' : '凉爽'}</h2>
				}
				// 自定义方法
				// 此时，实例对象有一个changeWeather属性，可以通过this调用
				changeWeather = () => {
					const isHot = this.state.isHot;
					// 更新state
					this.setState({isHot: !isHot})
					// state更新重新执行render函数
				}
			}

			// 将虚拟DOM渲染到页面上
			// React自动new MyComponent()并调用render函数
			ReactDOM.render(<MyComponent/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

---

### state总结

![image](6A9470910C094D66A77CAE99614A2AFC)

一个案例

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 准备好容器 -->
    <div id="test">
        
    </div>
</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<script type="text/babel">
       
       //定义一个父组件
       class Father extends React.Component{
            state = {du:""}
            render(){
                // 将state中的值作为props传递给Hua组件
                return (<form>
                        <Hua value = {this.state.du}/>
                        <Hua value = {this.state.du}/>
                    </form>)
            }
       }
        //定义华摄氏度组件
        class Hua{
            render(){
                return <input 
                    name="温度"
                    type="text"
                    onChange={this.handleInputChange}
                    />
            }
        }
        ReactDOM.render(<Father  />,document.getElementById("test"));
</script>
</html>
```

---

### props使用

![image](22BA1951068049B0A4F26192B7DCE27F)

![image](6C72C11FEFBA4A7AA27C1C83BA303641)

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			class MyComponent extends React.Component {
				constructor(props) {
					super(props);
					console.log(this)
				}
				
				render() {
					return <h2 id="title">{this.props.name}{this.props.age}</h2>
				}
			}

			// 将虚拟DOM渲染到页面上
			// React自动new MyComponent()并调用render函数
			ReactDOM.render(<MyComponent name="tom" age="18"/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

---

### 批量传递props

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>

		<script type="text/babel">
			class MyComponent extends React.Component {
				constructor(props) {
					super(props);
					console.log(this)
				}
				
				render() {
					return <h2 id="title">{this.props.name}{this.props.age}</h2>
				}
			}

			const obj = {name: "tom", age: "18"}
			// 批量传递props
			ReactDOM.render(<MyComponent {...obj}/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>

</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">

    
    function Person(props){
          return (
                <ul>
                    <li>{props.name}</li>
                    <li>{props.age}</li>
                    <li>{props.sex}</li>
                </ul>
            )
    }
    
    //在js中可以使用{...p}来复制一个对象，但是这个地方并不是复制对象，而是babel+react通过展开运算符，展开了一个对象
    //但是只能在标签中进行使用
    //const p = {name:"张三",age:"18",sex:"女"}   {14}就代表的是数值
    ReactDOM.render(<Person name="sss" age = {14} speak="8"/>,document.getElementById("div"));
    //ReactDOM.render(<Person {...p}/>,document.getElementById("div"));

    function speak(){
        console.log("这个是一个函数")
    }

</script>
</html>
```

---

### 对props进行限制

![image](1BCE6917FCC54FD1A99E2E2518DC1F3F)

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>
		<script type="text/javascript" src="./js/prop-types.js"></script>

		<script type="text/babel">
			class MyComponent extends React.Component {
				constructor(props) {
					super(props);
					console.log(this)
				}
				
				render() {
					return <h2 id="title">{this.props.name}{this.props.age}</h2>
				}
			}
			// 对props属性的类型进行限制
			MyComponent.propTypes = {
			    // 限制传递给该组件中name属性必须为String类型
				name: PropTypes.string.isRequired
			}

			const obj = {name: 11, age: "18"}
			// 批量传递props
			ReactDOM.render(<MyComponent {...obj}/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

---

### props简写写法

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>
		<script type="text/javascript" src="./js/prop-types.js"></script>

		<script type="text/babel">
			class MyComponent extends React.Component {
				constructor(props) {
					super(props);
					// props属性是只读的
					// 不可进行修改
					this.props.name = "mike"
				}
				
				render() {
					return <h2 id="title">{this.props.name}{this.props.age}</h2>
				}
			}

			const obj = {name: 11, age: "18"}
			// 批量传递props
			ReactDOM.render(<MyComponent {...obj}/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>
		<script type="text/javascript" src="./js/prop-types.js"></script>

		<script type="text/babel">
			class MyComponent extends React.Component {
				constructor(props) {
					super(props);
				}
				// 给props属性值添加限制
				static propTypes = {
					name: PropTypes.string,
					sex: PropTypes.string,
					age: PropTypes.number
				}
				
				render() {
					return <h2 id="title">{this.props.name}{this.props.age}</h2>
				}
			}

			const obj = {name: 'mike', age: 18}
			// 批量传递props
			ReactDOM.render(<MyComponent {...obj}/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>

</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">

    
    class Person extends React.Component{
        render(){
            //props是只读的
            return (
                <ul>
                    <li>{this.props.name}</li>
                    <li>{this.props.age}</li>
                    <li>{this.props.sex}</li>
                </ul>
            )
        }
        //对组件的属性对其进行限制
        static propTypes = {
            name:PropTypes.string.isRequired,
            sex:PropTypes.string,
            speak:PropTypes.func
        }
        //指定默认的标签属性
        static defaultProps = {
            sex:"不男不女",
            age:18
        }   
        
    }
    
   
    
    //在js中可以使用{...p}来复制一个对象，但是这个地方并不是复制对象，而是babel+react通过展开运算符，展开了一个对象
    //但是只能在标签中进行使用
    //const p = {name:"张三",age:"18",sex:"女"}   {14}就代表的是数值
    ReactDOM.render(<Person name="sss" age = {14} speak="8"/>,document.getElementById("div"));
    //ReactDOM.render(<Person {...p}/>,document.getElementById("div"));

    function speak(){
        console.log("这个是一个函数")
    }

</script>
</html>
```

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>

</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">

    
    class Person extends React.Component{
        render(){
            //props是只读的
            return (
                <ul>
                    <li>{this.props.name}</li>
                    <li>{this.props.age}</li>
                    <li>{this.props.sex}</li>
                </ul>
            )
        }
    }
    //对组件的属性对其进行限制
    Person.propTypes = {
        name:PropTypes.string.isRequired,
        sex:PropTypes.string,
        speak:PropTypes.func
    }
    //指定默认的标签属性
    Person.defaultProps = {
        sex:"不男不女",
        age:18
    }
    //在js中可以使用{...p}来复制一个对象，但是这个地方并不是复制对象，而是babel+react通过展开运算符，展开了一个对象
    //但是只能在标签中进行使用
    //const p = {name:"张三",age:"18",sex:"女"}   {14}就代表的是数值
    ReactDOM.render(<Person name="sss" age = {14} speak="8"/>,document.getElementById("div"));
    //ReactDOM.render(<Person {...p}/>,document.getElementById("div"));

    function speak(){
        console.log("这个是一个函数")
    }

</script>
</html>
```

---

### 类组件中构造器

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <div id="div"></div>
  </body>
  <!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
  <script
    src="../React-js/react.development.js"
    type="text/javascript"
  ></script>
  <script
    src="../React-js/react-dom.development.js"
    type="text/javascript"
  ></script>

  <script src="../React-js/babel.min.js"></script>

  <script type="text/babel">
    class Person extends React.Component {
      // 如果不写构造器，React自动将传入的props属性放在实例对象上
      render() {
        console.log(this)
        return (
          <ul>
            <li>{this.props.name}</li>
            <li>{this.props.age}</li>
            <li>{this.props.sex}</li>
          </ul>
        );
      }
    }

    const p = { name: "张三", age: "18", sex: "女" };
    ReactDOM.render(<Person {...p} />, document.getElementById("div"));
  </script>
</html>
```

截图

![image](D2C23C31FBA04042BE5E82962C74775B)

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <div id="div"></div>
  </body>
  <!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
  <script
    src="../React-js/react.development.js"
    type="text/javascript"
  ></script>
  <script
    src="../React-js/react-dom.development.js"
    type="text/javascript"
  ></script>

  <script src="../React-js/babel.min.js"></script>

  <script type="text/babel">
    class Person extends React.Component {
      // 类组件中写了构造器函数，必须在构造器中调用super函数
      // 如果constructor中没有接收props,也没有super(props)，此时this.props为undefined
      constructor() {
        super()
        console.log(this.props)
      }
      render() {
        return (
          <ul>
            <li>{this.props.name}</li>
            <li>{this.props.age}</li>
            <li>{this.props.sex}</li>
          </ul>
        );
      }
    }

    const p = { name: "张三", age: "18", sex: "女" };
    ReactDOM.render(<Person {...p} />, document.getElementById("div"));
  </script>
</html>
```

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <div id="div"></div>
  </body>
  <!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
  <script
    src="../React-js/react.development.js"
    type="text/javascript"
  ></script>
  <script
    src="../React-js/react-dom.development.js"
    type="text/javascript"
  ></script>

  <script src="../React-js/babel.min.js"></script>

  <script type="text/babel">
    class Person extends React.Component {
      // 类组件中写了构造器函数，必须在构造器中调用super函数
      // 接收props推荐写法
      constructor(props) {
        super(props)
        console.log(this.props)
      }
      render() {
        return (
          <ul>
            <li>{this.props.name}</li>
            <li>{this.props.age}</li>
            <li>{this.props.sex}</li>
          </ul>
        );
      }
    }

    const p = { name: "张三", age: "18", sex: "女" };
    ReactDOM.render(<Person {...p} />, document.getElementById("div"));
  </script>
</html>
```

---

### 函数式组件使用props

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>
		<script type="text/javascript" src="./js/prop-types.js"></script>

		<script type="text/babel">
			
			function MyComponent(props) {
				// 接收传入的props
				console.log(props)
				// 使用传入的props
				return <h1>{props.name}</h1>
			}
			// 限制函数组件中传入参数的类型
			MyComponent.propTypes = {
				name: PropTypes.string
			}
 			
			// 批量传递props
			ReactDOM.render(<MyComponent name="mike"/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

---

### 总结props

![image](E8C42157826C4C43A048D109340D2B95)

![image](03D2FEE6DFE64D749C8B3CE36D7A1185)

![image](EDAA9BB2094D4F72AD3A1A310BE89271)

https://www.bilibili.com/video/BV1wy4y1D7JT?p=26

---

### ref

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>
		<script type="text/javascript" src="./js/prop-types.js"></script>

		<script type="text/babel">
			class Demo extends React.Component {
				showData = () => {
					alert(this.refs.input.value)
				}
				showTip = () => {
					alert(this.refs.inputText.value)
				}
				// ref属性，给组件中标签打标识

				render() {
					return (
						<div>
							<input type="text" ref="input"/>
							<button onClick={this.showData}>点我展示左侧的数据</button>
							<input ref="inputText" onBlur={this.showTip} type="text" placeholder="失去焦点提示数据"/>
						</div>
					)
				}
			}
			
 			
			// 批量传递props
			ReactDOM.render(<Demo/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

---

### 回调形式的ref

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>
		<script type="text/javascript" src="./js/prop-types.js"></script>

		<script type="text/babel">
			class Demo extends React.Component {
				showData = () => {
					alert(this.input1.value)
				}
				showTip = () => {
					alert(this.input2.value)
				}
				// 回调ref
				render() {
					return (
						<div>
							<input type="text" ref={ Node => {this.input1 = Node}}/>
							<button onClick={this.showData}>点我展示左侧的数据</button>
							<input ref={Node => {this.input2 = Node}} onBlur={this.showTip} type="text" placeholder="失去焦点提示数据"/>
						</div>
					)
				}
			}
			
			// 批量传递props
			ReactDOM.render(<Demo/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>

</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">

    class Dom extends React.Component{

        state = {isHot:true};
        render(){
            //回调形式的ref 在ref中执行回调函数，将自身作为参数传递给回调函数
            return (
                <div>
                    // 回调函数中传入的参数代表这个html元素
                    <input ref={self =>{ this.dian = self;console.log(self)}} type="text" placeholder="点击弹出" />
                </div>
            )
        }
    }

    ReactDOM.render(<Dom />,document.getElementById("div"));

</script>
</html>
```

---

### 回调ref执行

![image](A98663C3FEE54F798C84681185000F90)

回调ref执行次数

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>

</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">

    class Dom extends React.Component{

        state = {isHot:true};
        render(){
            //回调形式的ref 在ref中执行回调函数，将自身作为参数传递给回调函数
            // 推荐写法
            return (
                <div>
                    // render组件时调用一次ref中的回调函数
                    // 每一次数据更新，页面重新渲染时都会重新调用ref中的回调函数
                    <input ref={self =>{ this.dian = self;console.log(this)}} type="text" placeholder="点击弹出" />
                </div>
            )
        }
    }

    ReactDOM.render(<Dom />,document.getElementById("div"));

</script>
</html>
```

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>

</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">

    class Dom extends React.Component{

        state = {isHot:true};
        getInputDom = (self) => {
            // this代表组件实例
            console.log(this)
            // self代表绑定的html元素本身
            this.inputDom = self
        }
        render(){
            //回调形式的ref 在ref中执行回调函数，将自身作为参数传递给回调函数
            return (
                <div>
                    // render组件时调用一次ref中的回调函数
                    // 每一次数据更新，页面重新渲染时都会重新调用ref中的回调函数
                    // ref的回调函数写成类绑定的形式
                    <input ref={this.getInputDom} type="text" placeholder="点击弹出" />
                </div>
            )
        }
    }

    ReactDOM.render(<Dom />,document.getElementById("div"));

</script>
</html>
```

---

### createRef函数

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>

</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">

    class Dom extends React.Component{
        //通过API，创建React的容器，相当于对于回调函数创建了一个相应的API，省略了中间环节
        //但是这个容器是专门专用的，所以每一个ref都需要创建这个
        MyRef = React.createRef();
        MyRef1 = React.createRef();
        
        btnOnClick = () =>{
            //创建之后，将自身节点，传入current中
            console.log(this.MyRef.current.value);
        }
        inputBlur = () =>{
            console.log(this);
        }
        render(){
            return (
                <div>
                    // ref={this.MyRef}代表把ref绑定的Dom放入this.MyRef中
                    <input ref={this.MyRef} type="text" placeholder="点击弹出" />&nbsp;
                    <button onClick = {this.btnOnClick}>点击</button>&nbsp;
                    <input ref={this.MyRef1} onBlur={this.inputBlur} type="text" placeholder="失去焦点弹出弹出" />
                </div>
            )
        }
    }

    ReactDOM.render(<Dom />,document.getElementById("div"));

</script>
</html>
```

---

### jsx中写注释

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>

</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">

    class Dom extends React.Component{
        render(){
            return (
                <div>
                    {/* 注释 */}
                </div>
            )
        }
    }

    ReactDOM.render(<Dom />,document.getElementById("div"));

</script>
</html>
```

---

### 总结Ref

https://www.bilibili.com/video/BV1wy4y1D7JT?p=31

---

### 事件处理

![image](B951F7749065487191028B71902779EF)

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>

</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">

    class Dom extends React.Component{
        /*
            React的事件是通过onXxx属性指定事件处理函数
                React使用的都是自定义的时间，而不是原生的事件
                React中的事件是通过事件委托方式处理的
            通过event.target得到发生事件的Dom元素对象
        */

        //通过API，创建React的容器，相当于对于回调函数创建了一个相应的API，省略了中间环节
        //但是这个容器是专门专用的，所以每一个ref都需要创建这个
        //官方提示我们不要过度的使用ref，如果发生时间的元素刚好是需要操作的元素，就可以使用事件去替代。
        MyRef = React.createRef();
        MyRef1 = React.createRef();
        
        // event代表事件对象
        btnOnClick = (event) =>{
            console.log(event)
            //创建之后，将自身节点，传入current中
            console.log(this.MyRef.current.value);
            //alert(this.refs.dian.value);
        }

        // event代表事件对象
        inputBlur = (event) =>{
            console.log(event)
            console.log(this.MyRef1.current.value);
        }
        render(){
            return (
                <div>
                    <input ref={this.MyRef} type="text" placeholder="点击弹出" />&nbsp;
                    <button onClick = {this.btnOnClick}>点击</button>&nbsp;
                    <input ref={this.MyRef1} onBlur={this.inputBlur} type="text" placeholder="失去焦点弹出弹出" />
                </div>
            )
        }
    }

    ReactDOM.render(<Dom />,document.getElementById("div"));

</script>
</html>
```

---

### 非受控组件

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>
		<script type="text/javascript" src="./js/prop-types.js"></script>

		<script type="text/babel">
			class Demo extends React.Component {
				handelSubmit = (e) => {
					// 阻止事件默认行为
					e.preventDefault()
					const {userName, password} = this
					alert(`${userName.value} ${password.value}`)
				}
				render() {
					return (
						<form action="" onSubmit={this.handelSubmit}>
							用户名：<input type="text" ref={c => this.userName = c} />
							密码：<input type="password" ref={c => this.password = c} />
							<button>登录</button>
						</form>
					)
				}
			}
			
 			
			// 批量传递props
			ReactDOM.render(<Demo/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>

</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">

/*
    页面中所有的输入数据都是现用现取的，就是非受控的组件
*/

    class Login extends React.Component{

        login = (event) =>{
            event.preventDefault(); //阻止表单提交
            console.log(this.name.value);
            console.log(this.pwd.value);
        }
        render() {
            return (
                <form action="http://www.baidu.com" onSubmit={this.login}>
                    用户名：<input ref = {self => this.name =self } type = "text" name ="username"/>
                    密码<input ref = {self => this.pwd =self } type = "password" name ="password"/>
                    <button>登录</button>
                </form>
            )
        }
    }

    ReactDOM.render(<Login />,document.getElementById("div"));
</script>
</html>
```

---

### 受控组件

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>

</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">

/*
    受控制组件，就是使用事件和state,输入类的组件，就是将内容绑定到state中的，在使用的时候使用state里面的   
*/

    class Login extends React.Component{

        state = {name:"",pwd:""};

        saveName = (event) =>{
            this.setState({name:event.target.value});
        }

        savePwd = (event) => {
            this.setState({pwd:event.target.value});
        }

        render() {
            return (
                <form action="http://www.baidu.com" onSubmit={this.login}>
                    用户名：<input onChange={this.saveName} type = "text" name ="username"/>
                    密码<input onChange={this.savePwd} type = "password" name ="password"/>
                    <button>登录</button>
                </form>
            )
        }
    }

    ReactDOM.render(<Login />,document.getElementById("div"));
</script>
</html>
```

---

### 高阶函数

![image](9455ACE962824F1AB4E863693EBB45C2)

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			
		</style>
	</head>
	<body>
		<div id="test"></div>

		<!-- 引入react核心库 -->
		<script type="text/javascript" src="./js/react.development.js"></script>
		<!-- 引入react-dom，用于支持react操作DOM -->
		<script type="text/javascript" src="./js/react-dom.development.js"></script>
		<!-- 引入babel，用于将jsx转为js -->
		<script type="text/javascript" src="./js/babel.min.js"></script>
		<script type="text/javascript" src="./js/prop-types.js"></script>

		<script type="text/babel">
			class Demo extends React.Component {
				state = {
					userName: '',
					password: ''
				}
				handelSubmit = (e) => {
					// 阻止事件默认行为
					e.preventDefault()
					const {userName, password} = this.state
					alert(userName)
				}
				// 高阶函数
				saveFormData(dataType) {
					return (event) => {
						this.setState({dataType: event.target.value})
					}
				}
				render() {
					return (
						<form action="" onSubmit={this.handelSubmit}>
							用户名：<input onChange={this.saveFormData('userName')} type="text"/>
							密码：<input onChange={this.saveFormData("password")} type="password" />
							<button>登录</button>
						</form>
					)
				}
			}
			
 			
			// 批量传递props
			ReactDOM.render(<Demo/>, document.getElementById("test"));
		</script>
	</body>
	</body>
</html>
```

---

### 不用柯里化实现

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>

</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">

/*
    高级函数：
    1.如果函数的参数是函数
    2.如果函数返回一个函数
    函数的珂里化：
    通过函数调用继续返回函数的方式，实现多次接收参数最后统一处理的函数编码形式
*/

    class Login extends React.Component{

        login = (event) =>{
            event.preventDefault(); //阻止表单提交
            console.log(this.name.value);
            console.log(this.pwd.value);
        }
 
        state = {name:"",pwd:""};

        // 非柯里化写法
        saveType = (type,event) =>{
            this.setState({type:event.target.value});
        }

        
        //因为事件中必须是一个函数，所以返回的也是一个函数，这样就符合规范了
        render() {
            return (
                <form action="http://www.baidu.com" >
                    用户名：<input onChange = {this.saveType('name')} type = "text" name ="username"/>
                    {/*直接调用回调函数也是可以的：将数据传递过去就可以*/}
                    用户名：<input onChange = {(event)=>{this.saveType('name',event)}} type = "text" name ="username"/>
                    密码<input onChange = {this.saveType('pwd', event)} type = "password" name ="password"/>
                    <button>登录</button>
                </form>
            )
        }
    }

    ReactDOM.render(<Login />,document.getElementById("div"));
</script>
</html>
```

---

### 组件生命周期

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
   

</head>
<body>
    <div id = "div" >

    </div>

</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">

    class Life extends React.Component{
        /*
           组件从创建到死亡，会经过一些特定的阶段
            React组件中包含一系列钩子函数{生命周期回调函数}，会在特定的时刻调用
            我们在定义组件的时候，会在特定的声明周期回调函数中，做特定的工作
        */

        //定义透明度
        state = {time:1};

        stop = () => {
            //卸载组件
            ReactDOM.unmountComponentAtNode(document.getElementById("div"))
          
        }

        //在组建挂载(渲染之后进行)
        componentDidMount(){
            console.log("componentDidMount")
            //定时器
            this.Inter = setInterval(()=>{
                let {time} = this.state;
                time -= 0.1;
                if(time <= 0){
                    time = 1;
                }
                this.setState({time:time});
            },200);
        }

        //组件被卸载之后执行
        componentWillUnmount(){
            console.log("componentDidMount")
            clearInterval(this.Inter);
        }

        render(){
            console.log("render")
            return (
                <div>
                    <h2 style = {{opacity:this.state.time}}>声明周期</h2>
                    <button onClick = {this.stop}>结束</button>
                </div>
            )
        }
    }

    ReactDOM.render(<Life />,document.getElementById("div"));

</script>
</html>
```

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
   

</head>
<body>
    <div id = "div" >

    </div>

</body>
<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">

   class A extends React.Component{
        constructor(props){
            console.log("A --- constructor")
            super(props);
            this.state = {num:1}
            console.log(this)
        }

        add = () => {
            let {num} = this.state;
            this.setState({num:num+1});
            //强制更新
            //this.forceUpdate();
        }

       render(){
           console.log("A --- render");
           console.log(this);
            return (
                <div>
                    <h1>这个是第{this.state.num}个</h1>
                    <B name = {this.state.num}/>
                    <button onClick = {this.add}>点击加一</button>
                </div>
            )
       }

       //在render之前执行
       componentWillMount(){
            console.log("A --- componentWillMount");
            console.log(this)
       }

       //在render之后执行
       componentDidMount(){
        console.log("A --- componenetDidMount");
        console.log(this)
       }

       //更新操作 setState之后执行，判断是否可以更新（true可以，false不可以）
       shouldComponentUpdate(){
            console.log("A --- shouldComponentUpdate");
            return true;
       }
       // 组件更新之前
       componentWillUpdate(){
            console.log("A --- componentWillUpdate");
       }
       //组件更新之后
       componentDidUpdate(){
            console.log("A --- componentDidUpdate");
       }

       //卸载组件之后
       componentWillUnmonut(){
            console.log("A --- componentWillUnmonut");
       }
     
   }
   class B extends React.Component{
       render(){
        console.log("B render")
           return(   
                <div>
                    <h1>这个是B组件,传递过来的是：{this.props.name}</h1>
                    
                </div>
           )
       }
       //父组件进行了更新，子组件先执行这个
       componentWillReceiveProps(){
        console.log("A --- componentWillReceiveProps");
       }
   }


    ReactDOM.render(<A name="mike"/>,document.getElementById("div"));

</script>
</html>
```

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <div id="div"></div>
  </body>
  <!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
  <script
    src="../React-js/17.0/react.development17.0.js"
    type="text/javascript"
  ></script>
  <script
    src="../React-js/17.0/react-dom.development17.0.js"
    type="text/javascript"
  ></script>

  <script src="../React-js/babel.min.js"></script>

  <!--引入对于组件标签的限制-->
  <script src="../React-js/17.0/prop-types.js"></script>

  <script type="text/babel">
    class A extends React.Component {
      constructor(props) {
        console.log("A --- constructor");
        super(props);
        this.state = { num: 1 };
      }

      add = () => {
        let { num } = this.state;
        this.setState({ num: num + 1 });
        //强制更新
        //this.forceUpdate();
      };

      render() {
        console.log("A --- render");
        return (
          <div>
            <h1>这个是第{this.state.num}个</h1>

            <button onClick={this.add}>点击加一</button>
            <h1>name:{this.state.name}</h1>
          </div>
        );
      }

      //必须是静态的
      //必须有返回值（Null或者state对象）
      //如果返回的是state对象，里面的将会对原有的state进行覆盖，并且不能修改【因为初始化，更新都会经过这个函数】
      //给组件传递的参数，可以作为该方法的参数传递过来。因此可以让该参数作为state。
      //也可以以props和state作为参数进行传递
      static getDerivedStateFromProps(props, state) {
        console.log("A --- getDerivedStateFromProps", props, state);
        // 返回的对象会被送到组件的state中
        return { name: "tom"};
      }

      //更新的时候调用，在render和componentDidUpdate之间
      //必须返回一个快照
      getSnapshotBeforeUpdate() {
        console.log("A --- getSnapshotBeforeUpdate");
        return null;
      }

      //在render之后执行
      componentDidMount() {
        console.log(this.state)
        console.log("A --- componenetDidMount");
      }

      //更新操作 setState之后执行，判断是否可以更新（true可以，false不可以）
      shouldComponentUpdate() {
        console.log("A --- shouldComponentUpdate");
        return true;
      }

      //组件更新之后
      componentDidUpdate() {
        console.log("A --- componentDidUpdate");
      }

      //卸载组件之后
      componentWillUnmonut() {
        console.log("A --- componentWillUnmonut");
      }
    }

    ReactDOM.render(<A name="mike" />, document.getElementById("div"));
  </script>
</html>
```

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <div id="div"></div>
  </body>
  <!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
  <script
    src="../React-js/17.0/react.development17.0.js"
    type="text/javascript"
  ></script>
  <script
    src="../React-js/17.0/react-dom.development17.0.js"
    type="text/javascript"
  ></script>

  <script src="../React-js/babel.min.js"></script>

  <!--引入对于组件标签的限制-->
  <script src="../React-js/17.0/prop-types.js"></script>

  <script type="text/babel">
    class A extends React.Component {
      constructor(props) {
        console.log("A --- constructor");
        super(props);
        this.state = { num: 1 };
      }

      add = () => {
        let { num } = this.state;
        this.setState({ num: num + 1 });
      };

      render() {
        console.log("A --- render");
        return (
          <div>
            <h1>这个是第{this.state.num}个</h1>

            <button onClick={this.add}>点击加一</button>
          </div>
        );
      }
      //更新的时候调用，在render和componentDidUpdate之间
      //必须返回一个快照
      // a代表之前的props，b代表之前的state
      getSnapshotBeforeUpdate(a,b) {
        console.log("A --- getSnapshotBeforeUpdate",a,b,this.props, this.state);
        return null;
      }

      //在render之后执行
      componentDidMount() {
        console.log(this.state)
        console.log("A --- componenetDidMount");
      }

      //更新操作 setState之后执行，判断是否可以更新（true可以，false不可以）
      shouldComponentUpdate() {
        console.log("A --- shouldComponentUpdate");
        return true;
      }

      //组件更新之后
      componentDidUpdate() {
        console.log("A --- componentDidUpdate");
      }

      //卸载组件之后
      componentWillUnmonut() {
        console.log("A --- componentWillUnmonut");
      }
    }

    ReactDOM.render(<A name="mike" />, document.getElementById("div"));
  </script>
</html>
```

![image](915B8E70EFDB4B79A45F8EF7E67BB9CC)

![image](6EBD724A083645B4A6ECAB01949193B9)

---

### diff算法

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>
</body>

<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">
    class Person extends React.Component{
        state = {
            person:[
                {id:1,name:"张三",age:18},
                {id:2,name:"李四",age:19}
            ]
        }

        addObject = () =>{
            let {person} = this.state;
            const p = {id:(person.length+1),name:"王五",age:20};
            this.setState({person:[p,...person]});
        }
        
        render() {
            return (
                <div>
                    <button onClick={this.addObject}>点击增加对象,使用id作为索引</button>
                    <ul>
                        {
                            this.state.person.map((p,index)=>{
                               return <li key = {p.id}>{p.name}</li>
                            })
                        }
                    </ul>
                </div>
            )
        }
    }

    ReactDOM.render(<Person />,document.getElementById("div"));
</script>
</html>
```

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>
</body>

<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">
    class Person extends React.Component{
        state = {
            person:[
                {id:1,name:"张三",age:18},
                {id:2,name:"李四",age:19},
            ]
        }

        addObject = () =>{
            let {person} = this.state;
            const p = {id:(person.length+1),name:"王五",age:20};
            this.setState({person:[p,...person]});
        }
        
        render() {
            return (
                <div>
                    <button onClick={this.addObject}>点击增加对象,使用id作为索引</button>
                    <ul>
                        {
                            this.state.person.map((p,index)=>{
                               return <li key = {index}>{p.name}</li>
                            })
                        }
                    </ul>
                </div>
            )
        }
    }

    ReactDOM.render(<Person />,document.getElementById("div"));
</script>
</html>
```

但是使用index作为key，li标签中包含input标签时，可能出错。

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "div">

    </div>
</body>

<!-- 引入依赖 ,引入的时候，必须就按照这个步骤-->
<script src="../React-js/react.development.js" type="text/javascript"></script>
<script src="../React-js/react-dom.development.js" type="text/javascript"></script>

<script src="../React-js/babel.min.js"></script>

<!--引入对于组件标签的限制-->
<script src="../React-js/prop-types.js"></script>

<script type="text/babel">
    class Person extends React.Component{
        state = {
            person:[
                {id:1,name:"张三",age:18},
                {id:2,name:"李四",age:19},
            ]
        }

        addObject = () =>{
            let {person} = this.state;
            const p = {id:(person.length+1),name:"王五",age:20};
            this.setState({person:[p,...person]});
        }
        
        render() {
            return (
                <div>
                    <button onClick={this.addObject}>点击增加对象,使用id作为索引</button>
                    <ul>
                        {
                            this.state.person.map((p,index)=>{
                               return <li key = {index}>{p.name}<input type="text"/></li>
                            })
                        }
                    </ul>
                </div>
            )
        }
    }

    ReactDOM.render(<Person />,document.getElementById("div"));
</script>
</html>
```

使用id作为key，效率更高。

![image](78653D4112524C9DBEAA2F8A606EFA36)

![image](6F55EB5FD2E7408CA8719EF040A6B1C3)

扩展：diff算法

diff 算法是 React 提升渲染性能的一种优化算法，在 React 中有着很重要的地位，也不止于 React ，在 Vue 中也有 diff 算法，似乎没有差别。在最近的 React 学习中，学到了 diff 算法，感觉视频中的内容有点浅，对 diff 算法不够深入，因此想要深入的了解以下 diff 算法。于是在掘金，知乎，CSDN 等平台上，看了大量的博客，都非常地不错，可惜看不明白，wwww。所以这篇文章只是自己对于 diff 算法的一点理解，有什么问题或者错误的地方，大家一定要指出！

什么是虚拟 DOM ？
在谈 diff 算法之前，我们需要先了解虚拟 DOM 。它是一种编程概念，在这个概念里，以一种虚拟的表现形式被保存在内存中。在 React 中，render 执行的结果得到的并不是真正的 DOM 节点，而是 JavaScript 对象

虚拟 DOM 只保留了真实 DOM 节点的一些基本属性，和节点之间的层次关系，它相当于建立在 JavaScript 和 DOM 之间的一层“缓存”

<div class="hello">
    <span>hello world!</span>
</div>
上面的这段代码会转化可以转化为虚拟 DOM 结构

{
    tag: "div",
    props: {
        class: "hello"
    },
    children: [{
        tag: "span",
        props: {},
        children: ["hello world!"]
    }]
}
其中对于一个节点必备的三个属性 tag，props，children

tag 指定元素的标签类型，如“li，div”
props 指定元素身上的属性，如 class ，style，自定义属性
children 指定元素是否有子节点，参数以数组形式传入
而我们在 render 中编写的 JSX 代码就是一种虚拟 DOM 结构。

什么是 diff 算法？
其实刚开始学习 React 的时候，很多人可能都听说过 React 很高效，性能很好这类的话语，这其实就是得益于 diff 算法和 Virturl DOM 的完美结合。

单纯的我刚开始会认为React 也只不过是引入了别人的 diff算法而已，能有多厉害，又不是原创 ？

但当我查阅了众多资料后，发现被提及最多的是一个 “传统 diff 算法”

其实 React 针对 diff 算法做出的优化，才是我们应当学习的

React 将原先时间复杂度为 O(n^3) 的传统算法，优化到了 O(n)

大致执行过程图

![image](1F791F1A5D2641B094476FADEC1DBC92)

那 React 是如何实现的呢？

三个策略
为了将复杂度降到 O(n)，React 基于这三个策略进行了算法优化

Web UI 中 DOM 节点跨层级的移动操作特别少，可以忽略不计。
拥有相同类的两个组件将会生成相似的树形结构，拥有不同类的两个组件将会生成不同的树形结构。
对于同一层级的一组子节点，它们可以通过唯一 id 进行区分。
针对这三个策略，React 分别对 tree diff、component diff 以及 element diff 进行算法优化

tree diff 分层求异
首先会将新旧两个 DOM 树，进行比较，这个比较指的是分层比较。又由于 DOM 节点跨层级的移动操作很少，忽略不计。React 通过 updataDepth 对 虚拟 DOM 树进行层级控制，只会对同层节点进行比较，也就是图中只会对相同颜色方框内的 DOM 节点进行比较。例如：

当对比发现节点消失时，则该节点及其子节点都会被完全删除，不会进行更深层次的比较，这样只需要对树进行一次遍历，便能完成整颗 DOM 树的比较

![image](C594D319642C429DABFF742D6330147B)

这里还有一个值得关注的地方：DOM 节点跨层级移动

为什么会提出这样的问题呢，在上面的删除原则中，我们发现当节点不存在了就会删除，那我只是给它换位了，它也会删除整个节点及其子节点吗？

![image](B57017C76A9F4D39B580EDD2F20B4638)

如图，我们需要实现这样的移动，你可能会以为它会直接这样移动

策略1

但是实际情况，并不是这样的。由于 React 只会简单的进行同层级节点位置变化，对于不同层级的节点，只有创建和删除操作，当发现 B 节点消失时，就会销毁 B，当发现 C 节点上多了 B 节点，就会创建 B 以及它的子节点。

因此这样会非常的复杂，所以 React 官方并不建议我们进行 DOM 节点跨级操作

component diff
在组件层面上，也进行了优化

如果是同一类型的组件，则按照原策略继续比较 虚拟 DOM tree
如果不是，则将这个组件记为 dirty component ，从而替换整个组件下的所有子节点
同时对于同一类型的组件，有可能其 Virtual DOM 没有任何变化，如果能够确切的知道这点就可以节省大量的 diff 运算的时间，因此 React 允许用户通过 shouldComponentUpdate() 判断该组件是否需要进行 diff 算法分析

总的来说，如果两个组件结构相似，但被认定为了不同类型的组件，则不会比较二者的结构，而是直接删除

element diff
element diff 是专门针对同一层级的所有节点的策略。当节点在同一层级时，diff 提供了 3个节点操作方法：插入，移动，删除

当我们要完成如图所示操作转化时，会有很大的困难，因为在新老节点比较的过程中，发现每个节点都要删除再重新创建，但是这只是重新排序了而已，对性能极大的不友好。因此 React 中提出了优化策略：

允许添加唯一值 key 来区分节点

image-20210824163240354

引入 key 的优化策略，让性能上有了翻天覆地的变化

那 key 有什么作用呢？

当同一层级的节点添加了 key 属性后，当位置发生变化时。react diff 进行新旧节点比较，如果发现有相同的 key 就会进行移动操作，而不会删除再创建

那 key 具体是如何起作用的呢？

首先在 React 中只允许节点右移

因此对于上图中的转化，只会进行 A，C 的移动

则只需要对移动的节点进行更新渲染，不移动的则不需要更新渲染

为什么不能用 index 作为 key 值呢？

index 作为 key ，如果我们删除了一个节点，那么数组的后一项可能会前移，这个时候移动的节点和删除的节点就是相同的 key ，在react中，如果 key 相同，就会视为相同的组件，但这两个组件是不同的，这样就会出现很麻烦的事情，例如：序号和文本不对应等问题

所以一定要保证 key 的唯一性

建议
React 已经帮我们做了很多了，剩下的需要我们多加注意，才能有更好的性能

基于三个策略我们需要注意

tree diff 建议：开发组件时，需要注意保持 DOM 结构稳定

component diff 建议：使用 shouldComponentUpdate() 来减少不要的更新

element diff 建议：减少最后一个节点移动到头部的操作，这样前面的节点都需要移动

参考资料
谈谈React中Diff算法的策略及实现

React diff算法

浅谈react 虚拟dom，diff算法与key机制

关于手写实现 diff 算法，还有点难度，这事等学完 React 后再说吧

非常感谢您的阅读，欢迎提出你的意见，有什么问题欢迎指出，谢谢！🎈


### 脚手架

![image](E1F7D1642DF647869AD2FFA134BC4A38)

![image](5563D44139ED4C3DB8D3096D51245614)

---

### 脚手架文件介绍

![image](B6CE2E8DCD394A538771116721896193)

index.html文件介绍

![image](0BDE9BD6DB604DFE81F42246EB33B575)

---

### 脚手架文件介绍

![image](FAFDF8D7FBFD424BBE9404E4A13AD4B2)

index.js是项目的入口文件，该文件中将App组件绑定到容器中，App组件是React中的全局父组件。

App.js定义了App组件的内容。App.css定义了App组件的标签的样式。

index.css定义全局的样式

---

### hello组件

脚手架文件介绍

![image](6AD2A056F8414DC3BCB1A95B17335DDF)

index.html
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>React App</title>
  </head>
  <body>
    <div id="root"></div>
  </body>
</html>
```

App.js
```
import React  from "react";

class App extends React.Component {
  render() {
    return (
      <div>
        hello, react
      </div>
    )
  }
}

export default App
```

index.js
```
import React from "react";
import ReactDOM from "react-dom";

import App from "./App";

ReactDOM.render(<App />, document.getElementById("root"));
```

最终效果

![image](B77783DE29694B5C98B72834A7A53B97)

将hello写成一个组件。

App.js
```
import React  from "react";
import Hello from "./hello";

class App extends React.Component {
  render() {
    return (
      <div>
        <Hello></Hello>
      </div>
    )
  }
}

export default App
```

hello.js
```
import React  from "react";

class Hello extends React.Component {
  render() {
    return (
      <div>
        hello, react
      </div>
    )
  }
}

export default Hello
```

将hello组件定义在文件中，并定义样式

![image](5A0082CA84494AB784007C7B874D86C5)

hello.js
```
import React from "react";
import "./hello.css";

class Hello extends React.Component {
  render() {
    return <div className="title">hello, react</div>;
  }
}

export default Hello;
```

hello.css
```
.title {
  color: red;
}
```

接着需要将一个组件的内容写在一个文件夹中。

![image](E745E99217AD4ACDB8590C261DD9FA2A)

最后的项目文件结构

![image](61A58F43B7A5426B80C3732D1C660012)

---

### 样式的模块化

比如，在hello.js定义hello组件，引入hello.css，但是之后，其他组件也可以使用这个样式。比如hello.css中定义了.h1 {
    color: red
}，后面其他组件的h1标签的文字颜色也会是红色。此时可以在

![image](91130894DCCD4DCDAA0E907D6BA376C0)

此时，hello.module.css中定义的样式只在hello.js定义的组件生效。

---

### 组件编码流程

![image](A2BC96D5BEEE45C58D9DD528EE30087A)

一般在component中定义一个文件夹，文件夹名字为组件的名字，再定义一个以组件为名字的js文件，在js文件中输入rcc+enter得到组件的大致代码，在创建组件名.module.css，书写组件的样式。

![image](C90F9C55A4404580B0B39FA999E934EC)

---

### TodoList案例

文件结构

![image](22D9F521A8F54A918E8C56D561BADF09)

index.js

```
//引入核心库
import React from 'react'
import ReactDOM from 'react-dom'
//引入组件
import App from './App.jsx'

ReactDOM.render(<App />,document.getElementById("root"))
```

App.jsx

```
//创建外壳组件APP
import React,{Component} from 'react'
import './App.css'
import Footer from './component/footer/footer'
import Header from './component/header/header'
import List from './component/list/list'

class App extends Component{

    state={todos:[
        {id:1,name:"吃饭",done:true},
        {id:2,name:"睡觉",done:false},
        {id:3,name:"打代码",done:true},
    ]}


    //添加相应的事情
    code = (value)=>{
        //如果想要子组件中的值传递给父组件，就可以给子组件一个函数，子组件在调用函数的时候，将值作为参数传递过去
        
        const {todos} = this.state;
        let p = {id:(todos.length+1),name:value,done:false}
        this.setState({todos:[p,...todos]});
    }
    

    //根据id,修改状态中是否被选中
    checked = (id,checked) =>{
        const {todos} = this.state;
        const newTodo =  todos.map((todo)=>{
            if(todo.id === id){
                return {...todo,done:checked};
            }
            return todo;
        })
        this.setState({todos:newTodo})

    }

    //点击删除按钮，删除其中一行
    deleteById =(id)=>{
        const {todos} = this.state;
        const newTo = todos.filter((todo)=>{
            return todo.id !== id
        })
        this.setState({todos:newTo})
    }

    //全选
    choseAll = (done)=> {
        const {todos} = this.state
        
        const newTo = todos.map((todo)=>{
            return {...todo,done};
        })
        this.setState({todos:[...newTo]})
    }


    //删除选中的内容
    Alldelete = () =>{
        const {todos} = this.state;
        // filter() 方法创建一个新的数组，新数组中的元素是通过检查指定数组中符合条件的所有元素。
        const newTo = todos.filter((todo)=>{
            return todo.done !== true
        })
        this.setState({todos:newTo})
    }


    render(){
        return (
            <div className="todo-container">
                <div className="todo-wrap">
                    <Header code = {this.code} />
                    {/*注意：传递参数的属性名称不能是关键字，比如delete*/}
                    <List todos = {this.state.todos} show = {this.checked} deleteById = {this.deleteById}/>
                    <Footer allCheck = {this.state} choseAll = {this.choseAll} Alldelete = {this.Alldelete} />
                </div>
                    
            </div>
        )
    }
}

export default App  
```

App.css
```
/*base*/
body {
    background: #fff;
  }
  
  .btn {
    display: inline-block;
    padding: 4px 12px;
    margin-bottom: 0;
    font-size: 14px;
    line-height: 20px;
    text-align: center;
    vertical-align: middle;
    cursor: pointer;
    box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.2), 0 1px 2px rgba(0, 0, 0, 0.05);
    border-radius: 4px;
  }
  
  .btn-danger {
    color: #fff;
    background-color: #da4f49;
    border: 1px solid #bd362f;
  }
  
  .btn-danger:hover {
    color: #fff;
    background-color: #bd362f;
  }
  
  .btn:focus {
    outline: none;
  }
  
  .todo-container {
    width: 600px;
    margin: 0 auto;
  }
  .todo-container .todo-wrap {
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 5px;
  }
```

header.jsx
```
import React, { Component } from 'react'
import PropType from 'prop-types'
import  './header.css'

export default class Header extends Component {

    static propTypes = {
        code:PropType.func.isRequired
    }


    handleKeyUp = (event) =>{
        const {target,keyCode} = event
        //keyCode:是键盘点击的那一个键值，13代表着回车2
        //判断是否是回车
        if(keyCode !== 13) return 
        //判断这个输入是否空
        if(target.value.trim() === ''){
            alert("输入的不能为空");
            return
        }
        this.props.code(target.value);
        target.value = "";
    }
    
    render() {
        return (
            <div className ="todo-header">
                <input onKeyUp={this.handleKeyUp}  type="text" placeholder="请输入你的任务名称，按回车键确认"/>
            </div>
        )
    }
}
```

header.css
```
 /*header*/
 .todo-header input {
    width: 560px;
    height: 28px;
    font-size: 14px;
    border: 1px solid #ccc;
    border-radius: 4px;
    padding: 4px 7px;
  }
  
  .todo-header input:focus {
    outline: none;
    border-color: rgba(82, 168, 236, 0.8);
    box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 8px rgba(82, 168, 236, 0.6);
  }
```

list.jsx
```
import React, { Component } from 'react';
import PropType from 'prop-types'
import Item from '../item/item'
import './list.css'

class List extends Component {

    //对接收的参数做限制,限制不能为空以及参数的类型
    static propTypes = {
        todos:PropType.array.isRequired,
        show:PropType.func.isRequired,
        deleteById:PropType.func.isRequired,
    }
    
    render() {
        const {todos} = this.props;
        console.log(this.props.show)
        return (
            
                <ul className="todo-main">
                    {
                        todos.map((todo)=>{
                            return <Item key = {todo.id} {...todo} createCheck = {this.props.show} deleteById = {this.props.deleteById} />
                        })
                    }
                </ul>
        );
    }
}

export default List;
```

list.css
```

/*main*/
.todo-main {
    margin-left: 0px;
    border: 1px solid #ddd;
    border-radius: 2px;
    padding: 0px;
  }
  
  .todo-empty {
    height: 40px;
    line-height: 40px;
    border: 1px solid #ddd;
    border-radius: 2px;
    padding-left: 5px;
    margin-top: 10px;
  }
```

item.jsx
```
import React, { Component } from 'react'
import './item.css'

export default class Item extends Component {

    state = {mouse:false}

    //鼠标移入移出的回调
    handleMouse = (flag) =>{
        return () =>{
          this.setState({mouse:flag});  
        }
    }
    //勾选以及取消勾选的id
    show =(id)=>{
        return (event)=>{
            this.props.createCheck(id,event.target.checked);
        }
    }

    //删除按钮
    handleDelete = (id) => {
        return () =>{
            // confirm()方法用于显示一个带有指定消息和确认及取消按钮的对话框。
            // 如果访问者点击"确定"，此方法返回true，否则返回false。
            // 如果直接使用confrim会提示错误，因此使用window.confrim
            if(window.confirm('确认删除吗？')){
                this.props.deleteById(id);
            }
        }
    }

    render() {
        const {id,name,done} = this.props;
        const {mouse} = this.state;

        return (
            <li style={{backgroundColor:mouse?'#ddd':'white'}} onMouseLeave={this.handleMouse(false)} onMouseEnter={this.handleMouse(true)}>
                <label>
                    <input type="checkbox" checked={done} onChange={this.show(id)}/>
                    <span>{name}</span>
                </label>
                <button onClick={this.handleDelete(id)} className="btn btn-danger" style={{display:mouse?'block':'none'}}>删除</button>
            </li>
        )
    }
}
```

item.css
```
/*item*/
li {
    list-style: none;
    height: 36px;
    line-height: 36px;
    padding: 0 5px;
    border-bottom: 1px solid #ddd;
  }
  
  li label {
    float: left;
    cursor: pointer;
  }
  
  li label li input {
    vertical-align: middle;
    margin-right: 6px;
    position: relative;
    top: -1px;
  }
  
  li button {
    float: right;
    display: none;
    margin-top: 3px;
  }
  
  li:before {
    content: initial;
  }
  
  li:last-child {
    border-bottom: none;
  }
```

footer.jsx
```
import React, { Component } from 'react';
import './footer.css'
class Footer extends Component {

    
    //全选以及全不选
    chose = (event) =>{
        //1.如果选中，所有的全都选中
        this.props.choseAll(event.target.checked)
    }

    //删除选中内容
    Alldelete = () =>{
        this.props.Alldelete();
    }



    render() {

        const {todos} = this.props.allCheck;
        // let sum = 0;
        // todos.map((todo)=>{
        //     if(todo.done){
        //         sum++
        //     }
        //     return sum;
        // })
        //reduce() 方法接收一个函数作为累加器，数组中的每个值（从左到右）开始缩减，最终计算为一个值
        //reduce((初始值,当前的元素)=>{},传递给函数的初始值)
        const sum =  todos.reduce((pre,todo)=>{return pre+(todo.done?1:0)},0)

        return (
            <div className="todo-footer">
                <label>
                    {/*注意不能使用defaultChecked,这个只能在初始化的时候执行一次，并且如果使用checkede就必须添加onChange*/}
                <input onChange={this.chose} type="checkbox"  checked = {sum === todos.length && todos.length!==0?true:false}/>
                </label>
                <span>
                <span>已完成{sum}</span> / 全部{todos.length}
                </span>
                <button onClick={this.Alldelete} className="btn btn-danger">清除已完成任务</button>
            </div>
        );
    }
}

export default Footer;
```

footer.css
```
/*footer*/
.todo-footer {
    height: 40px;
    line-height: 40px;
    padding-left: 6px;
    margin-top: 5px;
  }
  
  .todo-footer label {
    display: inline-block;
    margin-right: 20px;
    cursor: pointer;
  }
  
  .todo-footer label input {
    position: relative;
    top: -1px;
    vertical-align: middle;
    margin-right: 5px;
  }
  
  .todo-footer button {
    float: right;
    margin-top: 5px;
  }
```

index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id = "root"></div>
</body>
</html>
```

---

### 总结

![image](44C33FDA08284A8CB05FC19F39229F86)

---

### react ajax

![image](14563550854C4BA78C5CEBECF99D019A)

脚手架代理配置

https://www.bilibili.com/video/BV1wy4y1D7JT?p=65

https://www.bilibili.com/video/BV1wy4y1D7JT?p=66

---

### Github搜索案例

![image](A1B85699BD0441748102D82000D0602C)

文件结构

![image](B93EF6895B604F6088014116EB769B03)

index.js

```
//引入核心库
import React from 'react'
import ReactDOM from 'react-dom'
//引入组件
import App from './App.jsx'

ReactDOM.render(<App />,document.getElementById("root"))
```

App.jsx

```
//创建外壳组件APP
import React,{Component} from 'react'
import Header from './header/header';
import List from './list/list'

class App extends Component{
    
    state = {
        Git:[],
        isFrist:true,
        isLoad:false,
        isError:''
    }

    // gitHub = (value) =>{
    //     this.setState({Git:value}) 
    // }

    updateAppState = (stateObj) =>{
        this.setState(stateObj) 
    }
    
    render(){
        //通过 ...将状态中的全部赋值过去
        return ( 
            <div className="container">
                <Header updateAppState = {this.updateAppState} />
                
                <List {...this.state} />
            </div>    
            
        )
    }
}

export default App  
```

App.css为空文件

header.jsx

```
import React, { Component } from 'react'
import axios from 'axios';
export default class Header extends Component {

    search = () =>{
        //const {value} = this.KeyValue;
        //连续解构赋值，拿到this下面的KeyValue中的value,并进行重命名为KeyWord
        const {KeyValue:{value:keyWord}} = this;

        //在搜索之前设置,搜索的开始，结束第一次展示
        this.props.updateAppState({isFrist:false,isLoad:true})

        //切记在配置代理了之后一定需要添加相应的路径
        axios.get(`https://api.github.com/search/users?q=${keyWord}`).then(
            success => {
                this.props.updateAppState({Git:success.data.items,isLoad:false});
            },
            error =>    {
                this.props.updateAppState({isError:error.message,isLoad:false});
            }
        )
    }

    render() {
        return (
            <section className="jumbotron">
                <h3 className="jumbotron-heading">搜索GitHub用户</h3>
                <div>
                    {/*使用ref拿到输入的数据，ref中使用回调函数的形式，在实例对象中创建一个KeyValue的属性，值是该节点*/}
                    <input ref={ c => this.KeyValue = c} type="text" placeholder="输入关键词进行搜索"/>&nbsp;
                    <button onClick = {this.search}>搜索</button>
                </div>
            </section>
        )
    }
}
```

list.jsx
```
import React, { Component } from 'react';

import './list.css'
class List extends Component {


    

    render() {

        const {Git,isFrist,isLoad,isError} = this.props;
        return (
            <div className="row">
                {
                    //因为不能在JSX语法中使用if，只能是表达式，所以可以是有用三元运算符进行判断。
                    isFrist ? <h1>欢迎进入页面</h1> : 
                    isLoad ? <h2>正在搜索页面</h2> :
                    isError !== ''? <h1>{isError}</h1> :
                    //注意传递过来的一定是一个数组，不能是一个对象
                    //要不然初始化的时候对象就是 undefined 在遍历的时候就会出错
                    Git.map((git)=>{
                    return (
                        <div className="card" key = {git.id}>
                            <a href={git.html_url} target="_blank" rel="noreferrer">
                            <img alt="headImg" src={git.avatar_url} style={{width:'100px'}}/>
                            </a>
                            <p className="card-text">{git.login}</p>
                        </div>
                        )
                    })
                }
                
                
            </div>
        );
    }
}

export default List;
```

list.css
```
.album {
    min-height: 50rem; /* Can be removed; just added for demo purposes */
    padding-top: 3rem;
    padding-bottom: 3rem;
    background-color: #f7f7f7;
  }
  
  .card {
    float: left;
    width: 33.333%;
    padding: .75rem;
    margin-bottom: 2rem;
    border: 1px solid #efefef;
    text-align: center;
  }
  
  .card > img {
    margin-bottom: .75rem;
    border-radius: 100px;
  }
  
  .card-text {
    font-size: 85%;
  }
```

index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link href="./css/bootstrap.css" rel="stylesheet"> 
</head>
<body>
    <div id = "root"></div>
</body>
</html>
```
---

### 使用消息订阅来实现github案例

文件结构

![image](5FB4A13DF2A84742BCBA90C12E5D99BB)

改动

App.jsx

```
//创建外壳组件APP
import React,{Component} from 'react'
import Header from './header/header';
import List from './list/list'

class App extends Component{
    render(){
        //通过 ...将状态中的全部赋值过去
        return ( 
            <div className="container">
                <Header />
                
                <List  />
            </div>    
            
        )
    }
}

export default App  
```

header.jsx

```
import React, { Component } from 'react'
import axios from 'axios';
import PubSub from 'pubsub-js'

export default class Header extends Component {

    search = () =>{
        //const {value} = this.KeyValue;
        //连续解构赋值，拿到this下面的KeyValue中的value,并进行重命名为KeyWord
        const {KeyValue:{value:keyWord}} = this;

        //在搜索之前设置,搜索的开始，结束第一次展示
        PubSub.publish("getSate",{isFrist:false,isLoad:true})

        //切记在配置代理了之后一定需要添加相应的路径
        axios.get(`https://api.github.com/search/users?q=${keyWord}`).then(
            success => {
                PubSub.publish("getSate",{Git:success.data.items,isLoad:false})
            },
            error =>    {
                PubSub.publish("getSate",{isError:error.message,isLoad:false})
            }
        )
    }

    render() {
        return (
            <section className="jumbotron">
                <h3 className="jumbotron-heading">搜索GitHub用户</h3>
                <div>
                    {/*使用ref拿到输入的数据，ref中使用回调函数的形式，在实例对象中创建一个KeyValue的属性，值是该节点*/}
                    <input ref={ c => this.KeyValue = c} type="text" placeholder="输入关键词进行搜索"/>&nbsp;
                    <button onClick = {this.search}>搜索</button>
                </div>
            </section>
        )
    }
}
```

list.jsx
```
import React, { Component } from 'react';
import PubSub from 'pubsub-js'

import './list.css'
class List extends Component {

    state = {
        Git:[],
        isFrist:true,
        isLoad:false,
        isError:''
    }

    //在组件渲染之前订阅消息
    componentDidMount(){
        PubSub.subscribe("getSate",(_,data)=>{
            console.log(data)
            this.setState(data)
        })
    }

    render() {

        const {Git,isFrist,isLoad,isError} = this.state;
        return (
            <div className="row">
                {
                    //因为不能在JSX语法中使用if，只能是表达式，所以可以是有用三元运算符进行判断。
                    isFrist ? <h1>欢迎进入页面</h1> : 
                    isLoad ? <h2>正在搜索页面</h2> :
                    isError !== ''? <h1>{isError}</h1> :
                    //注意传递过来的一定是一个数组，不能是一个对象
                    //要不然初始化的时候对象就是 undefined 在遍历的时候就会出错
                    Git.map((git)=>{
                    return (
                        <div className="card" key = {git.id}>
                            <a href={git.html_url} target="_blank" rel="noreferrer">
                            <img alt="headImg" src={git.avatar_url} style={{width:'100px'}}/>
                            </a>
                            <p className="card-text">{git.login}</p>
                        </div>
                        )
                    })
                }
                
                
            </div>
        );
    }
}

export default List;
```

### fetch来进行网络请求

改动

![image](BDAD4E3ECC304FFCA32CD740B495CA7F)

header.jsx

```
import React, { Component } from 'react'
// import axios from 'axios';
import PubSub from 'pubsub-js'

export default class Header extends Component {

     search = async() =>{
        //const {value} = this.KeyValue;
        //连续解构赋值，拿到this下面的KeyValue中的value,并进行重命名为KeyWord
        const {KeyValue:{value:keyWord}} = this;

        //在搜索之前设置,搜索的开始，结束第一次展示
        PubSub.publish("getSate",{isFrist:false,isLoad:true})

    

        // fetch(`https://api.github.com/search/users?q=${keyWord}`).then(
        //     resolve =>{
        //         //关注分离原则，先判断网络是不是成功
        //         console.log("网络链接成功",resolve);
        //         //在通过json获取数据
        //         return resolve.json(); //获取数据
        //     },
        //     reject =>{
        //         console.log("网络链接失败",reject);
        //     }
        // ).then(
        //     resolve =>{
        //         console.log(resolve);
        //     }
        // )

        try {
            //链接网络,获取成功的返回值
            const wang = await fetch(`http://localhost:3000/api1/search/users?q=${keyWord}`)
            //通过成功的返回值，获取数据 json()只是获取json文件
            //还有其他获取的方法，但是这些方法只能使用一个
            const users = await wang.json();
           // const wang2 = await wang.clone(); 将返回的成功结果复制一份
            //提取出数据中想要的结果                                                                    
            console.log(users.items);
        } catch (error) {
            
        }
    }

    render() {
        return (
            <section className="jumbotron">
                <h3 className="jumbotron-heading">搜索GitHub用户</h3>
                <div>
                    {/*使用ref拿到输入的数据，ref中使用回调函数的形式，在实例对象中创建一个KeyValue的属性，值是该节点*/}
                    <input ref={ c => this.KeyValue = c} type="text" placeholder="输入关键词进行搜索"/>&nbsp;
                    <button onClick = {this.search}>搜索</button>
                </div>
            </section>
        )
    }
}
```

### 总结Github搜索案例

![image](E98831D9F4E045CF881BE148CFDE7BD8)

---

### SPA

![image](85B9E8C51BBD4118B8AA823CFC54D945)

---

### 路由理解

![image](5D67AC624E154F6FB052201A7BBB8E54)

https://www.bilibili.com/video/BV1wy4y1D7JT?p=76

---

### 路由基本使用

![image](4426464940F74525B973E680EBFF3A3F)


文件结构

![image](BAF2E4CBD4B3402B98884D217611D5CC)

App.js

```
import React from "react";
import { BrowserRouter, Link, Route,Routes} from "react-router-dom";
import About from "./components/About/About";
import Home from "./components/Home/Home";

class App extends React.Component {
  render() {
    return (
      <div>
        <BrowserRouter>
          <h3>主页</h3>
          {/* 书写路由链接 */}
          <Link to="/about">About</Link>
          <Link to="/home">Home</Link>
          {/* 书写路由的跳转 */}
          <Routes>
            <Route path="/about" element={<About/>}></Route>
            <Route path="/home" element={<Home/>}></Route>
          </Routes>
          
        </BrowserRouter>
      </div>
    );
  }
}

export default App;
```

About.js

```
import React, { Component } from "react";
export default class About extends Component {
  
  render() {
    return (
      <h3>我是About</h3>
    )
  }
}
```

Home.js

```
import React, { Component } from "react";
export default class Home extends Component {
  render() {
    return (
      <h3>我是Home</h3>
    )
  }
}
```

如果想要加入新的路由链接的话，需要这么写

UserCenter.js

```
import React, { Component } from "react";
export default class UserCenter extends Component {
  render() {
    return (
      <h3>我是UserCenter</h3>
    )
  }
}
```

App.js

```
import React from "react";
import { BrowserRouter, Link, Route,Routes} from "react-router-dom";
import About from "./components/About/About";
import Home from "./components/Home/Home";
import UserCenter from "./components/UserCenter/UserCenter";

class App extends React.Component {
  render() {
    return (
      <div>
        <BrowserRouter>
          <h3>主页</h3>
          {/* 书写路由链接 */}
          <Link to="/about">About</Link>
          <Link to="/home">Home</Link>
          <Link to="/UserCenter">UserCenter</Link>
          {/* 书写路由的跳转 */}
          <Routes>
            <Route path="/about" element={<About/>}></Route>
            <Route path="/home" element={<Home/>}></Route>
            <Route path="/userCenter" element={<UserCenter/>}></Route>
          </Routes>
          
        </BrowserRouter>
      </div>
    );
  }
}

export default App;
```

也可以在index.js中这样写

index.js

```
import React from "react";
import ReactDOM from "react-dom";
import { BrowserRouter} from "react-router-dom";

import App from "./App";

ReactDOM.render(
    <BrowserRouter>
        <App></App>
    </BrowserRouter>
, document.getElementById("root"));
```

App.js可以这么写
```
import React from "react";
import {Link, Route,Routes} from "react-router-dom";
import About from "./components/About/About";
import Home from "./components/Home/Home";
import UserCenter from "./components/UserCenter/UserCenter";

class App extends React.Component {
  render() {
    return (
      <div>
          <h3>主页</h3>
          {/* 书写路由链接 */}
          <Link to="/about">About</Link>
          <Link to="/home">Home</Link>
          <Link to="/UserCenter">UserCenter</Link>
          {/* 书写路由的跳转 */}
          <Routes>
            <Route path="/about" element={<About/>}></Route>
            <Route path="/home" element={<Home/>}></Route>
            <Route path="/userCenter" element={<UserCenter/>}></Route>
          </Routes>
          
      </div>
    );
  }
}

export default App;
```

这样Link和Route可以不被BrowserRouter标签包裹。

---

### 路由组件

index.js中App组件也可以被HashRouter包裹。

```
import React from "react";
import ReactDOM from "react-dom";
import { HashRouter } from "react-router-dom";

import App from "./App";

ReactDOM.render(
  <HashRouter>
    <App></App>
  </HashRouter>,
  document.getElementById("root")
);
```

![image](68D6C5EA9CB84EA3B6A7263B5923A583)

文件结构

![image](FB37CB6F280F4329A8B2B8DE2647871D)

index.js

```
import React from "react";
import ReactDOM from "react-dom";
import { BrowserRouter } from "react-router-dom";

import App from "./App";

ReactDOM.render(
  <BrowserRouter>
    <App></App>
  </BrowserRouter>,
  document.getElementById("root")
);
```

App.js

```
import React from "react";
import { Link, Route} from "react-router-dom";
import About from "./pages/About/About";
import Home from "./pages/Home/Home";
import UserCenter from "./pages/UserCenter/UserCenter";
import Headers from "./components/Headers/Headers";

class App extends React.Component {
  render() {
    return (
      <div>
        <h3>主页</h3>
        <Headers></Headers>
        {/* 书写路由链接 */}
        <Link to="/about">About</Link>
        <Link to="/home">Home</Link>
        <Link to="/UserCenter">UserCenter</Link>
        {/* 书写路由的跳转 */}

        <Route path="/about" component={About}></Route>
        <Route path="/home" component={Home}></Route>
        <Route path="/userCenter" component={UserCenter}></Route>
      </div>
    );
  }
}

export default App;
```

Home.js

```
import React, { Component } from "react";
export default class Home extends Component {
  render() {
    return (
      <h3>我是Home</h3>
    )
  }
}
```

About.js

```
import React, { Component } from "react";
export default class About extends Component {
  
  render() {
    console.log("About中的props", this.props)
    return (
      <h3>我是About</h3>
    )
  }
}
```

UserCenter.js

```
import React, { Component } from "react";
export default class UserCenter extends Component {
  render() {
    return (
      <h3>我是UserCenter</h3>
    )
  }
}
```

Headers.js

```
import React, { Component } from "react";
export default class Headers extends Component {
  
  render() {
    console.log("header中的props", this.props)
    return (
      <h3>欢迎</h3>
    )
  }
}
```

---

### Navlink

如何在点击的时候，给路由链接添加样式？

使用NavLink组件替代Link组件

文件结构如下：

![image](408DAB2FB9C84A2892110867A9559B7B)

App.js

```
import React from "react";
import { NavLink, Route } from "react-router-dom";
import About from "./pages/About/About";
import Home from "./pages/Home/Home";
import UserCenter from "./pages/UserCenter/UserCenter";
import Headers from "./components/Headers/Headers";
import "./App.css"

class App extends React.Component {
  render() {
    return (
      <div>
        <h3>主页</h3>
        <Headers></Headers>
        {/* 书写路由链接 */}
        <NavLink activeClassName="red" className="link" to="/about">
          About
        </NavLink>
        <NavLink activeClassName="red" className="link" to="/home">
          Home
        </NavLink>
        <NavLink activeClassName="red" className="link" to="/UserCenter">
          UserCenter
        </NavLink>
        {/* 书写路由的跳转 */}

        <Route path="/about" component={About}></Route>
        <Route path="/home" component={Home}></Route>
        <Route path="/userCenter" component={UserCenter}></Route>
      </div>
    );
  }
}

export default App;
```

App.css
```
.red {
  color: red;
}

.link {
  padding: 20px;
}
```

NavLink组件中可以添加类名，activeClassName代表链接被点击时添加的类。

---

### 封装NavLink

文件结构如下：

![image](614F0E8FE5D34538B2E8A1CBC9AF77DD)

App.js

```
import React from "react";
import {Route } from "react-router-dom";
import About from "./pages/About/About";
import Home from "./pages/Home/Home";
import UserCenter from "./pages/UserCenter/UserCenter";
import Headers from "./components/Headers/Headers";
import MyNavLink from "./components/MyNavLink/MyNavLink";
import "./App.css"

class App extends React.Component {
  render() {
    return (
      <div>
        <h3>主页</h3>
        <Headers></Headers>
        {/* 书写路由链接 */}
        <MyNavLink activeClassName="red" className="link" to="/about" children="About"></MyNavLink>
        <MyNavLink activeClassName="red" className="link" to="/home" children="Home">Home</MyNavLink>
        <MyNavLink activeClassName="red" className="link" to="/UserCenter" children="UserCenter">UserCenter</MyNavLink>
        {/* 书写路由的跳转 */}

        <Route path="/about" component={About}></Route>
        <Route path="/home" component={Home}></Route>
        <Route path="/userCenter" component={UserCenter}></Route>
      </div>
    );
  }
}

export default App;
```

MyNavLink.js
```
import React, { Component } from "react";
import { NavLink} from "react-router-dom";

export default class MyNavLink extends Component {
  
  render() {
    return (
        <NavLink activeClassName="red" className="link"{...this.props}>
        </NavLink>
    )
  }
}
```

![image](7EB822E118644C30BBD8F9BC80805BE9)

---

### Switch的使用

App.js

```
import React from "react";
import {Route } from "react-router-dom";
import About from "./pages/About/About";
import Home from "./pages/Home/Home";
import UserCenter from "./pages/UserCenter/UserCenter";
import Headers from "./components/Headers/Headers";
import MyNavLink from "./components/MyNavLink/MyNavLink";
import "./App.css"

class App extends React.Component {
  render() {
    return (
      <div>
        <h3>主页</h3>
        <Headers></Headers>
        {/* 书写路由链接 */}
        <MyNavLink activeClassName="red" className="link" to="/about" children="About"></MyNavLink>
        <MyNavLink activeClassName="red" className="link" to="/home" children="Home">Home</MyNavLink>
        <MyNavLink activeClassName="red" className="link" to="/UserCenter" children="UserCenter">UserCenter</MyNavLink>
        {/* 书写路由的跳转 */}

        <Route path="/about" component={About}></Route>
        <Route path="/home" component={Home}></Route>
        <Route path="/home" component={UserCenter}></Route>
      </div>
    );
  }
}

export default App;
```

当跳转到/home链接时，出现了Home组件和UserCenter组件的内容。但是实际上不应该这样。
这是可以使用Switch组件把注册路由的组件进行包裹。

App.js

```
import React from "react";
import {Route,Switch } from "react-router-dom";
import About from "./pages/About/About";
import Home from "./pages/Home/Home";
import UserCenter from "./pages/UserCenter/UserCenter";
import Headers from "./components/Headers/Headers";
import MyNavLink from "./components/MyNavLink/MyNavLink";
import "./App.css"

class App extends React.Component {
  render() {
    return (
      <div>
        <h3>主页</h3>
        <Headers></Headers>
        {/* 书写路由链接 */}
        <MyNavLink activeClassName="red" className="link" to="/about" children="About"></MyNavLink>
        <MyNavLink activeClassName="red" className="link" to="/home" children="Home">Home</MyNavLink>
        <MyNavLink activeClassName="red" className="link" to="/UserCenter" children="UserCenter">UserCenter</MyNavLink>
        {/* 书写路由的跳转 */}
        <Switch>
          <Route path="/about" component={About}></Route>
          <Route path="/home" component={Home}></Route>
          <Route path="/home" component={UserCenter}></Route>
        </Switch>
      </div>
    );
  }
}

export default App;
```

https://www.bilibili.com/video/BV1wy4y1D7JT?p=81

---

### 样式丢失问题

如果我们想给所有的路由前面加一个固定的名字。比如my/Home, my/About, my/UserCenter。

```
import React from "react";
import {Route,Switch } from "react-router-dom";
import About from "./pages/About/About";
import Home from "./pages/Home/Home";
import UserCenter from "./pages/UserCenter/UserCenter";
import Headers from "./components/Headers/Headers";
import MyNavLink from "./components/MyNavLink/MyNavLink";
import "./App.css"

class App extends React.Component {
  render() {
    return (
      <div>
        <h3>主页</h3>
        <Headers></Headers>
        {/* 书写路由链接 */}
        <MyNavLink activeClassName="red" className="link" to="/my/about" children="About"></MyNavLink>
        <MyNavLink activeClassName="red" className="link" to="/my/home" children="Home">Home</MyNavLink>
        <MyNavLink activeClassName="red" className="link" to="/my/UserCenter" children="UserCenter">UserCenter</MyNavLink>
        {/* 书写路由的跳转 */}
        <Switch>
          <Route path="/my/about" component={About}></Route>
          <Route path="/my/home" component={Home}></Route>
          <Route path="/my/UserCenter" component={UserCenter}></Route>
        </Switch>
      </div>
    );
  }
}

export default App;
```

如果访问一个不存在的路径，则会将public/index.html返回回来。

![image](CEB43F6EF73E4F6BA374306D3234CA84)

此外，存在样式丢失的问题。可以通过

1、

![image](4FEF1262ECD24DF5AF67373F9C991CC8)

2、使用HashRouter

![image](A4B92FD9BEBF4ED69B10716972839920)

总共3种方式

![image](50DB8811472F411BAB11FE9D13C57E08)

一般使用第一种方式。

---

### 路由的模糊匹配

模糊匹配

```
import React from "react";
import { Route, Switch } from "react-router-dom";
import About from "./pages/About/About";
import Home from "./pages/Home/Home";
import UserCenter from "./pages/UserCenter/UserCenter";
import Headers from "./components/Headers/Headers";
import MyNavLink from "./components/MyNavLink/MyNavLink";
import "./App.css";

class App extends React.Component {
  render() {
    return (
      <div>
        <h3>主页</h3>
        <Headers></Headers>
        {/* 书写路由链接 */}
        <MyNavLink
          activeClassName="red"
          className="link"
          to="/my/about"
          children="About"
        ></MyNavLink>
        
        <!-- 模糊匹配-->
        <!-- 请求/my/home/mainPage-->
        <MyNavLink
          activeClassName="red"
          className="link"
          to="/my/home/mainPage"
          children="Home"
        ></MyNavLink>
        
        <MyNavLink
          activeClassName="red"
          className="link"
          to="/my/UserCenter"
          children="UserCenter"
        ></MyNavLink>
        
        {/* 书写路由的跳转 */}
        <Switch>
          <Route path="/my/about" component={About}></Route>
          <Route path="/my/home" component={Home}></Route>
          <Route path="/my/UserCenter" component={UserCenter}></Route>
        </Switch>
      </div>
    );
  }
}

export default App;
```

点击Home的时候，请求/my/home/mainPage，但是注册的路由中没有对应的路径，但是模糊匹配上了/my/home，所以返回Home组件。

注意，模糊匹配也要满足一定条件才可以模糊匹配上。

```
import React from "react";
import { Route, Switch } from "react-router-dom";
import About from "./pages/About/About";
import Home from "./pages/Home/Home";
import UserCenter from "./pages/UserCenter/UserCenter";
import Headers from "./components/Headers/Headers";
import MyNavLink from "./components/MyNavLink/MyNavLink";
import "./App.css";

class App extends React.Component {
  render() {
    return (
      <div>
        <h3>主页</h3>
        <Headers></Headers>
        {/* 书写路由链接 */}
        <MyNavLink
          activeClassName="red"
          className="link"
          to="/my/about"
          children="About"
        ></MyNavLink>
        <MyNavLink
          activeClassName="red"
          className="link"
          to="/my/home/mainPage"
          children="Home"
        >
          Home
        </MyNavLink>
        <MyNavLink
          activeClassName="red"
          className="link"
          to="/my/UserCenter"
          children="UserCenter"
        >
          UserCenter
        </MyNavLink>
        {/* 书写路由的跳转 */}
        <Switch>
          <Route exact={true} path="/my/about" component={About}></Route>
          <Route exact={true} path="/my/home" component={Home}></Route>
          <Route exact={true} path="/my/UserCenter" component={UserCenter}></Route>
        </Switch>
      </div>
    );
  }
}

export default App;
```

点击Home的时候，请求/my/home/mainPage，但是注册的路由中没有对应的路径，无法返回任何东西。

![image](C43921DB0FBA42EDA4B75C8047E14B4D)

---

### Redirect使用

如果我们一上来希望转到一个路径，比如转到/about路径。

```
import React from "react";
import { Route, Switch } from "react-router-dom";
import About from "./pages/About/About";
import Home from "./pages/Home/Home";
import UserCenter from "./pages/UserCenter/UserCenter";
import Headers from "./components/Headers/Headers";
import MyNavLink from "./components/MyNavLink/MyNavLink";
import "./App.css";
import { Redirect } from "react-router-dom/cjs/react-router-dom.min";

class App extends React.Component {
  render() {
    return (
      <div>
        <h3>主页</h3>
        <Headers></Headers>
        {/* 书写路由链接 */}
        <MyNavLink
          activeClassName="red"
          className="link"
          to="/about"
          children="About"
        ></MyNavLink>
        <MyNavLink
          activeClassName="red"
          className="link"
          to="/home"
          children="Home"
        >
          Home
        </MyNavLink>
        <MyNavLink
          activeClassName="red"
          className="link"
          to="/UserCenter"
          children="UserCenter"
        >
          UserCenter
        </MyNavLink>
        {/* 书写路由的跳转 */}
        <Switch>
          <Route path="/about" component={About}></Route>
          <Route path="/home" component={Home}></Route>
          <Route path="/UserCenter" component={UserCenter}></Route>
          <Redirect to="/about"></Redirect>
        </Switch>
      </div>
    );
  }
}

export default App;
```

![image](BBCC6718AB9A47DAB9BA69C917BB0EEC)

---

### 嵌套路由

文件结构

![image](4765348136CA47158189809DC8212130)

index.js

```
//引入核心库
import React from 'react'
import ReactDOM from 'react-dom'

import {BrowserRouter} from 'react-router-dom'
//引入组件
import App from './App.jsx'

ReactDOM.render(
    <BrowserRouter>
        <App />
    </BrowserRouter>
    ,document.getElementById("root"))
```

App.jsx

```
//创建外壳组件APP
import React,{Component} from 'react'
import {Route,Switch,Redirect} from 'react-router-dom'
import About from './components/about/about'
import Home from './pages/home/home'
import Header from './pages/header/header'
import MyNavLink from './components/MyNavLink/myNavLink';

class App extends Component{
    
    render(){
        //通过 ...将状态中的全部赋值过去
        return ( 
            <div>
                <div className="row">
                <div className="col-xs-offset-2 col-xs-8">
                    <Header />
                </div>
                </div>
                <div className="row">
                <div className="col-xs-2 col-xs-offset-2">
                    <div className="list-group">
                    {/* <a className="list-group-item active" href="./about.html">About</a>
                    <a className="list-group-item" href="./home.html">Home</a> */}
                    {/* RouteBrowserRouterr:就是利用H5推出的history身上的API
                        HashRouter:就是利用#,也就是锚点 hash值
                    */}

                    {/*NavLink在点击的时候就会去找activeClassName="ss"所指定的class的值，如果不添加默认是active
                        这是因为Link相当于是把标签写死了，不能去改变什么。
                    */}
                    {/* <NavLink  className="list-group-item"  to="/about">About</NavLink>
                    <NavLink className="list-group-item"  to="/home">Home</NavLink> */}

                    {/*将NavLink进行封装，成为MyNavLink,通过props进行传参数，标签体内容是props特殊的一个属性，叫做children */}
                        <MyNavLink to = "/about" >About</MyNavLink>
                        <MyNavLink to = "/home" >Home</MyNavLink>
                    </div>
                </div>
                <div className="col-xs-6">
                    <div className="panel">
                    <div className="panel-body">
                       {/* 注册路由，也就是写对应的关系 */}
                       {/* 路由可以匹配多个路径,因此可以展示多个组件，但是按道理应该只匹配一个即可，而且多个匹配会很耗费性能
                       Switch:就可以保证路由在匹配到第一个路径之后，就不和继续向下走。 */}
                        <Switch>
                            <Route path="/about"component={About}/>
                            {/* exact={true}：开启严格匹配的模式，路径必须一致 */}
                            <Route   path="/home" component={Home}/>
                            {/* Redirect:如果上面的都没有匹配到，就匹配到这个路径下面 */}
                            <Redirect  to = "/about"/>
                        </Switch>
                    </div>
                    </div>
                </div>
                </div>
            </div>
            
        )
    }
}

export default App  
```

App.css为空文件

home.jsx
```
import React, { Component } from 'react'
import Message from './message/message'
import News from './news/news';
import MyNavLink from '../../components/MyNavLink/myNavLink'
import {Switch,Route,Redirect} from 'react-router-dom'
export default class home extends Component {
    render() {
        return (
            <div>
                <h2>Home组件内容</h2>
                <div>
                    <ul className="nav nav-tabs">
                    <li>
                        {/* react中路由的注册是有顺序的，因此在匹配的时候也是按照这个顺序进行的，因此会先匹配父组件中的路由 */}
                        <MyNavLink to = "/home/news">News</MyNavLink>
                    </li>
                    <li>
                        <MyNavLink  to = "/home/message">Message</MyNavLink>
                    </li>
                    </ul>
                    <Switch>
                        <Route path = "/home/news" component={News} />
                        <Route path = "/home/message" component={Message} />
                        <Redirect to="/home/message"/>
                    </Switch>
              </div>
            </div>
        )
    }
}
```

message.jsx

```
import React, { Component } from 'react'

export default class message extends Component {
    render() {
        return (
            <div>
                <ul>
                    <li>
                        <a href="/message1">message001</a>&nbsp;&nbsp;
                    </li>
                    <li>
                        <a href="/message2">message002</a>&nbsp;&nbsp;
                    </li>
                    <li>
                        <a href="/message/3">message003</a>&nbsp;&nbsp;
                    </li>
                </ul>
            </div>
        )
    }
}
```

news.jsx

```
import React, { Component } from 'react'

export default class news extends Component {
    render() {
        return (
            <div>
                <ul>
                    <li>news001</li>
                    <li>news002</li>
                    <li>news003</li>
                </ul>
            </div>
        )
    }
}
```

header.jsx
```
import React, { Component } from 'react'

export default class Hader extends Component {
    render() {
        
        return (
            <div className="page-header"><h2>React Router Demo</h2></div>
        )
    }
}
```

about.jsx

```
import React, { Component } from 'react'

export default class about extends Component {
    render() {
        console.log(this.props);
        return (
            <h3>这个是about</h3>
        )
    }
}
```

myNavLink.jsx

```
import React, { Component } from 'react'
import {NavLink} from 'react-router-dom'
export default class myNavLink extends Component {
    render() {
        return (
            // 通过{...对象}的形式解析对象，相当于将对象中的属性全部展开
            //<NavLink className="list-group-item" to = {this.props.to} children = {this.props.children}/>
            <NavLink className="list-group-item" {...this.props}/>
        )
    }
}
```
about.jsx

```
import React, { Component } from 'react'

export default class about extends Component {
    render() {
        console.log(this.props);
        return (
            <h3>这个是about</h3>
        )
    }
}
```
---

### 路由传参params参数

文件夹如下

![image](CFC9D92D1BAD45B593075329C6F2DE88)

index.js

```
import React from 'react'
import ReactDOM from 'react-dom'
import App from './App'
import {BrowserRouter} from 'react-router-dom'

ReactDOM.render(
	<BrowserRouter>
		<App/>
	</BrowserRouter>,
document.getElementById('root'))
```

App.jsx
```
import React, { Component } from 'react'
import Home from './pages/Home'
import About from './pages/About'
import Header from './components/Header'
import {NavLink,Route,Switch} from 'react-router-dom'

export default class App extends Component {
	render() {
		return (
			<div>
				<Header/>
				<div className="row">
					<div className="col-xs-2 col-xs-offset-2">
						<div className="list-group">

							{/* 原生html中，我们使用a标签进行页面的跳转 */}
							{/* <a className="list-group-item" href="./about.html">About</a>
							<a className="list-group-item" href="./home.html">Home</a> */}

							{/* React中，使用Link进行路径的切换 */}
							<NavLink activeClassName="demo" className="list-group-item"  to="/about">About</NavLink>
							<NavLink activeClassName="demo" className="list-group-item" replace={true} to="/home">Home</NavLink>
						</div>
					</div>
					<div className="col-xs-6">
						<div className="panel">
							<div className="panel-body">
							{/* 注册路由 */}
							<Switch>
								<Route path="/about" component={About}/>
								<Route path="/home" component={Home}/>
							</Switch>
							</div>
						</div>
					</div>
				</div>
			</div>
		)
	}
}
```

index.jsx(home组件)

```
import React, { Component } from 'react'
import Message from './Message'
import News from './News'
import {Route,Switch,NavLink} from 'react-router-dom'

export default class Home extends Component {
	render() {
		return (
			<div>
				<h3>我是Home组件的内容</h3>
				<div>
					<ul className="nav nav-tabs">
						<li>
							<NavLink className="list-group-item" activeClassName="demo" to="/home/news">News</NavLink>
						</li>
						<li>
							<NavLink className="list-group-item" activeClassName="demo" to="/home/message">Message</NavLink>
						</li>
					</ul>
					<div>
						{/* 注册路由 */}
						<Switch>
							<Route path="/home/news" component={News}/>
							<Route path="/home/message" component={Message}/>
						</Switch>
					</div>
				</div>
			</div>
			
		)
	}
}
```

message组件

```
import React, { Component } from 'react'
import {Link,Route} from 'react-router-dom'
import Detail from './Detail'

export default class Message extends Component {
	state = {
		messageArr : [
			{id:'001',title:'消息1'},
			{id:'002',title:'消息2'},
			{id:'003',title:'消息3'},
		]
	}
	render() {
		return (
			<div>
				<ul>
					{
						this.state.messageArr.map((msgObj)=>{
							return (
								<li key={msgObj.id}>

									{/* 跳转路由时携带params参数 */}
									<Link to={`/home/message/detail/${msgObj.id}/${msgObj.title}`}>{msgObj.title}</Link>&nbsp;&nbsp;
								</li>
							)
						})
					}
				</ul>
				<hr/>

				{/* 注册路由时，声明接收params参数 */}
				<Route path="/home/message/detail/:id/:title" component={Detail}/>
			</div>
		)
	}
}
```

Detail组件

```
import React, { Component } from 'react'

const mockData = [
	{id:'001',content:'你好，尚硅谷'},
	{id:'002',content:'你好，我未来的女朋友'},
	{id:'003',content:'你好，我未来的男朋友'},
]
export default class Detail extends Component {
	render() {

		//获取传递过来的params参数
		const {id,title} = this.props.match.params

		const result = mockData.find( detailObj =>detailObj.id === id)

		return (
			<ul>
				<li>ID:{id}</li>
				<li>TITLE:{title}</li>
				<li>CONTENT:{result.content}</li>
			</ul>
		)
	}
}
```

News组件

```
import React, { Component } from 'react'

export default class News extends Component {
	render() {
		return (
			<ul>
				<li>news001</li>
				<li>news002</li>
				<li>news003</li>
			</ul>
		)
	}
}
```

About组件

```
import React, { Component } from 'react'

export default class About extends Component {
	render() {
		// console.log(this.props);
		return <h3>我是About的内容</h3>
	}
}
```

Header组件

```
import React, { Component } from 'react'

export default class Header extends Component {
	render() {
		// console.log(this.props);
		return (
			<div className="row">
				<div className="col-xs-offset-2 col-xs-8">
					<div className="page-header"><h2>React Router Demo</h2></div>
				</div>
			</div>
		)
	}
}
```

---

### 传递query参数

改动

Message组件

```
import React, { Component } from 'react'
import {Link,Route} from 'react-router-dom'
import Detail from './Detail'

export default class Message extends Component {
	state = {
		messageArr : [
			{id:'001',title:'消息1'},
			{id:'002',title:'消息2'},
			{id:'003',title:'消息3'},
		]
	}
	render() {
		return (
			<div>
				<ul>
					{
						this.state.messageArr.map((msgObj)=>{
							return (
								<li key={msgObj.id}>

									{/* 跳转路由时携带params参数 */}
									{/* <Link to={`/home/message/detail/${msgObj.id}/${msgObj.title}`}>{msgObj.title}</Link>&nbsp;&nbsp; */}
								
									{/* 跳转路由时携带search参数 */}
									<Link to={`/home/message/detail?id=${msgObj.id}&title=${msgObj.title}`}>{msgObj.title}</Link>&nbsp;&nbsp;
								</li>
							)
						})
					}
				</ul>
				<hr/>

				{/* 注册路由时，声明接收params参数 */}
				{/* <Route path="/home/message/detail/:id/:title" component={Detail}/> */}

				{/* 注册路由时，如果携带的是search参数，无需声明接收，直接注册即可 */}
				<Route path="/home/message/detail" component={Detail}/>
			</div>
		)
	}
}
```

Detail组件

```
import React, { Component } from 'react'
import qs from 'querystring'

const mockData = [
	{id:'001',content:'你好，尚硅谷'},
	{id:'002',content:'你好，我未来的女朋友'},
	{id:'003',content:'你好，我未来的男朋友'},
]
export default class Detail extends Component {
	render() {
		//获取传递过来的search参数
		// const {search} = this.props.location
		// const {id,title} = qs.parse(search.slice(1))

		const result = mockData.find( detailObj =>detailObj.id === id)

		return (
			<ul>
				<li>ID:{id}</li>
				<li>TITLE:{title}</li>
				<li>CONTENT:{result.content}</li>
			</ul>
		)
	}
}
```

### 传递state对象

Message组件

```
import React, { Component } from 'react'
import {Link,Route} from 'react-router-dom'
import Detail from './Detail'

export default class Message extends Component {
	state = {
		messageArr : [
			{id:'001',title:'消息1'},
			{id:'002',title:'消息2'},
			{id:'003',title:'消息3'},
		]
	}
	render() {
		return (
			<div>
				<ul>
					{
						this.state.messageArr.map((msgObj)=>{
							return (
								<li key={msgObj.id}>

									{/* 跳转路由时携带params参数 */}
									{/* <Link to={`/home/message/detail/${msgObj.id}/${msgObj.title}`}>{msgObj.title}</Link>&nbsp;&nbsp; */}
								
									{/* 跳转路由时携带search参数 */}
									{/* <Link to={`/home/message/detail?id=${msgObj.id}&title=${msgObj.title}`}>{msgObj.title}</Link>&nbsp;&nbsp; */}

									{/* 跳转路由时携带state参数 */}
									<Link to={{pathname:'/home/message/detail',state:{id:'009',title:msgObj.title}}}>{msgObj.title}</Link>&nbsp;&nbsp; 

								</li>
							)
						})
					}
				</ul>
				<hr/>

				{/* 注册路由时，声明接收params参数 */}
				{/* <Route path="/home/message/detail/:id/:title" component={Detail}/> */}

				{/* 注册路由时，如果携带的是search参数，无需声明接收，直接注册即可 */}
				{/* <Route path="/home/message/detail" component={Detail}/> */}

				{/* 注册路由时，如果携带的是state参数，无需声明接收，直接注册即可 */}
				<Route path="/home/message/detail" component={Detail}/>
			</div>
		)
	}
}
```

Detail组件

```
import React, { Component } from 'react'
import qs from 'querystring'

const mockData = [
	{id:'001',content:'你好，尚硅谷'},
	{id:'002',content:'你好，我未来的女朋友'},
	{id:'003',content:'你好，我未来的男朋友'},
]
export default class Detail extends Component {
	render() {
		//获取传递过来的state参数
		const {id,title} = this.props.location.state

		const result = mockData.find( detailObj =>detailObj.id === id) || {}

		return (
			<ul>
				<li>ID:{id}</li>
				<li>TITLE:{title}</li>
				<li>CONTENT:{result.content}</li>
			</ul>
		)
	}
}
```

### 路由跳转

改动部分

Message组件

```
import React, { Component } from 'react'
import {Link,Route} from 'react-router-dom'
import Detail from './Detail'

export default class Message extends Component {
	state = {
		messageArr : [
			{id:'001',title:'消息1'},
			{id:'002',title:'消息2'},
			{id:'003',title:'消息3'},
		]
	}


	pushShow = (id,title)=>{
		return ()=>{
			this.props.history.push(`/home/message/detail/${id}/${title}`)
		}
	}

	replaceShow = (id,title)=>{
		return ()=>{
			this.props.history.replace(`/home/message/detail/${id}/${title}`)
		}
	}

	back = ()=>{
		this.props.history.goBack()
	}

	forward = ()=>{
		this.props.history.goForward()
	}

	go = ()=>{
		this.props.history.go(2)
	}

	render() {
		return (
			<div>
				<ul>
					{
						this.state.messageArr.map((msgObj)=>{
							return (
								<li key={msgObj.id}>

									{/* 跳转路由时携带params参数 */}
									<Link replace to={`/home/message/detail/${msgObj.id}/${msgObj.title}`}>{msgObj.title}</Link>&nbsp;&nbsp;
									<button onClick={this.pushShow(msgObj.id,msgObj.title)}>push查看</button>
									<button onClick={this.replaceShow(msgObj.id,msgObj.title)}>replace查看</button>
								
									
								</li>
							)
						})
					}
				</ul>
				<button onClick={this.back}>回退</button>
				<button onClick={this.forward}>前进</button>
				<button onClick={this.go}>测试go</button>
				<hr/>

				{/* 注册路由时，声明接收params参数 */}
				<Route path="/home/message/detail/:id/:title" component={Detail}/>

				{/* 注册路由时，如果携带的是search参数，无需声明接收，直接注册即可 */}
				{/* <Route path="/home/message/detail" component={Detail}/> */}

				{/* 注册路由时，如果携带的是state参数，无需声明接收，直接注册即可 */}
				{/* <Route path="/home/message/detail" component={Detail}/> */}
			</div>
		)
	}
}
```

Detail组件

```
import React, { Component } from 'react'
import qs from 'querystring'

const mockData = [
	{id:'001',content:'你好，尚硅谷'},
	{id:'002',content:'你好，我未来的女朋友'},
	{id:'003',content:'你好，我未来的男朋友'},
]
export default class Detail extends Component {
	render() {

		//获取传递过来的params参数
		const {id,title} = this.props.match.params
		const result = mockData.find( detailObj =>detailObj.id === id) || {}

		return (
			<ul>
				<li>ID:{id}</li>
				<li>TITLE:{title}</li>
				<li>CONTENT:{result.content}</li>
			</ul>
		)
	}
}
```

---

### withRouter使用

改动

```
import React, { Component } from 'react'
import {withRouter} from 'react-router-dom'


class Header extends Component {

	back = ()=>{
		this.props.history.goBack()
	}

  forward =  ()=>{
		this.props.history.goForward()
	}
	
	render() {
		// console.log(this.props);
		return (
			<div className="row">
				<div className="col-xs-offset-2 col-xs-8">
					<div className="page-header">
						<h2>React Router Demo</h2>
						<button onClick={this.back}>回退</button>
						<button onClick={this.forward}>前进</button>
					</div>
				</div>
			</div>
		)
	}
}

export default withRouter(Header)
```

---

### BrowerRouter与HashRouter

![image](46676EB9C8BF4721A9171A458A6E6830)

https://www.bilibili.com/video/BV1wy4y1D7JT?p=93

---

### antd使用

官网：https://ant.design/components/overview-cn/

antd适合于后台管理系统。

---

### antd按需引入

https://www.bilibili.com/video/BV1wy4y1D7JT?p=94

---

### antd自定义主题

https://www.bilibili.com/video/BV1wy4y1D7JT?p=95

---

### redux

![image](9D7A84600D1A4766A05A03B355789D5A)

---

### redux工作流程图

https://www.bilibili.com/video/BV1wy4y1D7JT?p=98

---

### 求和案例

Count.js

```
import React from "react";
class Count extends React.Component {
  state = {
    count: 0
  }
  increment = () => {
    let {value} = this.selectNumber
    let {count} = this.state
    this.setState({count: count + value * 1})
  }
  decrement = () => {
    let {value} = this.selectNumber
    let {count} = this.state
    this.setState({count: count - value * 1})
  }
  incrementIfOdd = () => {
    let {value} = this.selectNumber
    let {count} = this.state
    if(count % 2 === 1) {
        this.setState({count: count + value * 1})
    }
  }
  incrementAsync = () => {
    let {value} = this.selectNumber
    let {count} = this.state
    setTimeout( () => {
        this.setState({count: count + value * 1})
    },500)
    
  }
  render() {
    return (
      <div>
        <h1>当前求和为：{this.state.count}</h1>
        <select ref={c => this.selectNumber = c}>
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
        </select>&nbsp;
        <button onClick={this.increment}>+</button>&nbsp;
        <button onClick={this.decrement}>-</button>&nbsp;
        <button onClick={this.incrementIfOdd}>当前求和为奇数再加</button>&nbsp;
        <button onClick={this.incrementAsync}>异步加</button>&nbsp;
      </div>
    );
  }
}

export default Count;
```

---

### redux版本求和

文件夹

![image](A9F9BDEA38774FB1B84B199A53722FF6)

index.js

```
import React from 'react'
import ReactDOM from 'react-dom';
import
App from './App'
import store from './redux/store'

ReactDOM.render(<App/>,document.getElementById('root'))

//检测redux中状态的改变
store.subscribe(()=>{
	ReactDOM.render(<App/>,document.getElementById('root'))
})
```

App.jsx

```
import React, { Component } from 'react'
import Count from './components/Count'

export default class App extends Component {
	render() {
		return (
			<div>	
				<Count/>
			</div>
		)
	}
}
```

index.jsx

```
import React, { Component } from 'react'
// 引入store
import store from '../../redux/store'

export default class Count extends Component {

	state = {name:'tom'}

	increment = ()=>{
		//获取用户选择的数字
		const {value} = this.checkNumber
		// action
		store.dispatch({type:'increment',data:value*1})
	}

	decrement = ()=>{
		//获取用户选择的数字
		const {value} = this.checkNumber
		// action
		store.dispatch({type:'decrement',data:value*1})
	}

	incrementIfOdd = ()=>{
		//获取用户选择的数字
		const {value} = this.checkNumber
		// 获取store中保存的
		if(store.getState() % 2 !== 0){
			store.dispatch({type:'increment',data:value*1})
		}
	}
	incrementAsync = ()=>{
		//获取用户选择的数字
		const {value} = this.checkNumber
		setTimeout(()=>{
			store.dispatch({type:'increment',data:value*1})
		},500)
	}

	render() {
		return (
			<div>
				<h2>当前求和为：{store.getState()}</h2>
				<select ref={c => this.checkNumber = c}>
					<option value="1">1</option>
					<option value="2">2</option>
					<option value="3">3</option>
				</select>&nbsp;
				<button onClick={this.increment}>+</button>&nbsp;
				<button onClick={this.decrement}>-</button>&nbsp;
				<button onClick={this.incrementIfOdd}>奇数再+</button>&nbsp;
				<button onClick={this.incrementAsync}>异步+</button>
			</div>
		)
	}
}
```

store.js

```
/* 
	该文件是整个redux中最为核心的store对象
*/
//引入createStore，用于创建store对象
import {createStore} from 'redux'
//引入为Count组件服务的reducer，用于：初始化状态、加工状态
import countReducer from './count_reducer'

//调用createStore创建并暴露store，注意：要传入为store服务的reducer
export default createStore(countReducer)

```

count_reducer.js

```

export default function countReducer(preState=0,action){
	//从action对象中获取type和data
	const {type,data} = action
	switch (type) {
		case 'increment': //如果是加
			return preState + data
		case 'decrement': //如果是减
			return preState - data
		default: //如果是初始化
			return preState
	}
}
```

---

### redux完整版写法

文件结构

index.js

```
import React from 'react'
import ReactDOM from 'react-dom';
import App from './App'
import store from './redux/store'

ReactDOM.render(<App/>,document.getElementById('root'))

//检测redux中状态的改变
store.subscribe(()=>{
	ReactDOM.render(<App/>,document.getElementById('root'))
})
```

App.jsx

```
import React, { Component } from 'react'
import Count from './components/Count'

export default class App extends Component {
	render() {
		return (
			<div>	
				<Count/>
			</div>
		)
	}
}
```

count组件

```
import React, { Component } from 'react'
import store from '../../redux/store'
import {
	createIncrementAction,
	createDecrementAction,
	createIncrementAsyncAction
} from '../../redux/count_action'

export default class Count extends Component {

	state = {name:'tom'}

	increment = ()=>{
		//获取用户选择的数字
		const {value} = this.checkNumber
		store.dispatch(createIncrementAction(value*1))
	}

	decrement = ()=>{
		//获取用户选择的数字
		const {value} = this.checkNumber
		store.dispatch(createDecrementAction(value*1))
	}

	incrementIfOdd = ()=>{
		//获取用户选择的数字
		const {value} = this.checkNumber
		if(store.getState() % 2 !== 0){
			store.dispatch(createIncrementAction(value*1))
		}
	}

	incrementAsync = ()=>{
		//获取用户选择的数字
		const {value} = this.checkNumber
		store.dispatch(createIncrementAsyncAction(value*1))
	}

	render() {
		return (
			<div>
				<h2>当前求和为：{store.getState()}</h2>
				<select ref={c => this.checkNumber = c}>
					<option value="1">1</option>
					<option value="2">2</option>
					<option value="3">3</option>
				</select>&nbsp;
				<button onClick={this.increment}>+</button>&nbsp;
				<button onClick={this.decrement}>-</button>&nbsp;
				<button onClick={this.incrementIfOdd}>奇数再+</button>&nbsp;
				<button onClick={this.incrementAsync}>异步+</button>
			</div>
		)
	}
}
```

constant.js
```
/* 
	该文件是常量模块，里面配置着所有的action中的type值
*/
export const INCREMENT = 'increment' //代表加
export const DECREMENT = 'decrement'//代表减
```

count_action.js

```
/* 
	该问文件是专门用于创建Count组件相关的action
*/
import {INCREMENT,DECREMENT} from './constant'

export const createIncrementAction = number =>({type:INCREMENT,data:number})

export const createDecrementAction = number =>({type:DECREMENT,data:number})

export function createIncrementAsyncAction(number){
	//异步action中，往往都会开启一个同步action
	return (dispatch)=>{
		setTimeout(()=>{
			dispatch(createIncrementAction(number))
		},500)
	}
}
```

count_reducer.js

```
//引入常量模块
import {INCREMENT,DECREMENT} from './constant'

export default function countReducer(preState=0,action){
	console.log('@@@');
	//从action对象中获取type和data
	const {type,data} = action
	switch (type) {
		case INCREMENT: //如果是加
			return preState + data
		case DECREMENT: //如果是减
			return preState - data
		default: //如果是初始化
			return preState
	}
}
```

store.js

```
/* 
	该文件是整个redux中最为核心的store对象
*/
//引入createStore，用于创建store对象
import {createStore,applyMiddleware} from 'redux'
//引入为Count组件服务的reducer，用于：初始化状态、加工状态
import countReducer from './count_reducer'
//引入thunk用于支持异步action
import thunk from 'redux-thunk'

//调用createStore创建并暴露store，注意：要传入为store服务的reducer
export default createStore(countReducer,applyMiddleware(thunk))
```

---

### 项目打包运行

项目根目录运行npm run build

把打包好的文件放入服务器中，浏览器中打开，就可以看到页面。


---

### React扩展

setState更新状态

![image](407E2FEC4B2F479AAF945F6201A64717)

组件实现点击按钮，count++

```
import React, { } from "react";

export default class App extends React.Component {
  state = {count: 0}
  add = () => {
    this.setState({
      count: this.state.count + 1
    })
  }
  render() {
    return (
      <div>
        <h1>当前求和为：{this.state.count}</h1>
        <button onClick={this.add}>点击count+1</button>
      </div>
    )
  }
  
}

```

```
import React, { } from "react";

export default class App extends React.Component {
  state = {count: 0}
  add = () => {
    // setState是异步执行的
    // setState可以传入回调函数，该回调函数是页面数据更新然后render执行完成后，调用
    this.setState({
      count: this.state.count + 1
    }, () => {
      console.log("@@@@", this.state.count)
    })
    console.log("add---", this.state.count)
  }
  render() {
    return (
      <div>
        <h1>当前求和为：{this.state.count}</h1>
        <button onClick={this.add}>点击count+1</button>
      </div>
    )
  }
  
}

```

```
import React, { } from "react";

export default class App extends React.Component {
  state = {count: 0}
  add = () => {
    // setState中可以直接传入一个参数，参数是一个函数，函数执行返回的值作为新的state
    // 函数可以传入2个参数，state代表组件的state属性，props代表传入组件的属性
    this.setState((state, props) => {
      return {count: state.count+1}
    })
  }
  render() {
    return (
      <div>
        <h1>当前求和为：{this.state.count}</h1>
        <button onClick={this.add}>点击count+1</button>
      </div>
    )
  }
  
}
```

---

### lazyLoad

https://www.bilibili.com/video/BV1wy4y1D7JT?p=117

---

### stateHook

https://www.bilibili.com/video/BV1wy4y1D7JT?p=118

---

### EffectHook

https://www.bilibili.com/video/BV1wy4y1D7JT?p=119

---

### refHook

https://www.bilibili.com/video/BV1wy4y1D7JT/?p=120

---

### Fragement

https://www.bilibili.com/video/BV1wy4y1D7JT?p=121

---

### context

https://www.bilibili.com/video/BV1wy4y1D7JT?p=122

---

### pureComponent

https://www.bilibili.com/video/BV1wy4y1D7JT?p=123

---

### renderProp

https://www.bilibili.com/video/BV1wy4y1D7JT?p=124

---

### errorBoundary






---

### React hook

利用类组件使用点击按钮，count+1。

```
import React from "react";

export default class App extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0,
    };
  }
  setCount = (count) => {
    this.setState({
      count: count + 1,
    });
  };
  render() {
    return (
      <div>
        <p>count: {this.state.count}</p>
        <button
          onClick={() => {
            this.setCount(this.state.count);
          }}
        >点我count+1</button>
      </div>
    );
  }
}
```

函数组件实现上面的案例

```
import React, { useState } from "react";

export default function App() {
  const [count, setCount ] = useState(0);
  return (
    <div>
      <p>count: {count}</p>
      <button
        onClick={() => {
          setCount(count + 1);
        }}
      >
        点我count+1
      </button>
    </div>
  );
}
```

---

### useState使用

```
import React, { useState } from "react";

export default function App() {
  // 定义一个响应式数据
  // count 的初始值是0
  // setCount是一个函数，传入新的count的值
  const [count, setCount ] = useState(0);
  const handleClick = () => {
    // setCount中可以传入函数，代表更新state的代码逻辑
    setCount( () => {
      if(count < 3) {
        return count + 1
      } else {
        return count + 2
      }
    })
  }
  return (
    <div>
      <p>count: {count}</p>
      <button onClick={handleClick}> 点我count+1 </button>
    </div>
  );
}
```

```
import React, { useState } from "react";

export default function App() {
  // 定义一个响应式数据
  // count 的初始值是0
  // setCount是一个函数，传入新的count的值
  const [count, setCount ] = useState(0);
  const [person, setPerson] = useState({
    name: 'mike',
    age: 18
  })
  const handleClick = () => {
    setCount(count+1)
    // 修改对象中的数据
    setPerson({
      ...person,
      age: person.age + 1
    })
  }
  return (
    <div>
      <p>count: {count}</p>
      <p>name: {person.name}</p>
      <p>age: {person.age}</p>
      <button onClick={handleClick}> 点我 </button>
    </div>
  );
}
```

---

### useState惰性初始化

```
import React, { useState } from "react";

export default function App() {
  // 定义一个响应式数据
  // count 的初始值是0
  // setCount是一个函数，传入新的count的值
  const [count, setCount ] = useState(0);
  const [person, setPerson] = useState({
    name: 'mike',
    age: 18
  })
  const handleClick = () => {
    setCount(count+1)
    // 修改对象中的数据
    setPerson({
      ...person,
      age: person.age + 1
    })
  }
  // 每一次组件里的响应式数据发生变化时，会重新调用App函数，重新渲染组件
  // 但是第二次渲染组件时，不会再次执行useState()来进行初始化
  console.log("App组件开始渲染")
  return (
    <div>
      <p>count: {count}</p>
      <p>name: {person.name}</p>
      <p>age: {person.age}</p>
      <button onClick={handleClick}> 点我 </button>
    </div>
  );
}
```

---


---

### useEffect

```
import React, { useEffect, useState } from "react";

export default function App() {
  // 定义一个响应式数据
  // count 的初始值是0
  // setCount是一个函数，传入新的count的值
  const [count, setCount ] = useState(0);
  const [person, setPerson] = useState({
    name: 'mike',
    age: 18
  })
  // 第一次会执行useEffect中的函数
  // 后面第二个参数中的数据发生变化时，执行回调
  useEffect(() => {
    console.log("count发生改变", count)
  },[count])
  const handleClick = () => {
    setCount(count+1)
    // 修改对象中的数据
    setPerson({
      ...person,
      age: person.age + 1
    })
    // 这里得到的count是更新之前的count值
    console.log("count--",count)
  }
  // 每一次组件里的响应式数据发生变化时，会重新调用App函数，重新渲染组件
  // 但是第二次渲染组件时，不会再次执行useState()来进行初始化
  console.log("App组件开始渲染")
  return (
    <div>
      <p>count: {count}</p>
      <p>name: {person.name}</p>
      <p>age: {person.age}</p>
      <button onClick={handleClick}> 点我 </button>
    </div>
  );
}
```

---

### useEffect实现生命周期函数

```
import React, { useEffect, useState } from "react";

export default function App() {
  // 定义一个响应式数据
  // count 的初始值是0
  // setCount是一个函数，传入新的count的值
  const [count, setCount ] = useState(0);
  const [person, setPerson] = useState({
    name: 'mike',
    age: 18
  })
  // 第一次会执行useEffect中的函数
  // 后面不在执行
  useEffect(() => {
    console.log("count发生改变")
  },[])
  const handleClick = () => {
    setCount(count+1)
    // 修改对象中的数据
    setPerson({
      ...person,
      age: person.age + 1
    })
    // 这里得到的count是更新之前的count值
    console.log("count--",count)
  }
  // 每一次组件里的响应式数据发生变化时，会重新调用App函数，重新渲染组件
  // 但是第二次渲染组件时，不会再次执行useState()来进行初始化
  console.log("App组件开始渲染")
  return (
    <div>
      <p>count: {count}</p>
      <p>name: {person.name}</p>
      <p>age: {person.age}</p>
      <button onClick={handleClick}> 点我 </button>
    </div>
  );
}
```

```
import React, { useEffect, useState } from "react";

export default function App() {
  // 定义一个响应式数据
  // count 的初始值是0
  // setCount是一个函数，传入新的count的值
  const [count, setCount ] = useState(0);
  const [person, setPerson] = useState({
    name: 'mike',
    age: 18
  })
  // 第一次会执行useEffect中的函数
  // 后面不在执行
  useEffect(() => {
    console.log("count开始挂载")
    return () => {
      console.log("count开始卸载")
    }
  },[])
  useEffect(() => {
    console.log("count重新挂载")
  },[count, person])
  const handleClick = () => {
    setCount(count+1)
    // 修改对象中的数据
    setPerson({
      ...person,
      age: person.age + 1
    })
    // 这里得到的count是更新之前的count值
    console.log("count--",count)
  }
  return (
    <div>
      <p>count: {count}</p>
      <p>name: {person.name}</p>
      <p>age: {person.age}</p>
      <button onClick={handleClick}> 点我 </button>
    </div>
  );
}
```

---

### useReducer

https://www.bilibili.com/video/BV15Y4y1z7Fc?p=8

---

### useCallback

```
import React, { useCallback, useEffect, useState } from "react";

export default function App() {
  // 定义一个响应式数据
  // count 的初始值是0
  // setCount是一个函数，传入新的count的值
  const [count, setCount ] = useState(0);
  
  // 当第二个参数的数据发生改变时，执行useCallback第一个参数的函数
  const handleClick = useCallback(() => {
    console.log("useCallback function----",count)
    setCount(count+1)
  },[count])

  return (
    <div>
      <p>count: {count}</p>
      <button onClick={handleClick}> 点我 </button>
    </div>
  );
}
```

```
import React, { useCallback, useEffect, useState } from "react";

export default function App() {
  // 定义一个响应式数据
  // count 的初始值是0
  // setCount是一个函数，传入新的count的值
  const [count, setCount ] = useState(0);
  
  // 当第二个参数的数据发生改变时，执行useCallback第一个参数的函数
  const handleClick = useCallback(() => {
    setCount(count+1)
  },[count])

  return (
    <div>
      <p>count: {count}</p>
      <button onClick={handleClick}> 点我 </button>
      <hr/>
      <Son/>
    </div>
  );
}

function Son(props) {
  console.log("Son组件开始渲染")
  return (
    <div>
      <p>son 组件</p>
    </div>
  );
}
```

每一次父组件发生更新时，即使子组件中状态未发生改变，也会重新渲染，这有点浪费。

```
import React, { useCallback, useEffect, useState } from "react";

export default function App() {
  // 定义一个响应式数据
  // count 的初始值是0
  // setCount是一个函数，传入新的count的值
  const [count, setCount ] = useState(0);
  const [name, setName ] = useState("mike");
  const handleClick = () => {
    setCount(count+1)
  }
  const handleChangeName = () => {
    setName(name + "!")
  }
  return (
    <div>
      <p>count: {count}</p>
      <p>name: {name}</p>
      <button onClick={handleClick}> 点我 </button>
      <button onClick={handleChangeName}> 点我改变name </button>
      <hr/>
      <Son count={count}/>
    </div>
  );
}

// 传入Son组件的props如果不更新的话，Son组件不会重新渲染
const Son = React.memo(
  function Son(props) {
    console.log("Son组件开始渲染")
    return (
      <div>
        <p>son 组件</p>
      </div>
    );
  }
)
```

---

### useMemo

```
import React, { useCallback, useEffect, useMemo, useState } from "react";

export default function App() {
  const [a, setA] = useState(0)
  const [b, setB] = useState(0) 
  const [d, setD] = useState(0) 
  const handleAdd1 = () => {
    setA(a+1)
  }
  const handleAdd2 = () => {
    setB(b+1)
  }
  const handleAdd3 = () => {
    setD(d+1)
  }
  // 当第二个依赖的数据列表中的数据值发生改变时，执行第一个参数函数，并将返回的值赋值给c
  const c = useMemo(() => {
    console.log("计算c的值")
    return a + b
  }, [a, b])
  return (
    <div>
      <p>a: {a}</p>
      <p>b: {b}</p>
      <p>c: {c}</p>
      <button onClick={handleAdd1}> 点我a+1 </button>
      <button onClick={handleAdd2}> 点我b+1 </button>
      <button onClick={handleAdd3}> 点我d+1 </button>
      <hr/>
    </div>
  );
}

```

```
import React, { useCallback, useEffect, useMemo, useState } from "react";

export default function App() {
  const [a, setA] = useState(0)
  const [b, setB] = useState(0) 
  const [d, setD] = useState(0) 
  const handleAdd1 = () => {
    setA(a+1)
  }
  const handleAdd2 = () => {
    setB(b+1)
  }
  const handleAdd3 = () => {
    setD(d+1)
  }
  // 
  const c = useMemo(() => {
    console.log("计算c的值")
    // 返回dom
    return (
      <div>
        {a+b}
        <p>dom</p>
      </div>
    )
  }, [a, b])
  return (
    <div>
      <p>a: {a}</p>
      <p>b: {b}</p>
      <p>c: {c}</p>
      <button onClick={handleAdd1}> 点我a+1 </button>
      <button onClick={handleAdd2}> 点我b+1 </button>
      <button onClick={handleAdd3}> 点我d+1 </button>
      <hr/>
    </div>
  );
}

```

---

### react扩展

https://www.bilibili.com/video/BV1wy4y1D7JT?p=116

到

https://www.bilibili.com/video/BV1wy4y1D7JT?p=126

---

### react-router6

https://www.bilibili.com/video/BV1wy4y1D7JT?p=127

到

https://www.bilibili.com/video/BV1wy4y1D7JT?p=141

---






























