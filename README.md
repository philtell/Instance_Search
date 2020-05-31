**Development Environment**
| Enviroment Name | Version |
|--|--|
| OS | Ubuntu 18.04TLS |
| python | 3.7.3 |
|DL Framework|tensorflow|
|DL Framework|keras|

**Use case**:

**Pretreatment**:

1. Download Picture From Oxford Database.At first, you should run the command like this **sh getData.sh**with the shell of Ubuntu.

then ,you can run the command like under this sentence, it will be extract the feature from every picture in database and build indices file featureCNN.h.

对database文件夹内图片进行特征提取，建立索引文件featureCNN.h5

```
python index.py -database database -index featureCNN.h5
```
last, you can run the command like under this sentence, it will find three pics  which simlarity are most close in the dataset
使用database文件夹内all_souls_000000.jpg作为测试图片，在database内以featureCNN.h5进行近似图片查找，并显示最近似的3张图片

```
python query_online.py -query database/all_souls_000000.jpg -index featureCNN.h5 -result database
```

