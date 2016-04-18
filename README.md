# Apache Shiro integration with Spring Boot

## Usage
### pom.xml
```
<dependency>
    <groupId>com.millinch</groupId>
    <artifactId>spring-boot-shiro-starter</artifactId>
    <version>1.0.0</version>
</dependency>
```
### application.yml

```
shiro:
  realm: com.yourcompany.YourRealm
  login-url: /login
  success-url: /welcome
  sign-in:
    user-param: username
    password-param: password
    remember-me-param: rememberMe
  filter-chain-definitions:
    /login.html: authc
    /logout.html: logout
    /favicon.ico: anon
    /index.html: anon
    /assets/**: anon
    /**: authc
```