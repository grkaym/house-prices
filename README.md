# House Prices
## Overview
### Competition Description

住宅購入者に「理想の家」について語ってもらっても、おそらく地下室の天井の高さや東西を結ぶ鉄道への近さから話を始める人はいないだろう。しかし、この「遊び場」コンテストのデータセットは、価格交渉に影響を与える要素が、寝室の数や白いピケットフェンスなどよりもはるかに多いことを証明している。

アイオワ州エイムズにある住宅の（ほぼ）あらゆる側面を説明する79の説明変数を用いて、このコンテストでは、各住宅の最終価格を予測することが求められます。

## Evaluation
### Goal
各住宅の販売価格を予測するのがあなたの仕事です。テストセット内の各Idについて、SalePrice変数の値を予測する必要があります。

### Metric
提出されたデータは、予測値の対数と観測された販売価格の対数との間の二乗平均平方根誤差（RMSE）に基づいて評価されます。（対数変換を行うことで、高価な住宅と安価な住宅の予測誤差が、結果に等しく影響するようになります。）

### Submission File Format 
ファイルにはヘッダーを含め、以下の形式で記述する必要があります：
```csv
Id,SalePrice
1461,169000.1
1462,187724.1233
1463,175221
etc.
```

### Data
| カラム名            | 日本語での意味                      |
| --------------- | ---------------------------- |
| `SalePrice`     | 不動産の売却価格（ドル）。**予測対象となる目的変数** |
| `MSSubClass`    | 建物のクラス                       |
| `MSZoning`      | 一般的な用途地域・ゾーニング分類             |
| `LotFrontage`   | 物件が接している道路の長さ（フィート）          |
| `LotArea`       | 土地面積（平方フィート）                 |
| `Street`        | 道路へのアクセス方法・道路の種類             |
| `Alley`         | 路地へのアクセス方法                   |
| `LotShape`      | 土地の形状                        |
| `LandContour`   | 土地の平坦さ・地形                    |
| `Utilities`     | 利用可能な公共サービスの種類               |
| `LotConfig`     | 土地区画の配置・構成                   |
| `LandSlope`     | 土地の傾斜                        |
| `Neighborhood`  | Ames市内の地域・近隣エリア              |
| `Condition1`    | 主要道路や鉄道との位置関係                |
| `Condition2`    | 2つ目の主要道路や鉄道との位置関係            |
| `BldgType`      | 住居・建物の種類                     |
| `HouseStyle`    | 住宅のスタイル                      |
| `OverallQual`   | 建材や仕上がりを含む住宅全体の品質            |
| `OverallCond`   | 住宅全体の現在の状態                   |
| `YearBuilt`     | 建築年                          |
| `YearRemodAdd`  | 改築・リフォーム年                    |
| `RoofStyle`     | 屋根の形状                        |
| `RoofMatl`      | 屋根材                          |
| `Exterior1st`   | 主な外装材                        |
| `Exterior2nd`   | 2つ目の外装材                      |
| `MasVnrType`    | 石・レンガなどの化粧外装材の種類             |
| `MasVnrArea`    | 化粧外装材の面積（平方フィート）             |
| `ExterQual`     | 外装材の品質                       |
| `ExterCond`     | 外装材の現在の状態                    |
| `Foundation`    | 基礎の種類                        |
| `BsmtQual`      | 地下室の高さ・品質                    |
| `BsmtCond`      | 地下室全体の状態                     |
| `BsmtExposure`  | 地下室の外部への露出度（庭・外への開放性）        |
| `BsmtFinType1`  | 地下室の主要な仕上げ部分の品質・種類           |
| `BsmtFinSF1`    | 地下室の主要な仕上げ済み面積（平方フィート）       |
| `BsmtFinType2`  | 地下室の2つ目の仕上げ部分の品質・種類          |
| `BsmtFinSF2`    | 地下室の2つ目の仕上げ済み面積（平方フィート）      |
| `BsmtUnfSF`     | 地下室の未仕上げ面積（平方フィート）           |
| `TotalBsmtSF`   | 地下室の総面積（平方フィート）              |
| `Heating`       | 暖房方式                         |
| `HeatingQC`     | 暖房設備の品質・状態                   |
| `CentralAir`    | セントラル空調の有無                   |
| `Electrical`    | 電気設備の種類                      |
| `1stFlrSF`      | 1階の床面積（平方フィート）               |
| `2ndFlrSF`      | 2階の床面積（平方フィート）               |
| `LowQualFinSF`  | 低品質な仕上げ済み床面積                 |
| `GrLivArea`     | 地上階の居住面積（平方フィート）             |
| `BsmtFullBath`  | 地下室にあるフルバスルームの数              |
| `BsmtHalfBath`  | 地下室にあるハーフバスルームの数             |
| `FullBath`      | 地上階にあるフルバスルームの数              |
| `HalfBath`      | 地上階にあるハーフバスルームの数             |
| `Bedroom`       | 地下室より上にある寝室の数                |
| `Kitchen`       | キッチンの数                       |
| `KitchenQual`   | キッチンの品質                      |
| `TotRmsAbvGrd`  | 地上階の総部屋数（バスルームを除く）           |
| `Functional`    | 住宅の機能性評価                     |
| `Fireplaces`    | 暖炉の数                         |
| `FireplaceQu`   | 暖炉の品質                        |
| `GarageType`    | ガレージの位置・種類                   |
| `GarageYrBlt`   | ガレージの建築年                     |
| `GarageFinish`  | ガレージ内部の仕上げ状態                 |
| `GarageCars`    | ガレージの収容可能台数                  |
| `GarageArea`    | ガレージ面積（平方フィート）               |
| `GarageQual`    | ガレージの品質                      |
| `GarageCond`    | ガレージの状態                      |
| `PavedDrive`    | 車道が舗装されているか                  |
| `WoodDeckSF`    | ウッドデッキ面積（平方フィート）             |
| `OpenPorchSF`   | オープンポーチ面積（平方フィート）            |
| `EnclosedPorch` | 囲われたポーチの面積（平方フィート）           |
| `3SsnPorch`     | 3シーズン用ポーチの面積（平方フィート）         |
| `ScreenPorch`   | 網戸付きポーチの面積（平方フィート）           |
| `PoolArea`      | プール面積（平方フィート）                |
| `PoolQC`        | プールの品質                       |
| `Fence`         | フェンスの品質                      |
| `MiscFeature`   | その他の設備・特徴                    |
| `MiscVal`       | その他の設備・特徴の金銭的価値              |
| `MoSold`        | 売却された月                       |
| `YrSold`        | 売却された年                       |
| `SaleType`      | 売却方法・取引の種類                   |
| `SaleCondition` | 売却時の条件・状況                    |
