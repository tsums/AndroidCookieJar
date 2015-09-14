###Android Cookie Jar

A CookieStore implementation for Android apps that keeps cookies in a SharedPreferences instance.

This is by no means the most efficient method for saving cookies, and really shouldn't be considered best practice, but it works, and doesn't require sqlite setup.

Based on [java.net.InMemoryCookieStore](https://github.com/szitnik/SoftwareAnalysis/blob/master/SoftwareSources/jdk1.8.0/src/java/net/InMemoryCookieStore.java) and uses [Base64Coder](http://www.source-code.biz/base64coder/java/)

####Installation

```gradle
dependencies {
    compile 'biz.source_code:base64coder:2010-09-21'
    compile 'com.tsums.androidcookiejar:androidcookiejar:1.0@aar'
}
```

####Usage

In your Application class:

```java
CookieHandler.setDefault(
    new CookieManager(
        PersistentCookieStore.getInstance(this),
            CookiePolicy.ACCEPT_ORIGINAL_SERVER));
```

AndroidCookieJar has been tested with Apache UrlConnection, Volley, and OkHttp.
