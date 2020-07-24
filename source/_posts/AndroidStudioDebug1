---
title: Android Studio Debug 之 运行期代码植入
date: 2020-07-24 00:00:00
categories: 
- Android
tags:
- Android Studio
---

![图片](https://raw.githubusercontent.com/QuincySx/QuincySx.github.io/writing/raw/CustomGoodsRenderers.gif)


填入以下代码可以查看各种类的数据
```Java
if (((Object) this) instanceof String
        || ((Object) this) instanceof Number
        || ((Object) this) instanceof Class) {
    return ((Object) this);
}
StringBuilder sb = new StringBuilder("{");
Class<?> cls = ((Object) this).getClass();
java.lang.reflect.Field[] fields = cls.getDeclaredFields();
if (fields != null) {
    int size = fields.length;
    for (java.lang.reflect.Field field : fields) {
        field.setAccessible(true);
        Object value = field.get((Object) this);
        sb.append(field.getName())
                .append("=")
                .append(String.valueOf(value));
        if (--size > 0) {
            sb.append(", ");
        }
    }
}
return sb.append("}").toString();
```
