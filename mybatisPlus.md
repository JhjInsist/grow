# Typora

## 分页查询

分页使用十分之多

1. 原始使用limit
2. pageHelper
3. mp内置分页插件

> 如何使用？

1. 直接配置拦截器即可
2. 使用page

```java
public void testPage(){
	//参数一：当前页 
	//参数二：页面大小
	Page<User>page = new Page<>(2,5);
	user.selectPage(Page,null);
	
	
	
}
```

![image-20220324223139479](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20220324223139479.png)

## 删除操作

1. 根据id删除记录

   ```java
   //删除通过id
   public void testDelectById(){
   	userMapper.deleteById("id");
   }
   
   //删除通过id批量
   public void testDelectById(){
   	userMapper.deleteById(Array.asList(1111111l,222222222l));
   }
   
   //删除通过map
   
   @test
   Public void testDeleteMap(){
   	HashMap<String,Object>map = new HashMap<>();
   }
   ```

### 逻辑删除

管理员可以查看被查看删除的数据！ 以防止数据丢失

## 性能分析插件

开发时会遇到一些慢sql

mp提供性能分析插件

作用：分析每条sql执行时间

超过时间停止运行



## 条件构造器

十分重要：Wrapper

很多官方文档

