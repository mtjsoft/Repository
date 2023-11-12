# Repository
发布自己封装库的仓库

## 引用发布的库

project build.gradle 添加仓库地址

```
buildscript {
   repositories {
       //仓库地址
       maven {
            url 'https://raw.githubusercontent.com/mtjsoft/Repository/master'
       }
   }
}

allprojects {
   repositories {
       //仓库地址
       maven {
            url 'https://raw.githubusercontent.com/mtjsoft/Repository/master'
       }
   }
}
```

## 在module build.gradle 中 依赖已存在的库
如：
```
    implementation 'io.github.mtjsoft:jp2-android:1.0.0'
```

## 已发布的库

- [x]  jp2-android
