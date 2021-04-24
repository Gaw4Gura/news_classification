## News Classification Task for [China Software Cup](http://www.cnsoftbei.com/plus/view.php?aid=599)

- use `tensorflow.keras` to setup a Text CNN model
- use `pandas.read_excel()` and engine `openpyxl` to read the *.xlsx* file offered by the contest
- use `jieba` to realize the Chinese word tokenization
- use `gensim.Word2Vec` and the pre-training model for Chinese from [this blog](https://blog.csdn.net/zkq_1986/article/details/84990426)
- use **Cosine Decay with Warm Restarts** method to control the learning rate mentioned by [this paper](https://arxiv.org/abs/1608.03983)
- use a improved cross entropy function $loss = -(1-\epsilon)\log{\left(e^{z_{max}}/Z\right)}-\epsilon\sum_{1}^{n}\frac{1}{n}\log{\left(e^{z_{max}}/Z\right)}$，其中$Z=\sum_{i=1}^{n}z_{i}$，$z_{max}=\max_{1\le i\le n}{z_i}$