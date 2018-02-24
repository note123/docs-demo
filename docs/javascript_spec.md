# 描述定义Javascript代码编写中需要注意的问题点

### use strict 模式下 编程注意点

##### 1. cannot declare a parameter named 'err' as it shadows the name of a strict mode function*
> 当使用strict模式时， 函数的方法名称和参数名称必须不同，否则会出现以上错误