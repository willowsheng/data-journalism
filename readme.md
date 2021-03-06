# 数据新闻-实验II: 从事件链到文本

+ 选择10篇文献：实验I的新闻数据
+ 每篇选择最长的2条事件链
+ 生成复杂触发词（触发词、概括词和轻动词的组合）
+ 确定事件要素（基于依存关系）
+ 确定句法结构（自行设计句式）
+ 根据时间顺序排列（自行设计排列顺序）

---

> **一些设计：**
> 
> *排列顺序设计：* 按行文顺序排列
> 
> *句法结构：*
> 
> `Subject [Target NP Once] Trigger [Target NP Once] Object [Time]`
> 
> 主干是“主谓宾”结构。若这句话中包含的目标 NP 不在主语或宾语中出现过（即为修饰语或补语等），则按照句子的自然顺序在主谓或动宾之间加入。最后，如果有相关的时间词组，则在句子最后加上。
> 
> *使用的module：* `LTP 4.1.4`

---

使用方法：

```Shell
    python3 -u DataJournalism-Task2.py
```

新闻数据都在.py文件里，修改后运行即可。其中，`target`变量标记的是将要分析的变量。
