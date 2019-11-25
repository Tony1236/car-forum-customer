# car-forum-customer
汽车论坛消费者用车体验内容的判别与标注 比赛的代码

比赛网址： <https://www.datafountain.cn/competitions/365/datasets>

## models

+ ZEN
+ XLNet
+ AlBERT
+ ERNIE
+ BERT+ROBERTA

## 运行

1. 需要下载相应的预训练模型，对数据集的处理参考process_data.ipnb和ernie_process.ipynb文件

2. 运行的参数保存在相应的sh文件里面，根据数据和模型的路径自己进行修改

3. 修改相应的generate_ccf_submission.py文件，然后运行，就可以得到提交文件

## results

+ A榜单成绩：61名

| 模型  | 精度  | 备注 |
|:------------- |:---------------:| -------------:|
|  albert+roberta+zen       | **0.89024699000**     | 投票 |
| zenv1+roberta+albertv2  | 0.88196301000       | 投票 | 
| roberta    | 0.87532502000           | 12层  |
| ZEN_v1   | 0.87853360000           | 11.10  |
| XLNet   | 0.86586291000          |   |
| ERNIE   | 0.84082258000          |   |
| albert_v2  | 0.86472315000          | large版本  |
| albert_v1  | 0.84656274000         | base版本  |


+ B榜单成绩：69名

| 模型  | 精度  | 备注 |
|:------------- |:---------------:| -------------:|
|  albert+roberta+zen       | **0.89336467**     | 投票 |




+ 还尝试过其他的传统模型，不过效果都没有上面的几个好，所以就没有列出来

## 改进的地方

1. 只进行了投票的处理，后期需要考虑对模型概率的融合
2. 由于计算资源的限制，没有尝试更大的预训练模型
3. 没有进行细致的调节参数（时间比较紧）