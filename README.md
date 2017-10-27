# lec9
第二次个人报告
</br>
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
