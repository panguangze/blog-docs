* 只有整个结构体实例是可变的时候才允许其中的可变属性改变
* ![image-20200117131051800](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200117131051800.png)
* 结构体更新语法
* ![image-20200117133046036](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200117133046036.png)
* **结构体的内存分配问题**
* ![image-20200117134631154](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200117134631154.png)
* ![image-20200117135331900](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200117135331900.png)
* ![image-20200117135615388](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200117135615388.png)
* 枚举类型比起结构体更加的灵活
* Option枚举出现的地方采用可能出现空值，当使用了Option包装你的值的时候也就是意味着你需要处理如果该值为空的情况。在rust中所有的类型除了Option都不会为空
* rust中的match必须match所有的的情况。
* if let是match只关心一种情况的版本。
* ![image-20200117195419813](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200117195419813.png)
* rust默认所有的东西都是私有的，夫模块无法访问私有子模块，但是子模块可以访问父模块。同时pub关键字只对他所修饰的有效，对于其中的子组件无效。**但是对于枚举来说其中的成员会随着父pub而变为共有的**
* use的引用尽量要use到父模块
* ![image-20200117201501161](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200117201501161.png)
* 

