有监督学习的弊端：回答机械化，只能回答标准答案。

解决的方式是另一种学习方式，LHF，人类反馈学习。或者强化人类反馈学习。

---

涌现能力：简单个体的叠加，会出现非常复杂的结果。比如水分子的排列组合形成雪花。对应到大模型中就是随着模型参数的增加，会涌现一大批的能力。

对应有几个学习方式，不改变参数规模与值的情况下的输出，能够完成任务。

1. 上下文学习，在上下文中给予案例，模型自己学习。
2. instruction following，指令内容非常详细且细致。
3. chain of thought，

对应知识图谱的数据集构建过程就是上下文学习？

1. 信息污染。垃圾进垃圾出。
2. 安全可控和伦理。

---

**openai提出的scaling law 是什么？规模法则。**

**模型风洞是什么？有点像自动调参？**

团队认为是知识密度等同于制程，类似于摩尔定律。 

---

- kaggle在无网络中提交的方法，参考链接：https://blog.csdn.net/weiyuxin107/article/details/125173767

  1. 下载包到对应文件中。

  `!pip download <package-name> -d ./package` 

  下载完成后会看到`output`文件夹中出现了`package`里面为安装包

  ![image.png](.\pictures\image.png)

  1. 从对应包中下载到本地再上传

     ```python
     import shutil
     # base_name：压缩包名，base_dir：压缩包路径
     shutil.make_archive(base_name='./package',format="zip",base_dir='./package')
     
     # 查看文件链接
     from IPython.display import FileLink
     FileLink(r'package.zip')
     ```

  2. 使用上传数据集的方法上传对应的包

     解压后，按照上传数据集的方法上传对应的包

     `!pip install <package-name> --no-index --find-links=file:/kaggle/input/<dataset-name>/` 

---

RNN的输入，首先是转换成词表，接着高维映射到低维中，这时的矩阵是可以计算的。

我疑惑的还是对应的矩阵的运算，互信息的矩阵运算。

大模型学习的是token，信息都可以转换为token。

分为预训练与后训练。