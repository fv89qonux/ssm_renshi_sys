## 本项目实现的最终作用是基于SSM公司人事管理系统
## 分为1个角色
### 第1个角色为管理员角色，实现了如下功能：
 - 公告管理
 - 员工管理
 - 文档管理
 - 用户管理
 - 管理员登录
 - 职位管理
 - 部门管理
## 数据库设计如下：
# 数据库设计文档

**数据库名：** ssm_renshi_sys

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [dept_inf](#dept_inf) |  |
| [document_inf](#document_inf) |  |
| [employee_inf](#employee_inf) |  |
| [job_inf](#job_inf) |  |
| [notice_inf](#notice_inf) |  |
| [user_inf](#user_inf) |  |

**表名：** <a id="dept_inf">dept_inf</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | name |   varchar   | 255 |   0    |    N     |  N   |       | 名字  |
|  3   | remark |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 备注  |

**表名：** <a id="document_inf">document_inf</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | title |   varchar   | 255 |   0    |    N     |  N   |       | 标题  |
|  3   | filename |   varchar   | 255 |   0    |    N     |  N   |       | 文件名  |
|  4   | remark |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 备注  |
|  5   | CREATE_DATE |   timestamp   | 19 |   0    |    N     |  N   |   current_timestamp()    |   |
|  6   | user_id |   int   | 10 |   0    |    Y     |  N   |   NULL    | 用户ID  |

**表名：** <a id="employee_inf">employee_inf</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | DEPT_ID |   int   | 10 |   0    |    N     |  N   |       |   |
|  3   | JOB_ID |   int   | 10 |   0    |    N     |  N   |       |   |
|  4   | name |   varchar   | 255 |   0    |    N     |  N   |       | 名字  |
|  5   | CARD_ID |   varchar   | 18 |   0    |    N     |  N   |       |   |
|  6   | ADDRESS |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  7   | POST_CODE |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  8   | TEL |   varchar   | 16 |   0    |    Y     |  N   |   NULL    |   |
|  9   | PHONE |   varchar   | 11 |   0    |    N     |  N   |       |   |
|  10   | QQ_NUM |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  11   | email |   varchar   | 255 |   0    |    N     |  N   |       | 邮箱  |
|  12   | SEX |   int   | 10 |   0    |    N     |  N   |   1    |   |
|  13   | PARTY |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  14   | BIRTHDAY |   datetime   | 19 |   0    |    Y     |  N   |   NULL    |   |
|  15   | RACE |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  16   | education |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 教育经历  |
|  17   | SPECIALITY |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  18   | HOBBY |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  19   | remark |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 备注  |
|  20   | CREATE_DATE |   timestamp   | 19 |   0    |    N     |  N   |   current_timestamp()    |   |

**表名：** <a id="job_inf">job_inf</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | name |   varchar   | 255 |   0    |    N     |  N   |       | 名字  |
|  3   | remark |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 备注  |

**表名：** <a id="notice_inf">notice_inf</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | title |   varchar   | 255 |   0    |    N     |  N   |       | 标题  |
|  3   | CONTENT |   text   | 65535 |   0    |    N     |  N   |       |   |
|  4   | CREATE_DATE |   timestamp   | 19 |   0    |    N     |  N   |   current_timestamp()    |   |
|  5   | user_id |   int   | 10 |   0    |    Y     |  N   |   NULL    | 用户ID  |

**表名：** <a id="user_inf">user_inf</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | loginname |   varchar   | 255 |   0    |    N     |  N   |       | 登录名称  |
|  3   | PASSWORD |   varchar   | 16 |   0    |    N     |  N   |       |   |
|  4   | STATUS |   int   | 10 |   0    |    N     |  N   |   1    |   |
|  5   | createdate |   timestamp   | 19 |   0    |    N     |  N   |   current_timestamp()    |   |
|  6   | userName |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 用户名  |

