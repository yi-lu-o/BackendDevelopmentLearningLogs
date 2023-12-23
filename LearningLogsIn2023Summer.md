# 2023年夏天后端开发踩坑记录

## 2023年7月25日

1.在tomcat访问文件的过程中没有把待访问文件放在webapp的直接子目录下，导致原地打转了近1h

## 2023年8月1日

问题1:在学习请求响应（Request&Response）时，无法通过前端表单页面(html)跳转到后端Servlet类

原因分析：Servlet类的路径设置错误,对于HTML中的form标签中action属性的设置

问题2：在制作登录页面时，mybatis的数据库url路径设置错误，要学会慢慢的看报错信息

## 2023年8月2日

问题1：个人管理系统查询功能的开发遇到困难，不知道如何把前后端的技术融合起来！！！

问题2：踩踩踩大坑啦！！！jsp页面${}中无法显示内容，原因定位错误，以为是ResultMap的问题，绕了一个大圈

原因是：JSP和Servlet版本导致el功能默认关闭，加入<%@page isELIgnored="false"%>标签手动开启el功能。

启示：要善于描述问题，用搜索引擎解决问题呀！！！

## 2023年8月3日

问题1：servlet登录问题Status 500 - Error instantiating servlet class 

解决：包路径写错“com.YiluLearner”!="com.YiLuLearner"

## 2023年8月9日

问题1：用spring框架整合mybatis时出现问题

解决方法：UserDao.class和UserDaoMapper.xml没有一一对应，应该将UserDaoMapper.xml改为UserDao.xml

