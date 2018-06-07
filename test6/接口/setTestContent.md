<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：setTestContent[返回](../README.md)
用例： [管理实验内容](../用例/管理实验内容.md)

- 功能：
    对任教课程的实验内容进行增删改操作，管理课程实验内容。
    
- 权限：
    老师：可以对实验内容进行编辑，增加实验或者删除实验。
    
- API请求地址： 
    接口基本地址/v1/api/setTestContent

- 请求方式 ：
    POST
- 请求实例：

        {
 			 
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
                    "point_project": "数据表合理"
                   
                },
                {
                    "point_id": 02
                    "point_Maxresult": 15,
                    "point_project": "数据表完整"
                                   
                 }
                
                ]
                }
            ] 
        }
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |tests_num|实验总数|
  |test data|所有实验内容的数据集合|
  |point_id|评分项编号|
  |test_name|实验名称|
  |single point|评分项数据集合|
  |test_stand|实验标准要求|
  |final_date|实验截止时间|
  |point_Maxresult|单个评分项分数满分界限|
  |point_project|评分项|
  |course_name|课程名称|
    
- 返回实例：

        {         
            "status": true,
            "info":"保存成功，重新刷新页面查看"   
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|  

 
  
  


