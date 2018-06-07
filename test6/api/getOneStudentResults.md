<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getOneStudentResults  [返回](../README.md)
用例： [查看成绩](../用例/查看成绩.md)

- 功能：
    返回一个学生的所有实验成绩和实验评价。
    
- 权限：
    学生：只能查看自己的成绩，即接口参数student_id必须等于登录学生的student_id
    老师：可以查看所有学生的成绩。
    
- API请求地址： 
    接口基本地址/v1/api/getOneStudentResults/<student_id>

- 请求方式 ：
    POST
- 请求实例：

        {
            "Term_id": "20151011",
            "course_id": "10086"
            "student_id: "2015104144xx"
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
            "student_id": "2015104144xx", 
            "github_username": "hushuoming", 
            "grade": "2015", 
            "profession": "软件工程4", 
            "result_sum": 98,
            "avg_result":96.5, 
            "tests_num":2 ,   
            "tests data": [
                {
                "test_id":01,
                "web_exists": true, 
                "result": 98, 
                "memo":"本实验实现得思路清晰，框架完善，数据表合理",
                "update_date": "2018-05-01 23:02",
                "single point":[
                {
                    "point_id": 01
                    "point_result": 20,
                    "point_memo": "系统某个部分设置得不好，需重新架构"
                   
                },
                {
                    "point_id": 02
                    "point_result":15, 
                    "point_memo": "清晰，合理，美观"
                                   
                 },
                
                ]
                }, 
                {
                  "test_id":02,
                  "web_exists": true, 
                  "result": 95, 
                  "memo":"本实验做得好",
                  "update_date": "2018-04-01 13:02"
                "single point":[
                {
                    "point_id": 01
                    "point_result": 18,
                    "point_memo": "数据表xx地方不合理"
                   
                },
                {
                    "point_id": 02
                    "point_result":15, 
                    "point_memo": "类图思路清晰，合理"
                                   
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
  |github_username|学生的gitHub用户名|
  |class|班级|
  |name|真实姓名|   
  |tests_num|实验总数|
  |avg_result|实验平均成绩|   
  |data|所有实验的成绩和评语|
  |test_id|实验编号|
  |web_exists|本实验的GitHub网页是否存在|
  |result|本实验成绩，可以为空，为空表示没有批改，没有批改的实验不入平均成绩，为0分则要计入平均成绩，所以成绩为空和为0是不一样的。|
  |memo|本实验老师的评价，可以为空|
  |update_date|本实验老师的批改日期，可以为空|
  |single_point|多项评分数据|
  |point_id|评分项编号|
  |point_memo|单个评分项的评语|
  |point_result|单个评分项得分|
 
  
  


