<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getTestContent  [返回](../README.md)
用例： [查看实验内容](../用例/查看实验内容.md)

- 功能：
    获取学生的在修课程中的所有实验内容以及实验要求。
    
- 权限：
    学生：可以查看该门课程的所有实验内容
    
- API请求地址： 
    接口基本地址/v1/api/getTestContent

- 请求方式 ：
    POST
- 请求实例：

        {
            "Term_id": "201511",
            "course_id": "10086"
            "student_id: "201510414405"
        }
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |Term_id|学期编号|
  |course_id|课程代码|
  |student_id|学生的学号|
    
- 返回实例：

        {         
            "status": true,
            "info": null,    
            "credit": "3.5", 
            "course_name": "软件系统分析", 
            "tests_num":2 ,   
            "tests data": [
                {
                "test_id":01,
                "test_name": "图书管理系统类图", 
                "test_stand":"类图中完善功能结构，清晰",
                "final_date": "2018-06-01",
                "single point":[
                {
                    "point_id": 01
                    "point_Maxresult": 20,
                    "point_project": "功能完善"
                   
                },
                {
                    "point_id": 02
                    "point_Maxresult": 15,
                    "point_project": "界面设计"
                                   
                 },
                
                ]
                }, 
                {
               "test_id":02,
                "test_name": "建立数据库表", 
                "test_stand":"数据表中要有xx,xx,xx属性",
                "final_date": "2018-06-20",
                "single point":[
                {
                    "point_id": 01
                    "point_Maxresult": 18,
                    "point_project": "数据表完整"
                   
                },
                {
                    "point_id": 02
                    "point_Maxresult": 15,
                    "point_project": "数据表合理"
                                   
                 }，
				                {
                    "point_id": 03
                    "point_Maxresult": 60,
                    "point_project": "数据表xx"
                                   
                 }
                
                ]
                }
            ] 
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |student_id|学号|
  |class|班级|
  |name|真实姓名|   
  |total|实验总数|
  |avg_result|实验平均成绩|   
  |data|所有实验的成绩和评语|
  |point_id|评分项编号|
  |test_name|实验名称|
  |test_stand|实验标准要求|
  |final_date|实验截止时间|
  |point_Maxresult|单个评分项分数满分|
  |point_project|评分项|
  |credit|学分|  
  |course_name|课程名称|
 
  
  


