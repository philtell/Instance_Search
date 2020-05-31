**Development Environment**
| Enviroment Name | Version |
|--|--|
| OS | Ubuntu 18.04TLS |
| python | 3.7.3 |
|DL Framework|tensorflow|
|DL Framework|keras|

**Use case**:
对database文件夹内图片进行特征提取，建立索引文件featureCNN.h5

```
python index.py -database database -index featureCNN.h5
```

使用database文件夹内all_souls_000000.jpg作为测试图片，在database内以featureCNN.h5进行近似图片查找，并显示最近似的3张图片

```
python query_online.py -query database/all_souls_000000.jpg -index featureCNN.h5 -result database
```

