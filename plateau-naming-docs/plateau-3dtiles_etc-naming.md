## plateau-3dTiles_etc-naming

### 1. 本ドキュメントの説明
本ドキュメントは、国土交通省都市局がProject PLATEAUとして公開するオープンデータ（**3DTiles形式、Shape形式、GeoJSON形式、MVT形式**）のダウンロードファイルフォルダ構成規則及び命名規則を公開することにより、利用者の検索、ダウンロード、データを利用した開発等の利便性を向上させることを目的とする。
<br>


### 2. ファイル名の表記の方法等
ファイル名の表記の方法その他の項目については[「Project PLATEAUオープンデータ-ファイル命名規則及びフォルダ構成規則」](../README.md)に従う。
<br>

### 3. ファイル概要
本ドキュメントの対象とするファイルの概要とファイル形式は以下のとおりである。



| フォルダ名 | 説明 |
|:-|:-|
| 01_building &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| このフォルダにはCityGMLのbldgを3DTiles形式に変換したデータが格納されており、テクスチャの有無と解像度の違いにより最大3種類となる。<br>接尾辞が_bldg_notextureの3DTilesはテクスチャのつかない建物モデルで、全ての都市に存在する。LOD2以上の建物モデルが存在する都市については、これに加えて接尾辞が_bldg_low_resolutionあるいは_bldg_textureの3DTilesが存在し、それぞれ低解像度のテクスチャがついた建物モデル、高解像度のテクスチャがついた建物モデルが格納されている。<br>これに加えて、これらの建物モデルのうち、ランドマークとなる建物名を表示するために使用するランドマークデータが格納されており、このファイルはShapeファイル形式である。 |
| 02_bridge &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| このフォルダにはCityGMLのbrid:Bridgeを3DTiles形式に変換したデータが格納される。このファイルは一部の都市（東京都23区および八王子市）のみに存在する。|
| 03_road &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|このフォルダにはCityGMLのtran:RoadをMVT形式に変換したデータが格納される。|
| 04_railway &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|このフォルダにはCityGMLのtran:RailwayをGeoJSON形式に変換したデータが格納される。|
| 05_park &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|このフォルダには公園の位置を表すポイントデータとポリゴンデータの2種類のデータが格納される。ポイントデータの形式はGeoJSON形式で、ポリゴンデータの形式はMVT形式である。なお、公園のポリゴンデータが存在するのは、一部の都市（東京都23区および八王子市）のみである。|
| 06_urbanplan &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|このフォルダにはCityGMLのurfに含まれる都市計画区域（urf:UrbanPlan）、区域区分（urf:AreaClassification）、地域地区（urf:DistrictsAndZones）のデータをMVT形式に変換したファイルが格納される。なお、VIEW用のデータは、都市計画区域と区域区分をまとめてひとつのデータセット（接尾辞：_toshikeikaku）とし、地域地区については用途地域（同 _youtochiiki）とその他の地域地区（同 _chiikichiku）の二つのデータセットに分割して作成した。|
| 07_landuse &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|このフォルダにはCityGMLのluse（土地利用現況）をMVT形式に変換したデータが格納される。|
| 08_emergency_road &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|このフォルダにはGeoJSON形式で作成された緊急輸送道路のデータが格納される。|
| 09_fld_ntl &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|このフォルダにはCityGMLのfldに含まれる、国管理河川における洪水浸水想定区域データを3DTiles形式に変換したデータを格納する。ファイルは河川と規模（計画規模・想定最大規模）毎に水面表現ありと無しの2種類ずつ作成されていて、接尾辞はそれぞれ_fld_texture_mlitと_fld_mlitとなる。|
| 10_fld_pref &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|このフォルダにはCityGMLのfldに含まれる、県管理河川における洪水浸水想定区域データを3DTiles形式に変換したデータを格納する。ファイルは河川と規模（計画規模・想定最大規模）毎に水面表現ありと無しの2種類ずつ作成されていて、接尾辞はそれぞれ_fld_texture_prefと_fld_prefとなる。|
| 11_dosha &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|このフォルダにはCityGMLのlsldに含まれる、土砂災害警戒区域データをMVTT形式に変換したデータを格納する。ファイルは土石流、地すべり、急傾斜の災害タイプごとに作成されている。|
| 12_tsunami &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|このフォルダにはCityGMLのtnmに含まれる、津波浸水想定データを3DTiles形式に変換したデータを格納する。水面表現有りと無しの2種類ずつ作成されていて、接尾辞はそれぞれ_tsunami_textureと_tsunamiとなる。|
| 13_takashio &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|このフォルダにはCityGMLのhtdに含まれる、高潮浸水想定区域データを3DTiles形式に変換したデータを格納する。水面表現有りと無しの2種類ずつ作成されていて、接尾辞はそれぞれ_takashio_textureと_takashioとなる。|
| 14_naisuihanran &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|このフォルダにはCityGMLのifldに含まれる、内水浸水想定区域データを3DTiles形式に変換したデータを格納する。水面表現有りと無しの2種類ずつ作成されていて、接尾辞はそれぞれ_naisuihanran_textureと_naisuihanranとなる。|
<br>

### 4. 3DTiles形式のフォルダ構成規則
3DTiles形式、Shape形式、GeoJSON形式、MVT形式のデータセットのフォルダ構成規則は以下のとおりとする。  

```
[市町村コード5桁]_[市区町村名英名]_[整備年度]_3dtiles_etc_[更新回数]_op  
│   
├ 01_building
│ ├ [市町村コード5桁]_[市区町村名英名]_[整備年度]_bldg_texture
│ │       ├── data
│ │     　└── tileset.json
│ ├ [市町村コード5桁]_[市区町村名英名]_[整備年度]_bldg_low_resolution
│ │       ├── data
│ │     　└── tileset.json
│ ├ [市町村コード5桁]_[市区町村名英名]_[整備年度]_bldg_notexture
│ │       ├── data
│ │     　└── tileset.json
│ └ landmark
│        　└── _.shp
├ 02_bridge
│ └ [市町村コード5桁]_[市区町村名英名]_[整備年度]_bridge
│          ├── data
│        　└── tileset.json
├ 03_road
│ └ [市町村コード5桁]_[市区町村名英名]_[整備年度]_tran
├ 04_railway
│ └ _.json
├ 05_park
│ ├  _.json
│ └ [市町村コード5桁]_[市区町村名英名]_[整備年度]_park
├ 06_urbanplan
│ ├ [市町村コード5桁]_[市区町村名英名]_[整備年度]_toshikeikaku
│ ├ [市町村コード5桁]_[市区町村名英名]_[整備年度]_yotochiiki
│ └ [市町村コード5桁]_[市区町村名英名]_[整備年度]_chiikichiku
├ 07_landuse
│ └ [市町村コード5桁]_[市区町村名英名]_[整備年度]_luse
├ 08_emergency_road
│ └  _.json
├ 09_fld_ntl 
│ ├ [市町村コード5桁]_[市区町村名英名]_[整備年度]_fld_mlit
│ │      └── [水系名]_[河川名]_[計画規模/想定最大規模]
│ │             ├── data
│ │             └── tileset.json
│ └ [市町村コード5桁]_[市区町村名英名]_[整備年度]_fld_texture_mlit
│        └── [水系名]_[河川名]_[計画規模/想定最大規模]
│  　            ├── data
│   　  　       └── tileset.json
├ 10_fld_pref 
│ ├ [市町村コード5桁]_[市区町村名英名]_[整備年度]_fld_pref
│ │      └── [水系名]_[河川名]_[計画規模/想定最大規模]
│ │             ├── data
│ │             └── tileset.json
│ └ [市町村コード5桁]_[市区町村名英名]_[整備年度]_fld_texture_pref
│        └── [水系名]_[河川名]_[計画規模/想定最大規模]
│  　            ├── data
│   　  　       └── tileset.json
├ 11_dosha
│ ├  [市町村コード5桁]_[市区町村名英名]_[整備年度]_dosekiryu
│ ├ [市町村コード5桁]_[市区町村名英名]_[整備年度]_jisuberi
│ └ [市町村コード5桁]_[市区町村名英名]_[整備年度]_kyukeisha
├ 12_tsunami
│ ├ [市町村コード5桁]_[市区町村名英名]_[整備年度]_tsunami
│ │       ├── data
│ │     　└── tileset.json
│ └ [市町村コード5桁]_[市区町村名英名]_[整備年度]_tsunami_texture
│          ├── data
│    　  　└── tileset.json
├ 13_takashio
│ ├ [市町村コード5桁]_[市区町村名英名]_[整備年度]_takashio
│ │       ├── data
│ │     　└── tileset.json
│ └ [市町村コード5桁]_[市区町村名英名]_[整備年度]_takashio_texture
│          ├── data
│    　  　└── tileset.json
└ 14_naisuihanran
   ├ [市町村コード5桁]_[市区町村名英名]_[整備年度]_naisuihanran
   │       ├── data
   │     　└── tileset.json
   └ [市町村コード5桁]_[市区町村名英名]_[整備年度]_naisuihanran_texture
            ├── data
       　  　└── tileset.json
```
 (例: 01100_sapporo-shi_2020_3dtiles_etc_2_op) 

なお、建物モデル（01_building）については、特に建物の数が多く、描画パフォーマンスが悪い場合に、都市を複数の地域に分割して3DTilesの整備を行った。東京都は特別区単位、名古屋市、大阪市は行政区単位で作成したが命名基準に変更はなく、01_building以下に格納される3DTilesの数が多くなるのみである。  
政令市以外で同様の措置がとられた都市 **（岡崎市）** については、以下の命名基準に則って格納した。

```
[市町村コード5桁]_[市区町村名英名]_[整備年度]_3dtiles_etc_[更新回数]_op  
│   
├ 01_building
│ ├ [市町村コード5桁]_[地域名英名]_[整備年度]_bldg
│ │       ├── data
│ │     　└── tileset.json
│ ├ [市町村コード5桁]_[地域名英名]_[整備年度]_bldg_low_resolution
│ │       ├── data
│ │     　└── tileset.json
│ ├ [市町村コード5桁]_[地域名英名]_[整備年度]_bldg_notexture
│ │       ├── data
│ │     　└── tileset.json
│ └ ・・・
```
**岡崎市における地域名英名：honcho, iwazu, mutsumi, nukata, ohira, okazaki, tobu, yahagi)**
<br>

### 5. GeoJSON形式のファイル命名規則
GeoJSON形式のデータのファイル命名規則は以下のとおりとする。

鉄道
```
[市町村コード5桁]_[市区町村名英名]_[整備年度]_railway.json
```
(例: 07203_koriyama-shi_park.json）

公園
```
[市町村コード5桁]_[市区町村名英名]_[整備年度]_park.json
```
(例: 07203_koriyama-shi_park.json）

緊急輸送道路
```
[市町村コード5桁]_[市区町村名英名]_[整備年度]_emergency_route.json
```
(例: 07203_koriyama-shi_emergency_route.json）

### 6. Shape形式のファイル命名規則
Shape形式のデータのファイル命名規則は以下のとおりとする。

ランドマーク
```
[市町村コード5桁]_[市区町村名英名]_[整備年度]_landmark.shp, *.shx, *.dbf, *.prj
```
### 各構成要素の意味は以下のとおりとする。
| 構成要素 | 説明 |
|:-|:-|
| 計画規模/想定最大規模 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| 計画規模の場合は「l1」を、想定最大規模の場合は「l2」を使用する。 |