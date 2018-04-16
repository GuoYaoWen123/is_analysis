

实验三：图书管理系统领域对象建模
----------------
##### 流程一：借书记录
##### uml源码如下
````
@startuml

object order {
	 	读者姓名 = "郭耀文"
	 	图书ISBN号 = "11-22-33
	 	借出时间 = "2015-10-10"
	 	归还期限 = "2019-46-20"
}


@endumlml

````
![借书记录](https://github.com/GuoYaoWen123/is_analysis/blob/master/test3/借书记录.png）


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
	 	简介 = "四川省德阳市"
	 	作者 = "林俊杰"
	}

@endumll
````
![图书对象](https://github.com/748580573/is_analysis/blob/master/test3/%E5%9B%BE%E4%B9%A6%E5%AF%B9%E8%B1%A1.png)


##### 流程三：游客对象

````
@startuml
 object visitor{
    查询图书信息
    注册账号
 }
@enduml
````
！[游客对象](https://github.com/748580573/is_analysis/blob/master/test3/%E6%B8%B8%E5%AE%A2%E5%AF%B9%E8%B1%A1.png)


##### 流程四：管理员对象

````
@startuml

object libraryManager {
		 username = "mr"
		 password = "guoyaowen"
}


@enduml
````
![管理员对象](https://github.com/748580573/is_analysis/blob/master/test3/%E7%B3%BB%E7%BB%9F%E5%AF%B9%E8%B1%A1.png)



##### 流程五：系统对象

````
@startuml



package "library" #DDDDDD {

object reader {
	 	username = "mrwuqwe"
		password = "qweqw"
	}
	object visitor {
		注册账号
	}

	object 图书管理员 {
		 username = "mrqwq"
		 password = "wuqweqwe"
	}



	

	object book {
	 	书名 = "信息系统分析与设计"
	 	ISBN号 = "123-321-121-321"
	 	总量 = "500"
	 	库存 = "400"
	 	价格 = "19"
	 	出版社 = "科学出版社"
	 	简介 = "成都大学"
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

![](https://github.com/748580573/is_analysis/blob/master/test3/%E7%B3%BB%E7%BB%9F%E5%AF%B9%E8%B1%A1.png)

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
![系统类](https://github.com/748580573/is_analysis/blob/master/test3/%E7%B3%BB%E7%BB%9F%E7%B1%BB.png)

##### 

##### 流程七：读者对象

````
@startuml
	object reader {
	 	username = "cxz"
		password = "123"
	}
@enduml
````
![读者对象](https://github.com/748580573/is_analysis/blob/master/test3/%E8%AF%BB%E8%80%85%E5%AF%B9%E8%B1%A1.png)
