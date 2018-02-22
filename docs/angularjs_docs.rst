AngualrJS 技术文档
=================

$resource
---------

它是创建资源对象的工厂，底层封装了$http service，提供与RESTful服务端数据资源进行交互。

*应用$resource*

并不是直接通过$resource服务本身同服务器通信，$resource是一个创建资源对象的工厂，用来创建同服务端交互的对象。

    var User = $resource('/api/users/:userId', {userId:'@id'});

返回的User对象包含了同后端服务进行交互的方法，我们可以把User对象理解成同RESTFul的后端服务进行交互的接口。
该对象包含两个get类型的方法已经三个非get类型的方法。

    User.get({id:'123'}, successFn, errorFn);

该方法向url发送一个get请求，并期望一个json类型的响应。这里会向/api/users/123发送一个请求，successFn处理请求成功响应，errorFn处理错误
