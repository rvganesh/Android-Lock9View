# Android-Lock9View [ ![Download](https://api.bintray.com/packages/takwolf/maven/Android-Lock9View/images/download.svg) ](https://bintray.com/takwolf/maven/Android-Lock9View/_latestVersion) [![API](https://img.shields.io/badge/API-5%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=5) #

An Android grid lock screen view with a callback interface. It is very simple to use.

## ScreenShot ##

![Screenshot](screenshot/screenshot.png)

## Demo ##

[![Lock9View Demo on Google Play Store](http://developer.android.com/images/brand/en_generic_rgb_wo_60.png)](https://play.google.com/store/apps/details?id=com.takwolf.android.lock9)

## Usage ##

### Gradle ###

```gradle
compile 'com.takwolf.android:lock9view:0.0.2'
```

### Layout ###

```xml
<com.takwolf.android.lock9.Lock9View
    android:id="@+id/lock_9_view"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_gravity="center"
    app:nodeSrc="@mipmap/lock_9_view_node_normal"
    app:nodeOnSrc="@mipmap/lock_9_view_node_highlighted"
    app:lineColor="#ff006699"
    app:lineWidth="8dp" />
```

### Activity ###

```java
Lock9View lock9View = (Lock9View) findViewById(R.id.lock_9_view);
lock9View.setCallBack(new CallBack() {
    @Override
    public void onFinish(String password) {
        Toast.makeText(MainActivity.this, password, Toast.LENGTH_SHORT).show();
    }
});
```

## Author ##

TakWolf

[takwolf@foxmail.com](mailto:takwolf@foxmail.com)

[http://takwolf.com](http://takwolf.com)

## License ##

    Copyright 2015-2016 TakWolf
    
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.