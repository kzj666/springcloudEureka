#Eureka注册中心

##实现一个注册中心
第一步，导入依赖
```xml
<!--eureka依赖-->
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-eureka-server</artifactId>
    <version>1.4.6.RELEASE</version>
</dependency>
```
第二步，配置yml配置文件
第三步，在核心启动类上加上@EnableEureka~Serve注解  

##配置provider，使其启动便自动放入注册中心
第一步，导入依赖
```xml
<!--eureka依赖-->
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-eureka</artifactId>
    <version>1.4.6.RELEASE</version>
</dependency>
```
第二步，配置yml配置文件
第三步，在核心启动类上加上@EnableEurekaClient注解 


##配置一些监控的信息（在provider服务中）
第一步，导入监控的依赖
```xml
<!--actutor完善监控信息(erekua的status指向网页的信息依赖)-->
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```
第二步，配置yml配置文件中info属性，添加自己的一些信息

##团队协作中，可以实现服务发现的机制
第一步，在核心启动类中加上@EnableDiscoveryClient注解

第二步，注入DiscoveryClient对象，调用getService()、getInstances等方法

