Maven Use Alternative Local Repository Demo
===========================================

怎么样给Maven设置一个不同的本地仓库，用来保存下载下来的jar包。

重点很简单，就是在maven的用户配置文件`~/.m2/settings.xml`中添加：

```
<localRepository>~/my-new-dir</localRepository>
```

但是在这个Demo中，为了方便验证并且不破坏已有文件，我们在当前项目中提供了一个`user-settings.xml`并且指定使用它来代替`~/.m2/settings.xml`。

相关的命令我写在了`run.sh`中。

run.sh
------

执行`run.sh`：

```
./run.sh
```

由于要下载不少依赖包，所以需要花几分钟时间。成功运行后，你会看到在当前项目的`dotM2`目录中多了很多文件，证明我们的确成功的更改了`localRepository`.
