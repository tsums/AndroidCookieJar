###PersistentCookieStore

A CookieStore implementation for Android apps that keeps cookies in a SharedPreferences instance.

Based on [java.net.InMemoryCookieStore](https://github.com/szitnik/SoftwareAnalysis/blob/master/SoftwareSources/jdk1.8.0/src/java/net/InMemoryCookieStore.java) and uses [Base64Coder](http://www.source-code.biz/base64coder/java/)

To use, put the following line into your Application java file:

```java
CookieHandler.setDefault(new CookieManager(PersistentCookieStore.getInstance(this), CookiePolicy.ACCEPT_ORIGINAL_SERVER));
```
