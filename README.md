### 本文将给大家带来Object的方法总结



1，Object.is()
	Object.is()它用来比较两个值是否严格相等，与严格比较运算符（ === ）的行为基本一致，是在三等号判断的基础上新增了两个不同之处。
	Object.is()不同之处只有两个：一是+0不等于-0，二是NaN等于自身
	Object.is()，===，==判断基本类型时，是判断值是否相等；判断引用类型时，是判断指针是否相等，也就是说是否指向同一块堆内存
    
2，Object.assign()
	Object.assign()方法用于对象的合并，将源对象（ source ）的所有可枚举属性，复制到目标对象（ target ）
   注意：
    这里是浅拷贝！！
    此方法只拷贝源对象的自身属性，不拷贝继承的属性！！
    如果目标对象与源对象有同名属性，或多个源对象有同名属性，则后面的属性会覆盖前面的属性！！
    Object.assign可以用来处理数组，但是会把数组视为对象
    Object.assign([1, 2, 3], [4, 5])	// [4, 5, 3]
    
3、Object.keys()、Object.values()、Object.entries()
    Object.keys()方法，返回一个数组，成员是参数对象自身的（不含继承的）所有可遍历（ enumerable ）属性的键名数组。

    Object.values()方法返回一个数组，成员是参数对象自身的（不含继承的）所有可遍历（ enumerable ）属性的键值数组。

    Object.entries()方法返回一个数组，成员是参数对象自身的（不含继承的）所有可遍历（ enumerable ）属性的键值对数组。

    let obj = {name:"winne",age:22};
    let objKeys = Object.keys(obj);
    let objValues = Object.values(obj);
    let objItem = Object.entries(obj);

    console.log(objKeys);   //["name","age"]
    console.log(objValues); //["winne",22]
    console.log(objItem);   //[["name","winne"],["age",22]]