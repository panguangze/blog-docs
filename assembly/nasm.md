* elf:https://www.cnblogs.com/qscfyuk/p/11697816.html
* elf文件格式是在有操作系统以后才可以执行的，bin文件是纯粹的二进制文件，在没有操作系统的时候也可以执行
* ![image-20200119172200654](/home/panguangze/Documents/githubs/blog-docs/assembly/asserts/image-20200119172200654.png)
* 这里pusha的作用是把当前的寄存器的值入栈，防止被调用子程序破坏了值
* （1）ESP：栈指针寄存器(extended stack pointer)，其内存放着一个指针，该指针永远指向系统栈最上面一个栈帧的栈顶。  由于栈的地址大小是从上到下从大到小，所以ESP指在栈的最底端。
  （2）EBP：基址指针寄存器(extended base pointer)，其内存放着一个指针，该指针永远指向系统栈最上面一个栈帧的底部。指在栈的最顶端。
* 在这里要注意由于在intel系统中栈是向下生长的(栈越扩大其值越小,堆恰好相反)
* eax一般用来保存函数的返回值，***\*记住esp是栈顶指针寄存器，ebp是栈底指针寄存器。\****
  **ESP 中的指针将一直指向这个新位置, 所以 ESP 中的地址数据是动态的**.
* 根据上述的定义,在通常情况下ESP是可变的,随着栈的生产而逐渐变小,而ESB寄存器是固定的,只有当函数的调用后,发生入栈操作而改变
* https://blog.csdn.net/anancolorful/article/details/80271543
* https://blog.csdn.net/qq_41884002/article/details/81452889

