* ownership的出现是为了解决一些内存的问题，在编译期间解决内存的分配，从而不用再运行期间进行gc
* string常量是不可变的
* string常量和String是不一样的，String是可变的，是被分配在heap中的
* ![image-20200116192950100](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200116192950100.png)
* 对于所有大小已知的数据都会被分配在栈上面
* ![image-20200116194140249](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200116194140249.png)
* ![image-20200116194236582](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200116194236582.png)
* 这段代码只是复制了一份指针而已，但是这里要注意，并不是简单的复制了一份指针而已，这里是做了move操作！此时的s1已经不能再被使用了，是无效的。可以避免两次释放同一块内存的错误
* ![image-20200116194714375](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200116194714375.png)
* ![image-20200116194904760](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200116194904760.png)
* 这种操作并不会让x失效，因为这里x实在栈中。
* If a type has the `Copy` trait, an older variable is still usable after assignment. Rust won’t let us annotate a type with the `Copy` trait if the type, or any of its parts, has implemented the `Drop` trait
* ![image-20200116195421438](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200116195421438.png)
* ![image-20200116200122378](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200116200122378.png)
* ![image-20200116200606302](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200116200606302.png)
* ![image-20200116200807779](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200116200807779.png)
* 但是这种机制可以被突破，不过目前好像rust社区还在讨论这玩意。不让这样做的原因是为了防止数据竞争
* ![image-20200116201201967](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200116201201967.png)
* ![image-20200116201328683](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200116201328683.png)
* 当被以immutable借用时不可以再被mutable借用，反过来同样。
* Note that a reference’s scope starts from where it is introduced and continues through the last time that reference is used
* ![image-20200116201912514](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200116201912514.png)
* ![image-20200116203104636](/home/panguangze/Documents/githubs/blog-docs/rust/asserts/image-20200116203104636.png)
* 

