# lec9 第二次个人报告
</br>
<h1>第九课视频内容（没看完）</h1>
    <p>将词语用向量表示，意思相近的词语它们对应的词向量在词向量空间里的距离也是相近的。</p>
<img src="/image/1.png" width="450" height="250">
    <p>相近意思的句子由语法树生成的向量在词向量空间里的距离也是相近的。</p>
<img src="/image/2.png" width="450" height="250">
    <p>将句子划分成细小的结构，如介词、名词、介词短语和动词短语等等（用到SVG算法，还不知道SVG作用原来，在看论文）。</p>
<img src="/image/4.png" width="450" height="250">
    <p>词向量p由词向量c1和c2通过公式：p=tanh((W1*c1+W2*c2)+b)算出，并经过RNN得出结果p向量的可信度。</p>
<img src="/image/5.png" width="450" height="250">
    <p>先将相邻的两个词向量都算一下，比较每一个p的分数，将分数大的如[[5],[2]]作为左孩子c1和作为有孩子c2的单词set的词向量[[7],[1]]算出下一个p并得出分数再进行比较。（向量[[0],[1]]这个节点就删除了）</p>
<img src="/image/6.png" width="450" height="250">
    <p>最后生成如下语法树。</p>
<img src="/image/3.png" width="450" height="250">
<h2>SVM</h2>
    <P>Vapnik等人在多年研究统计学习理论基础上对线性分类器提出了另一种设计最佳准则。其原理也从线性可分说起，然后扩展到线性不可分的情况。甚至扩展到使用非线性函数中去，这种分类器被称为支持向量机（Support Vector Machine，简称SVM）。SVM就是将线性不可分问题映射到高维空间，让其变得线性可分。适合于解决文本分析问题，其核函数中对于文本分析有较好表现的是径向积函数，之前学习过，这几天又加深学习了一遍。贴出两个网址，如下：</P>
    <p>手把手教你实现SVM算法</p>
http://blog.csdn.net/alvine008/article/details/9097105
    <p>核函数</p>
http://wenku.baidu.com/view/8c17ebda5022aaea998f0fa8.html
