### shell学习的笔记

1.通过使用$[@]输出列表中的值
====
```
[root@localhost ~]# cat a.sh 
#!/bin/bash
set -x

buy_list=(1 101)
for i in ${buy_list[@]};do
  echo $i
done
------------
输出结果：
[root@localhost ~]# sh a.sh 
1
101

总结：$[@]可以将列表中的元素一一列出，也可以返回脚本参数的内容
拓展：$[#]可以返回脚本参数的个数
```
