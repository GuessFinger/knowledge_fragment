- 查找文件 

  shift + shfit   或者 ctrl + shift + N

- 查找类

  ctrl + N

- 选择一行

  shift + end

- 跳转至文件的开头/结尾

  ctrl + home/end

- 快速打印

  sout + table

- 生成构造方法

   alt +insert

- 格式化代码

  ctrl + alt + L 

- 自动补全代码

  ctrl + shift + enter

- 跳转至最近一个打开过的页面

  ctrl + table   如果按住 可以进行来回的切换

- 浏览最近打开过的文件 

  ctrl + e 

- 删除某一行

  ctrl + y 

- 剪切某一行

  ctrl + x

- 复制某一行

  ctrl + d 

- 添加注释

  ctrl + /

- 跳转至方法的实现处  我认为这个很高效  这个需要重点进行记忆 不管是在java中还是在js中 都可用

  ctrl + b 

- 移除没有用的包

  ctrl + alt +o 

- 选中光标所在的单词  这个我认为也很常用

  ctrl + w  这个用处比较大 可以反复尝试一下

- 文件重命名

  shift + f6

- 打开不同页面之间的来回切换

  alt +  ←/→

- 查看当前文件的结构  

  你可以使用 ctrl +f12  或者 alt + 7   我认为alt + 7 的展示效果更好一点  ctrl + f12  只是简单展示

- 定位到某一行

  ctrl  + g 

- 快速的给某一行添加 if /for /tyr catch  等等代码块  这个简直不要太爽

  ctrl + alt + t  需要选中

- 代码向下移动

  alt + shift + ↑/↓

- 这个也简直不要太爽  快速找到页面中错误地方

  f2

- 查找当前文件在项目中的位置

  alt + f1 





----

刚才把昨天看到的debug 实践了一下

进行几点说明

1. step over：在单步执行时，在函数内遇到子函数时不会进入子函数内单步执行，而是将子函数整个执行完再停止，也就是把子函数整个作为一步。有一点,经过我们简单的调试,在不存在子函数的情况下是和step into效果一样的（简而言之，越过子函数，但子函数会执行）。

2. step into：单步执行，遇到子函数就进入并且继续单步执行（简而言之，进入子函数）；

3. step out：当单步执行到子函数内时，用step out就可以执行完子函数余下部分，并返回到上一层函数。

4. force shift f7  表示强制步入  这个暂时还没有用到

5. run ro curosr  表示步入到光标处 前提是中间没有断点

6. 还有就是可以设置断点条件  ，这个条件只能设置 显示变量的条件 执行到断点处 然后直接执行完毕 

   就会跳到断点条件处

7. 可以选中某个值 然后添加到watch中 观察你要监测对象值的变换