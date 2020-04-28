## 使用方式


```添加依赖
<dependency>
  <groupId>top.remember5</groupId>
  <artifactId>spring-boot-encrypt-starter</artifactId>
  <version>1.0</version>
</dependency>
```



注解可以添加到方法上或者类上
加密：
```java
@AESDecryptBody
@DESDecryptBody
@RSADecryptBody
```


解密：
```java
@AESEncryptBody
@DESEncryptBody
@MD5EncryptBody
@RSAEncryptBody
@SHAEncryptBody
```

指定方式，使用一下注解
```java
@DecryptBody
@EncryptBody
```


完整配置请参考：
```
encrypt:
   aes-config:
      key: xx
   des-config:
      key: xxx
   rsa-config:
      private-key: xx
      public-key: xxx
      open: true 
      show-log: true 
      max-encrypt-block: 117
      max-decrypt-block: 256
```


## FAQ
使用的是spring的HttpInputMessage实现，非spring项目暂时不能使用,注解使用aop实现

