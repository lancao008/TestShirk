###测试了android shrink和混淆，结论如下

shrinkResources true  

 * 既可以删除从没被引用过的图片，也可以删除从没被引用过的layout和其引用的图片
 * 没有在manifest中注册的activity会在混淆之后删除并且删除它引用的布局文件和布局文件引用的图片
 * 一旦activity在manifest中注册即使没被使用过，也不会在混淆中删除它引用的东西

proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'

    有了这行代码就不需要在自己的项目中添加常规的android混淆代码

![](https://github.com/lipangit/TestShirk/blob/master/show.png)
