---
title: Android Spinner
date: 2017-07-11 15:44:53
tags: Android
---
文章改动记录：
1. 2017-07-11 文字初始化

**注意**
> 默认Android版本从16开始
> 默认优先使用Google的MD设计

这是一篇关于Android Spinner的使用介绍。
## 起因
    有时候Android自带的Spinner不能满足我们的需要，或者设计师大大需要改为其他自定义的样式的时候，我们就需要能够自定义她的样式了。
## Spinner的XML属性
常用的属性有：
1. **entries**: 可以使用该属性在XML里面绑定数据源，也可以不设置，然后在Activity里面动态设置。如：
```
    android:entries="@array/spinnerData"
```
其中spinnerData是一个在String资源文件里面定义的String数组，具体如下：
```
    <string-array name="spinnerData">
        <item>请选择…</item>
        <item>第一行</item>
        <item>第二行</item>
        <item>第三行</item>
    </string-array>
```
2. **spinnerMode**: 用来控制Spinner的显示形式
3. **prompt**: 该属性需要配合**spinnerMode**属性一起使用，如果Spinner的菜单形式是弹出框的时候，该属性可以控制弹框的标题; 同时，该属性的文字需要在string文件里面设置，不能在XML文件里面直接写字符串。如：
![](/images/android_spinner.png)

## Spinner的显示方式
Spinner有两种显示方式，一种是下拉菜单形式，一种是弹出框的形式，在XML文件里面是由**spinnerMode**属性来控制的。
```
android:spinnerMode="dialog"
android:spinnerMode="dropdown"
```
