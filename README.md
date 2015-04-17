###得出两个结论

shrinkResources true  
    既可以删除从没被引用过的图片，也可以删除从没被引用过的layout和其引用的图片
    
proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
    有了这行代码就不需要在自己的项目中添加常规的android混淆代码
