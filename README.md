# Signate StudentCup 2022　 solution 



## 課題
英語圏の求人情報に含まれるテキストデータをもとに、その職務内容が①データサイエンティスト、②機械学習エンジニア、③ソフトウェアエンジニア、④コンサルタント のどの職種に該当するかを判別するアルゴリズムを構築する。
[link](https://signate.jp/competitions/724#abstract)

### 評価関数
F1score （マクロ平均）

## 自分の仕事
[Qitta](https://qiita.com/carbscountry/items/dc98de3a2e03af5c9006)の記事にやり方を載せました
- GPUの計算環境整備
    - EC2のg4dn.xlarge
    - nvidia-docker


## Models
- Deberta-v3-large
- Deberta-v3-base
- Deberta-large
- RoberTa-large

## Work
- Resolve encoding error
- htmlタグの除去
- 重複データの除去
- StratifiedKFold(jobflag) Fold=5
- CrossEntropyLoss
- AdamW
- Pooler Output
  - Mean Pooling
  - Attention Pooling
- epoch : 10
- stacking(LGBM,CTB,logistic)
- 最頻値でアンサンブル

## Result
### 最終提出
5 / 221  位（繰り上げで3位入賞）🥇

public LB : 0.762

private LB : 0.755
