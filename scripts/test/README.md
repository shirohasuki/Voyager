这个文件夹用于将workload文件夹下的测试用例分类调用，以便测试时选择ut,it,st以及跳过哪些测试。

如果你想在测试服务器添加一个测试用例，就需要按照workload->scripts/test的顺序修改这两个地方

推荐可以在这个文件夹下添加一个`local`文件夹，用于存放本地的测试用例，方便本地调试，测试服务器的用例作为本地的子集。


示例：

1. 运行cpu的所有ut和it测试，npu的it测试
```
test.py -cpu ut it -npu it
```

2. 运行mini-test集
```
test.py -mini-test
```