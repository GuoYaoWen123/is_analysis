<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：setTeacherCourses  [返回](../README.md)
用例： [学生选课](../用例/教师选课.md)

- 功能：
    教师选择课程进行教学活动。
    
- 权限：
    老师：可以查看自己已选课程所有学生的选课情况。
    
- API请求地址： 
    接口基本地址/v1/api/setTeacherCourses

- 请求方式 ：
    POST
 
- 请求实例：  
        { 
            "teacher_id": "123456",
            "total": 4,
            "data": [
                {
                "courses_id":1,
                "courses_name":信息系统分析与设计, 
                "courses_coll":"信息科学与工程学院",
                }, 
                {
                ...其他课程
                }
            ] 
        }

- 请求参数说明:       
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |teacher_id|教师编号|
  |total|本次显示的课程信息|
  |data|课程信息|
  |courses_id|课程编号|
  |courses_name|课程名字|
  |courses_coll|开课学院| 
  
  
 
- 返回实例：

        {         
            "status": true,
            "info": null
        }

- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|


