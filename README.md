# Android Cookie Jar


A CookieStore implementation for Android apps that keeps cookies in a SharedPreferences instance.

This is by no means the most efficient method for saving cookies, and really shouldn't be considered best practice, but it works, and doesn't require sqlite setup.

Based on [java.net.InMemoryCookieStore](https://github.com/szitnik/SoftwareAnalysis/blob/master/SoftwareSources/jdk1.8.0/src/java/net/InMemoryCookieStore.java) 

## Installation

```gradle
dependencies {
    compile 'com.tsums.androidcookiejar:androidcookiejar:1.1@aar'
}
```

## Usage

In your Application class:

```java
CookieHandler.setDefault(
    new CookieManager(
        PersistentCookieStore.getInstance(this),
            CookiePolicy.ACCEPT_ORIGINAL_SERVER));
```
Using a different CookiePolicy is inadvisable. The author of this library is not responsible for misconfigured Cookie Jars.

AndroidCookieJar has been tested with Apache UrlConnection, Volley, and OkHttp.

## License
```
The MIT License (MIT)

Copyright (c) 2015 Trevor Summerfield

Permission is hereby granted, free of charge, to any person obtaining a 
copy of this software and associated documentation files (the "Software"), 
to deal in the Software without restriction, including without limitation 
the rights to use, copy, modify, merge, publish, distribute, sublicense, 
and/or sell copies of the Software, and to permit persons to whom the 
Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in 
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS 
OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, 
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE 
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER 
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING 
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER 
DEALINGS IN THE SOFTWARE.
```
