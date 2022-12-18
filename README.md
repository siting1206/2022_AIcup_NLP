# 2022 AIcup 作物影像判釋

## 環境

```
torch         1.13.0
torchvision   0.14.0
timm          0.6.11
scikit-learn  1.1.3
matplotlib    3.6.2
```

## 預訓練模型

由timm提供之SwinV2
```
swinv2_base_window12to24_192to384_22kft1k
```

## 下載、切分資料集

下載並解壓縮此次競賽之資料集

<split.py> :
   以訓練9:驗證1的比例切分資料集

    *需更改路徑再執行*
    
   執行後會得到一組Mead及Std和一組切分好的資料集(參考下圖範例)
   
```
├─datasp91
│  ├─val
│  │  ├─asparagus
│  │  ├─bambooshoots
│  │  ├─betal
│  │  ├─......
│  │  ├─tea
│  │  └─waterbamboo
│  └─train
│     ├─asparagus
│     ├─bambooshoots
│     ├─betal
│     ├─......
│     ├─tea
│     └─waterbamboo
```

## 模型訓練

<swin_train.py> :
  開始訓練 SwinV2 模型
  
  *需更改路徑再執行*

## 模型預測

<swin_test.py> :

  預測並將結果輸出csv檔
  
  *需更改路徑再執行*

