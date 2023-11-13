# Repository
发布自己封装库的仓库

## 引用发布的库

project build.gradle 添加仓库地址

```
buildscript {
   repositories {
       //GitHub仓库地址。如果网络原因无法拉取到依赖库，可选择使用gitee仓库地址。二选一即可
       maven {
            url 'https://raw.githubusercontent.com/mtjsoft/Repository/master/maven_repo'
       }
       // 国内网络原因，可以选择使用gitee仓库地址
       maven {
            url 'https://gitee.com/mtj_java/maven-repository/raw/master/maven_repo'
       }
   }
}

allprojects {
   repositories {
       //GitHub仓库地址。如果网络原因无法拉取到依赖库，可选择使用gitee仓库地址。二选一即可
       maven {
            url 'https://raw.githubusercontent.com/mtjsoft/Repository/master/maven_repo'
       }
       // 国内网络原因，可以选择使用gitee仓库地址
       maven {
            url 'https://gitee.com/mtj_java/maven-repository/raw/master/maven_repo'
       }
   }
}
```

## 在module build.gradle 中 依赖已存在的库
如：
```
    implementation 'cn.mtjsoft.maven:jp2-android:1.0.0'
```

## 已发布的库
使用文档详见仓库 doc 目录

- [x]  BarcodeScanning
- [x]  jp2-android
- [x]  ocr-android