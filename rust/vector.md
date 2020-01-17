* ![image-20200117202207732](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200117202207732.png)
* ![image-20200117202347689](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200117202347689.png)
* 为什么第一个元素的引用会关心 vector 结尾的变化？不能这么做的原因是由于 vector 的工作方式：在 vector 的结尾增加新元素时，在没有足够空间将所有所有元素依次相邻存放的情况下，可能会要求分配新内存并将老的元素拷贝到新的空间中。这时，第一个元素的引用就指向了被释放的内存。借用规则阻止程序陷入这种状况。
* rust不支持String类型的索引，**但是rust支持range索引**
* ![image-20200117213035393](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200117213035393.png)
* 
* 

