

## 用户接口文档 ##

###1.用户注册接口###

**地址：**
http://localhost:8080/designShop/user/register

**入参：**
{
"userName":"朱敬国",
"loginName":"zhujg",
"passww":"123456789",
"email":"15765517018@163.com",
"sex":"0",
"tel":"15765517018"
}

**返回值：**
{
"code":0,
"info":"注册成功!"
}

### 2.用户登录接口 ###

**地址：**
http://localhost:8080/designShop/user/login

**入参：**
{
"loginName":"zhujg",
"passww":"123456789"
}

**返回值：**
{
"code": 0,
"info": "登录成功！",
"retObj": {
"createTime": 1503993557000,
"email": "15765517018@163.com",
"loginName": "zhujg",
"passww": "",
"roleId": "1001",
"sex": "0",
"tel": "15765517018",
"uId": 1,
"updateTime": 1503993557000,
"userName": "朱敬国",
"userStatus": "1"
}

### 3.修改用户接口 ###

**地址：**
http://localhost:8080/designShop/user/update

**入参：**
{
"userName":"朱敬国",
"email":"15765517018@163.com",
"tel":"15765517018",
"sex":"1"
}

**返回值：**
{
"code":0,
"info":"修改成功！"
}

### 4.注销接口 ###

**地址：**
http://localhost:8080/designShop/user/logout

**入参：**
{}

**返回值：**
{
"code":0,
"info":"注销成功！"
}

### 5.通过用户ID查询用户个人信息接口 ###

**地址：**
http://localhost:8080/designShop/user/queryUserByuId

**入参：**
{}

**返回值：**
{
"code": 0,
"info": "查询成功！",
"retObj": {
"createTime": 1503993557000,
"email": "15765517018@163.com",
"loginName": "zhujg",
"passww": "25f9e794323b453885f5181f1b624d0b",
"roleId": "1001",
"sex": "1",
"tel": "15765517018",
"uId": 1,
"updateTime": 1503993557000,
"userName": "朱敬国",
"userStatus": "1"
}


##地址接口文档##

###1.通过用户ID查询地址列表###

**地址：**
http://localhost:8080/designShop/addr/getAddrByUserId

**入参：**
{}

需要sessionID

**返回值：**
{"code":0,"info":"查询成功","retObj":[{"addrDesc":"北京市昌平区沙河","addrId":1,"addrPerson":"朱敬国","addrTel":"18611339434","createTime":1505878299000,"updateTime":1505878299000,"userId":1}]}
###2.通过地址ID修改地址信息###

**地址：**
http://localhost:8080/designShop/addr/updateAddrByAddrId

**入参：**
{
"addrId":"1","addrPerson":"朱敬国","addrTel":"18611339434","addrDesc":"北京市昌平区沙河"}

**返回值：**
{"code":0,"info":"修改成功"}
###3.通过地址ID获取地址详细信息###

**地址：**
http://localhost:8080/designShop/addr/getAddrByAddrId

**入参：**
{addrId: "1"}

**返回值：**
{"code":0,"info":"查询成功","retObj":{"addrDesc":"北京市昌平区","addrId":1,"addrPerson":"朱敬国","addrTel":"18611339434","createTime":1505878299000,"updateTime":1505878299000,"userId":1}}
###4.添加地址###

**地址：**
http://localhost:8080/designShop/addr/addAddr

**入参：**
{
"addrPerson":"朱敬国",
"addrTel":"18611339434",
"addrDesc":"北京市昌平区"
}

需要sessionID

**返回值：**
{"code":0,"info":"添加成功"}

###5.通过地址ID删除地址###

**地址：**
http://localhost:8080/designShop/addr/delAddr

**入参：**
{"addrId":"1"}

**返回值：**
{"code":0,"info":"删除成功"}
