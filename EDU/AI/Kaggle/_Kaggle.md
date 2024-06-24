Tags: #
____
# How to download dataset from kaggle in colab
> https://www.kaggle.com/discussions/general/74235

1. Upload api key
```
from google.colab import files
files.upload()
```
2. Download, unzip and use
```
!mkdir ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
!kaggle competitions download -c dogs-vs-cats
!unzip dogs-vs-cats.zip
!rm test1.zip
!mkdir -p ./dogcat
!unzip train.zip -d ./dogcat
```

____
### Zero-Links

____
### Links