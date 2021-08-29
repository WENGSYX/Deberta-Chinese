# Deberta-Chinese

​      本项目，基于微软开源的Deberta模型，在中文领域进行预训练。开源本模型，旨在为其他人提供更多预训练语言模型选择。

​        本预训练模型，基于WuDaoCorpora语料库预训练而成。WuDaoCorpora是北京智源人工智能研究院（智源研究院）构建的大规模、高质量数据集，用于支撑“悟道”大模型项目研究。

​      使用WWM与n-gramMLM 等预训练方法进行预训练。

| 预训练模型            | 学习率 | batchsize | 设备   | 语料库 | 时间 | 优化器 |
| --------------------- | ------ | --------- | ------ | ------ | ---- | ------ |
| Deberta-Chinese-Large | 1e-5   | 512       | 2*3090 | 200G   | 14天 | AdamW  |



​      

### 加载与使用

依托于huggingface-transformers

```
tokenizer = BertTokenizer.from_pretrained("WENGSYX/Deberta-Chinese-Large")
model = AutoModel.from_pretrained("WENGSYX/Deberta-Chinese-Large")
```


#### 注意，请使用BertTokenizer加载中文词表
