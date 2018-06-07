<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getUserInfo  [返回](../README.md)
用例： [查看用户信息](../用例/查看用户信息.md),[修改用户信息](../用例/修改用户信息.md)

- 功能：
    查看用户的所有信息。
    
- 权限：
    学生/老师：查看自己的信息，必须先登录，不能查看其他用户的信息。    
    
- API请求地址： 
    接口基本地址/v1/api/getUserInfo/<user_id>

- 请求方式 ：
    GET
- 请求实例
        {         
           
                "user_id":"201510414405",    
         
        }
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |user_id|用户的ID号。对应表USERS.USER_ID的值|
  
- 返回实例：

        {         
                "status": true,
                "info": null,   
                "name":"胡硕明",
                "github_username":"Sun-So",
                "type":"学生",
                "student": {
                    "student_id": "201510414405",
                    "grade": "2015",
                    "profession": "软件工程",
         
            
            }          
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |name|用户的真实姓名|  
  |github_username|gitHub用户名|
  |type|用户类型：老师或者学生|
  |student_id|学号|
  |grade|年级|
  |profession|在读专业|
  |class|班级|
  |result_sum|成绩汇总|
  |web_sum|网站正确与否汇总|
  |teacher_id|老师工号|
  |department|老师所属部门|

