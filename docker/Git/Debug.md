https://blog.csdn.net/weixin_42288182/article/details/96568718



主要原因是git仓库上已经存在readme文件，故在提交时可能会存在冲突，这时您需要选择的是保留线上的文件或者舍弃线上的文件：

#### 解决办法：

1、如果您舍弃线上的 文 件，则在推送时选择强制推送，强制推送需要执行下面的命令：
 `git push origin master -f`

2、如果您选择保留线上的readme文件,则需要先执行

```
git pull origin master
```

