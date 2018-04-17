

实验三：图书管理系统领域对象建模
----------------
##### 流程一：借书记录
##### uml源码如下
````
@startuml

object order {
	 	读者姓名 = "郭耀文"
	 	图书ISBN号 = "11-22-33
	 	借出时间 = "2015-6-10"
	 	归还期限 = "2019-8-20"
}


@endumlml

````
![借书记录](https://github.com/GuoYaoWen123/is_analysis/blob/master/test3/借书记录.png)


流程三
````
@startuml

	object book {
	 	 书名 = "信息系统分析与设计"
	 	ISBN号 = "123-321-123-321"
	 	总量 = "500"
	 	库存 = "400"
	 	价格 = "19"
	 	出版社 = "科学出版社"
	 	简介 = "您好"
	 	作者 = "林俊杰"
	}

@endumll
````
![图书对象](https://github.com/GuoYaoWen123/is_analysis/blob/master/test3/图书对象.png)


##### 流程三：游客对象

````
@startuml
 object visitor{
    查询图书信息
    注册账号
 }
@enduml
````
！[游客对象](https://github.com/GuoYaoWen123/is_analysis/blob/master/test3/游客对象.png)


##### 流程四：管理员对象

````
@startuml

object libraryManager {
		 username = "郭先生"
		 password = "郭耀文"
}


@enduml
````
![管理员对象](https://github.com/GuoYaoWen123/is_analysis/blob/master/test3/读者对象.png)
 
 
 说明：与读者对象代码大同小异，故此处引用读者对象截图


##### 流程五：系统对象

````
@startuml



package "library" #DDDDDD {

object reader {
	 	username = "郭先生"
		password = "郭耀文"
	}
	object visitor {
		注册账号
	}

	object 图书管理员 {
		 username = "mrguo"
		 password = "郭文"
	}



	

	object book {
	 	书名 = "信息系统分析与设计"
	 	ISBN号 = "123-321-121-321"
	 	总量 = "500"
	 	库存 = "400"
	 	价格 = "19"
	 	出版社 = "科学出版社"
	 	简介 = "您的世界"
	 	作者 = "林俊杰"
	}

	object order {
	 	读者姓名 = "csh"
	 	图书ISBN号 = "66-29-66"
	 	借出时间 = "2018-4-10"
	 	归还期限 = "2018-4-20"
	}

	

}


@enduml
````

![系统对象](https://github.com/GuoYaoWen123/is_analysis/blob/master/test3/系统对象.png)

##### 记录如下

##### 流程六：系统类
##### uml源码如下
````
@startuml

package "library" #DDDDDD {

	class librarymManager {

		+维护图书()
		+归还图书()
		+借还图书()
		+维护读者信息()
	}
	class reader {

		+查询借阅图书信息()
		+预订图书()
		+取消预订图书()
	}
	class visitor {
		+查询图书信息()
	}

	class book {
	 	-书名
	 	-ISBN号
	 	-总量
	 	-库存
	 	-价格
	 	-出版社
	 	-简介
	 	-作者
	}

	class order {
	 	-读者姓名
	 	-图书ISBN号
	 	-借出时间
	 	-归还期限
	}	 


}


@enduml
````
![系统类](https://github.com/GuoYaoWen123/is_analysis/blob/master/test3/系统类.png)

##### 

##### 流程七：读者对象

````
@startuml
	object reader {
	 	username = "郭先生"
		password = "郭耀文"
	}
@enduml
````
![读者对象](https://github.com/GuoYaoWen123/is_analysis/blob/master/test3/读者对象.png)
