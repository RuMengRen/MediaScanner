﻿# MediaScanner
Android platform to scan media files to the system database tools.  

QQ Group: 547839514  
Author URL: [http://www.yanzhenjie.com](http://www.yanzhenjie.com)  

----

# Dependencies
* Gradle
```groovy
compile 'com.yanzhenjie:mediascanner:1.0.0'
```

* Maven
```xml
<dependency>
  <groupId>com.yanzhenjie</groupId>
  <artifactId>mediascanner</artifactId>
  <version>1.0.0</version>
  <type>pom</type>
</dependency>
```

# Usage

## Create Scanner
```java
MediaScanner mediaScanner = new MediaScanner(this);
...
```

## Create Scanner, need callback
```java
// if need callback.
ScannerListener listener = new ScannerListener() {
    @Override
    public void oneComplete(String path, Uri uri) {
        // A file is scanned.
    }

    @Override
    public void allComplete(String[] filePaths) {
        // All file is scanned.
    }
}
MediaScanner mediaScanner = new MediaScanner(this, listener);
...
```

## Scan file path
```
if(!mediaScanner.isRunning()) {
    String filePath = ...
    mediaScanner.scan(filePath);
}
...
```

## Scan file path array
```java
if(!mediaScanner.isRunning()) {
    String[] fileArray = ...
    mediaScanner.scan(fileArray);
}
...
```

## Scan file path list
```
if(!mediaScanner.isRunning()) {
    String fileList = ...
    mediaScanner.scan(fileList);
}
...
```

**欢迎中国开发者关注作者微信公众号**  
扫码或者微信添加公众号-搜索**严振杰**  
![wechat](./image/wechat.jpg)

# License
```text
Copyright 2017 Yan Zhenjie

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```