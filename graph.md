graph TD
    A[数据读取<br/>HDFS+PySpark] --> B[文本预处理<br/>分词、编码、padding]
    B --> C1[句子1编码器<br/>Embedding→LSTM→Pooling→Dense]
    B --> C2[句子2编码器<br/>Embedding→LSTM→Pooling→Dense]
    C1 --> D1[句子1向量]
    C2 --> D2[句子2向量]
    D1 --> E[相似度计算<br/>点积+归一化]
    D2 --> E
    E --> F[输出相似度分数]
    F --> G[交互式输入预测]
