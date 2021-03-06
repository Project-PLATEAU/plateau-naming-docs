## plateau-fbx-naming

### 1. 本ドキュメントの説明
本ドキュメントは、国土交通省都市局がProject PLATEAUとして公開するオープンデータ（**FBX形式**）のダウンロードファイルフォルダ構成規則及び命名規則を公開することにより、利用者の検索、ダウンロード、データを利用した開発等の利便性を向上させることを目的とする。

### 2. ファイル名の表記の方法等
ファイル名の表記の方法その他の項目については[「Project PLATEAUオープンデータ-ファイル命名規則及びフォルダ構成規則」](../README.md)に従う。


### 3. FBX形式のフォルダ構成規則
FBX形式のデータセットのフォルダ構成規則は以下のとおりとする。  
なお、メッシュコードを地図上で表示する図郭マップはルートフォルダ直下にpdf形式で格納すること。  

```
[市町村コード5桁]_[市区町村名英名]_[整備年度]_fbx_[更新回数]_op  
│   
├ bldg  
│ ├ lod1  
│ │  └──[メッシュコード]_bldg_[CRS]_fbx   
│ │       └── _.fbx  
│ └ lod2  
│    └──[メッシュコード]_bldg_[CRS]_fbx     
│         └── _.fbx   
├ dem   
│   └─_.fbx
│  
├ tran  
│   └─_.fbx  
│
├ brid  
│   └─_.fbx   
│
└ metadata   
   └─_.xml
```
 (例: 01100_sapporo-shi_2021_fbx_2_op) 

### 4. FBX形式のファイル命名規則
FBX形式のデータのファイル命名規則は以下のとおりとする。

```
[メッシュコード]_[地物型]_[CRS]_[オプション].fbx  
```
(例: 53394507_bldg_6677.fbx）

メタデータのファイル命名規則は以下のとおりとする。
```
fbx_[市町村コード]_[整備年度]_metadata_[オプション].xml  
```

### 各構成要素の意味は以下のとおりとする。
| 構成要素 | 説明 |
|:-|:-|
| [メッシュコード] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| ファイル単位となる地域メッシュのメッシュコードを付与する。<br>メッシュコードは「JISX0410地域メッシュコード」に定められた第2次地域区画（統合地域メッシュ、一辺の長さ約10km）又は基準地域メッシュ（第3次地域区画、一辺の長さ約1km）単位を用いることを基本とする。<br>ファイルを分割する場合は[「3D都市モデル標準作業手順書（第2.0版）」](https://www.mlit.go.jp/plateau/libraries/)  5.4.1に則って行う。 |
| [地物型] | [地物型]にはファイルに含まれる地物型を識別する接頭辞を付与する。<br>接頭辞は[「3D都市モデル標準作業手順書（第2.0版）」](https://www.mlit.go.jp/plateau/libraries/)  5.4.3の表5-8のものを用いる。 |
| [CRS] | オブジェクトに適用される空間参照系の略称を使用する。<br>略称は[「3D都市モデル標準作業手順書（第2.0版）」](https://www.mlit.go.jp/plateau/libraries/)  5.4.3の表5-9のものを用いる。 |
| [オプション] | 必要に応じてファイルを細分したい場合の識別子。 |


