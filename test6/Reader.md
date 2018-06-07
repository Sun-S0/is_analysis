<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 基于GitHub的实验管理平台的分析与设计

### 成都大学信息科学与工程学院

|学号|班级|姓名|照片|
|:-------:|:-------------: | :----------:|:---:|
|201510414405|软件(本)15-4|胡硕明|![](photo.jpg)|

## 1. 概述
- 基于GitHub的实验管理平台的作用是在线管理实验成绩的Web应用系统。学生和老师的实验内容均存放在GitHUB
页面上。
- 学生的功能主要有：

-       1.查看个人资料以及修改个人资料
        2.查看某个学期的课程成绩（只能查询自己的成绩）
        3.查看当前学期的可选课程
        4.查看某个学期的实验内容
        
- 老师的功能主要有：

-       1.查看个人资料以及修改个人资料
        2.维护自己任教的课程以（管理实验内容）
        3.查看学生成绩以及评定成绩
        4.查看当前学期可任教的课程
- 老师和学生都能通过本系统的链接方便地跳转到学生的每个GitHUB实验目录，以便批改实验或者查看实验情况。
- 实验成绩按每个单项成绩计算，计算出分项成绩总和为本次实验的总成绩，每项实验的满分为100分，最低为0分。
- 系统自动计算每个学生的所有实验的平均分。
    
## 2. 系统总体结构
![](系统分析图.png)

界面设计参见：https://Sun-So.github.io/is_analysis/test6/src/ui/index.html
    
## 3. 用例图设计 [源码](src/WebUserCase.puml)
![](WebUserCase.png)

## 4. 类图设计 [源码](src/class.puml)
![](class.png)

## 5. 数据库设计
- ### [参见数据库设计](./数据库设计.md)

## 6. 用例及界面详细设计
- ### [“登陆”用例](./用例/学生列表.md),[界面](https://Sun-So.github.io/is_analysis/test6/ui/index.html)
- ### [“登出”用例](./用例/评定成绩.md),[界面](https://Sun-So.github.io/is_analysis/test6/ui/评定成绩.html)
- ### [“查看个人资料”用例](./用例/查看成绩.md),[界面](https://zwdbox.Sun-So.io/is_analysis/test6/ui/查看成绩.html)
- ### [“修改个人资料”用例](./用例/修改密码.md),[界面](https://zwdbox.Sun-So.io/is_analysis/test6/ui/顶部菜单.html)
- ### [“修改密码”用例](./用例/修改用户信息.md),[界面](https://zwdbox.Sun-So.io/is_analysis/test6/ui/顶部菜单.html)
- ### [“学生列表”用例](./用例/查看用户信息.md),[界面](https://zwdbox.Sun-So.io/is_analysis/test6/ui/顶部菜单.html)
- ### [“查看成绩”用例](./用例/登出.md),[界面](https://Sun-So.github.io/is_analysis/test6/ui/顶部菜单.html)
- ### [“评定成绩”用例](./用例/登录.md),[界面](https://Sun-So.github.io/is_analysis/test6/ui/登录.html)
- ### [“选择学期”用例](./用例/登录.md),[界面](https://Sun-So.github.io/is_analysis/test6/ui/登录.html)
- ### [“实验内容”用例](./用例/登录.md),[界面](https://Sun-So.github.io/is_analysis/test6/ui/登录.html)
- ### [“管理实验”用例](./用例/登录.md),[界面](https://Sun-So.github.io/is_analysis/test6/ui/登录.html)
- ### [“老师选课”用例](./用例/登录.md),[界面](https://Sun-So.github.io/is_analysis/test6/ui/登录.html)
- ### [“学生选课”用例](./用例/登录.md),[界面](https://Sun-So.github.io/is_analysis/test6/ui/登录.html)

    