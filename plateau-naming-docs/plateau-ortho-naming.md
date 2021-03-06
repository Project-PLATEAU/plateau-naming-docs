## plateau-ortho-naming

### 1. 本ドキュメントの説明
本ドキュメントは、国土交通省都市局がProject PLATEAUとして公開するオープンデータ（**ortho形式**）のダウンロードファイルフォルダ構成規則及び命名規則を公開することにより、利用者の検索、ダウンロード、データを利用した開発等の利便性を向上させることを目的とする。

### 2. ファイル名の表記の方法等
ファイル名の表記の方法その他の項目については[「Project PLATEAUオープンデータ-ファイル命名規則及びフォルダ構成規則」](../README.md)に従う。


### 3. ortho形式のフォルダ構成規則
obj形式のデータセットのフォルダ構成規則は以下のとおりとする。  

```
[市町村コード5桁]_[市区町村名英名]_[整備年度]_ortho_[更新回数]_op  
│   
├ images  
│   └──_.tif  
│
└ metadata   
    └─_.pdf
```
 (例: 23100_nagoya-shi_ortho_2020_2_op) 

### 4. ortho形式のファイル命名規則
ortho形式(GeoTIFF形式）のデータのファイル命名規則は以下のとおりとする。

```
[メッシュコード]_[オプション].tif  
```
(例: /////）

メタデータのファイル命名規則は以下のとおりとする。  
なお、[整備年度]は当該データが撮影された年度を西暦で表す。
```
ortho_[市町村コード]_[整備年度]_metadata_[オプション].pdf  
```
(例: /////）

### 各構成要素の意味は以下のとおりとする。
| 構成要素 | 説明 |
|:-|:-|
| [メッシュコード] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| ファイル単位となる地域メッシュのメッシュコードを付与する。<br>メッシュコードは「JISX0410地域メッシュコード」に定められた第2次地域区画（統合地域メッシュ、一辺の長さ約10km）又は基準地域メッシュ（第3次地域区画、一辺の長さ約1km）単位を用いることを基本とする。<br>ファイルを分割する場合は[「3D都市モデル標準作業手順書（第2.0版）」](https://www.mlit.go.jp/plateau/libraries/)  5.4.1に則って行う。 |
| [地物型] | [地物型]にはファイルに含まれる地物型を識別する接頭辞を付与する。<br>接頭辞は[「3D都市モデル標準作業手順書（第2.0版）」](https://www.mlit.go.jp/plateau/libraries/)  5.4.3の表5-8のものを用いる。 |
| [CRS] | オブジェクトに適用される空間参照系の略称を使用する。<br>略称は[「3D都市モデル標準作業手順書（第2.0版）」](https://www.mlit.go.jp/plateau/libraries/)  5.4.3の表5-9のものを用いる。 |
| [オプション] | 必要に応じてファイルを細分したい場合の識別子。 |
