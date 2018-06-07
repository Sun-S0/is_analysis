# 接口：SelectCourse  [返回](../../README.md)
用例： [选课](../用例/选课.md)

- 功能：
    学生，老师可以选择本学期的课程
    
- 权限：
    学生,老师：需要先登录系统，老师优先选择课程，学生选课页面才开放权限
    
- API请求地址： 
    接口基本地址/v1/api/SelectCourse

- 请求方式 ：
    POST

- 请求实例：

        {
			"name":"胡硕明"
			"grade":"2015"
			"profession":"软件工程"
            "student_id":"201510414405"
			
        }
        
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |name|姓名|
  |grade|年级|
  |profession|专业|
  |student_id|学生学号|
 
  
- 返回实例：

           "status": true,
            "info": null,    
            "Course_num":2 ,   
            "data": [
                {
                "course_id":8866,
                "course_name": "大数据, 
                "credit": 4.5, 
                "course_hour":"88",
                "name": "Kobe",
                   
                },
                {
                "course_id":9999,
                "course_name": "人工智能", 
                "credit": 5, 
                "course_hour":"60",
                "name": "Cna",
            ] 
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |data|返回主体信息JSON串|
  |course_id|课程代码|
  |course_name|课程名字|
  |credit|学分|
  |course_hour|学时|
  |name|教师名字|
