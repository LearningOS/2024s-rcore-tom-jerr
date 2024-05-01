1. `a0`中实际上是当前任务的上下文
5. `csrrw sp, sscratch, sp`，将内核栈切换到用户栈，从而使程序进入用户态执行
6. `sp`中存放内核栈，`sscratch`中存放用户栈
7. `__alltraps`中的第一条指令`csrrw sp, sscratch, sp`