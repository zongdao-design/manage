[![Donate](http://www.zongdaosoft.com/static/index/images/logo.png)](http://www.zongdaosoft.com/)
# ApiDoc接口文档编写规范  
#### 作者：[RanChao]() 版本：[v1.0.0]()
### **前言**
 团队合作或者是项目对接，接口文档是非常重要的，一般接口文档都是通过开发人员写的。一个工整规范的文档显得是非重要。
### **什么是接口文档？**
在项目开发中，web项目的前后端分离开发，APP开发，需要由前后端工程师共同定义接口，编写接口文档，之后大家都根据这个接口文档进行开发，到项目结束前都要一直维护。  
### **为什么要写接口文档？**
1、项目开发过程中前后端工程师有一个统一的文件进行沟通交流开发  
2、项目维护中或者项目人员更迭，方便后期人员查看、维护  
### **ApiDoc常用参数模拟**
#### @api  
HTTP接口调用方法、路径及名称
```
@api post /user/list 01.分页查询
```
#### @apiGroup
api 分组
```
@apiGroup 用户管理
```
#### @apiVersion
api 版本号
```
@apiVersion 1.0.0
```
#### @apiDescription
apiDescription 接口描述
```
@apiDescription 分页查询用户信息
```
#### @apiParam
请求参数
```
@apiParam {Int} currpage 当前页
@apiParam {Int} count 每页多少条
@apiParam {String} key 关键字，编号/名称模糊查询
...
```
#### @apiSuccess
返回数据描述
```
@apiSuccess {String} status 状态，0正常，1异常
@apiSuccess {String} msg 消息，异常时的错误消息
@apiSuccess {Object[]} data 数组对象
@apiSuccess {String} data.id 主键
...
```
#### @apiParamExample
接口入参示例
```
@apiParamExample 入参示例
    {
        "currpage":"1",
        "count","20",
        ...
     }
```
#### @apiSuccessExample
接口成功返回样例
```
@apiSuccessExample 正确示例
    {
        "status":"0",
        "msg","",
        "data":[
            {
                "id":"1",
                "user_name":"小琳",
                ...
            }
        ]
     }
```
#### @apiErrorExample
接口失败返回样例
```
@apiErrorExample 错误示例
    {
        "status":"1",
        "msg":"错误的消息提示~"
    }
```
#### @apiDefine
类似于宏定义，可以被引用
```
@apiDefine BaseUserName 用户管理 
    ...
```
#### @apiUse
使用@apiDefine定义的描述
```
@apiUse BaseUserName
```
更详细的说明请参考官方文档http://apidocjs.com
#### 生成文档
cd到apidoc.json所在路径（即项目根目录）执行如下命令apidoc -i src/ -o apidoc/即可。
```
{
  "name": "API文档",
  "version": "1.0.0",
  "description": "***的***服务api文档",
  "title": "***平台API开放平台（***服务）",
  "url" : "http://ip:端口/***",
  "generate":"如何打包生成cd E:\\Workspaces\\***\\*** apidoc -i ***/ -o apidoc/***/"
}
```
#### 示例
完整的一个接口文档的示例及展示效果
```
/**
    * @api {post} /user/list 01.分页查询
    * @apiGroup 用户管理
    * @apiVersion 1.0.0
    * @apiDescription 分页查询用户信息
    * @apiParam {Int} currpage 当前页
    * @apiParam {Int} count 每页多少条
    * @apiParam {String} [key] 关键字，编号/名称模糊查询
    * @apiSuccess {String} status 状态，0正常，1异常
    * @apiSuccess {String} msg 消息，异常时的错误消息
    * @apiSuccess {Object[]} data 对象
    * @apiSuccess {String} data.id 用户id，主键
    * @apiSuccess {String} data.user_name 用户名称
    * @apiSuccess {String} data.account 用户账户
    * @apiSuccess {String} data.remark 备注
    * @apiParamExample 入参示例
    *   {
    *       "currpage":"1",
    *       "count":"20",
    *       "key":"小"
    *   }
    * @apiSuccessExample 正确示例
    *   {
    *       "status":"0",
    *       "msg":"",
    *       "data":[
    *           {
    *               "id":"1",
    *               "user_name":"小林",
    *               "account":"wanglin",
    *               "remark":"备注"
    *           }
    *       ]
    *   }
    * @apiErrorExample  错误示例
    *   {
    *       "status":"1",
    *       "msg":"错误的消息提示~"
    *   }
    * */
```

![](https://img-blog.csdnimg.cn/20191023161804368.png)
![](https://img-blog.csdnimg.cn/20191023162044607.png)
![](https://img-blog.csdnimg.cn/20191023162121938.png)
![](https://img-blog.csdnimg.cn/20191023162203595.png)
