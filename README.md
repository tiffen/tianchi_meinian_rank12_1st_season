# 天池美年AI大赛，第一赛季排名12
github上分享的第一份代码，希望大家多给点星星，谢谢^ ^

由于系统路径在程序内部才把code的文件夹加入，因此主函数中调用的子程序都会有红色下划线，但可以运行。

我们组有两份代码，虽然都用lgbm模型，但特征工程都是独立实现，b榜最优成绩是各自5+3份结果的求平均的融合，线上分数0.02792，最后排名第12名。

这份代码提交过b榜单份结果，线上成绩是0.02816，线下分数在0.02758到0.02810之间波动，但后来发现特征选择的代码有点bug，做了些修改，复现时也发现以前做特征工程时莫名其妙地落下了0102这栏文字特征，加上这栏特征后好像线下分数下降了，跑了两份一份0.02809一份0.02824，因此后来先把0102删掉了。

特征工程等其他详细信息决赛之后再补充吧。

data里的zip文件要手动解压，虽然有a、b榜的vid名单，但官方没有公布答案，只能获得线下分数，若要比较结果，建议从训练集里再划分出训练集、验证集和测试集。
由于我还不太懂git bash的用法，有一个原始数据超过25m没法上传，先发百度云的链接，学会了git bash后再传进data文件夹里。
链接：https://pan.baidu.com/s/1pwp90ubent3_4_e9SgQSyA 密码：rb61

硬件及环境：
操作系统 Windows10 |Python 3.6.1 |Anaconda 4.4.0 (64-bit)|

使用的package

jieba  __version__ = '0.39'

gensim __version__ = '3.4.0'

numpy __version__ ='1.14.2'

pandas __version__ ='0.20.1'

sklearn __version__ = '0.18.1'

lightgbm __version__ = '2.1.0'

内存16G应该足够了，预处理大概要3小时和训练需要2小时左右（CPU：ryzen-1700 OC 3.40hz）
