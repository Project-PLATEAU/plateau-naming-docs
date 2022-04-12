# Project PLATEAUオープンデータ-ファイル命名規則及びフォルダ構成規則

### 1. 本ドキュメントの説明
　本ドキュメントは、国土交通省都市局がProject PLATEAUとして公開するオープンデータのダウンロードファイル命名規則及びフォルダ構成規則を公開することにより、利用者の検索、ダウンロード、データを利用した開発等の利便性を向上させることを目的とする。

### 2. ファイル名の表記の方法
　ケバブケース (kebab case)を用いる。すなわち、文字は半角英数字とし、単語間は「_」（半角アンダーバー）又は「-」（半角ハイフン）で繋ぐこととする。

### 3. ダウンロードファイルの単位
Project PLATEAUが[G空間情報センター](https://www.geospatial.jp/ckan/dataset/plateau)においてオープンデータとして公開するダウンロードファイル（以下、「ダウンロードファイル」という。）は、 Zip形式又は7z形式により、市区町村単位で提供する。  
ファイルの圧縮はルートフォルダのみを対象とし、その内部のいかなるサブフォルダにも圧縮形式のファイルを含んではならない。

### 4. ダウンロードファイル命名規則（総則）
　ダウンロードファイルの命名は原則として以下の規則に従う。

```
[市区町村コード]_[市区町村名英名]_[整備年度]_[形式名]_[更新回数]_op
```
<dl><dt>例</dt>
<dd>01100_sapporo-shi_2021_citygml_2_op.zip</dd>
<dd>01100_sapporo-shi_2021_3dtiles_etc_1_op.zip</dd>
<dd>13101_chiyoda-ku_2021_fbx_2_op.zip</dd>
</dl>

  
#### 各項目の解説は以下のとおり。

* 市町村コード5桁: 総務省が定める[「全国地方公共団体コード」](https://www.soumu.go.jp/denshijiti/code.html")の上5桁を数字で表す。

* 市区町村名英名: デジタル庁が定める[「行政基本情報データ連携モデル_住所」](https://cio.go.jp/guides)に従う。すなわち、市区町村名称を国土地理院が定める「地名等の英語表記規程」（平成 28 年国地達第 10 号）に準拠しつつ、市区町村の種別はcityやwardではなく-shiや-kuで表す。

* 整備年度: データセットが作成された年度を4桁の西暦で表す。

* 形式名: 各データ形式ごとに以下の形式名とする。

| データ形式 | 形式名 |
|:-----------|:-----------|
| CityGML形式 | citygml |
| 3Dtiles形式、Shapefile形式、GeoJSON形式、MVT形式 | 3dtiles_etc |
| FBX形式 | fbx |
| OBJ形式 | obj |
| GeoTIFF形式 | ortho |

* 更新回数: 整備年度ごとに加算する。最初のデータセットは1とする。

* op: オープンデータであることを表す識別子。

### 5. 各データ形式のファイル命名規則及びフォルダ構成規則
各データ形式ごとのファイル命名規則及びフォルダ構成規則は以下のドキュメントを参照すること。

| データ形式 | 規則 |
|:-----------|:-----------|
| CityGML形式 | [「3D都市モデル標準作業手順書（第2.0版）」](https://www.mlit.go.jp/plateau/libraries/)  5.4   <br> ※PLATEAUウェブサイトへのリンク |
| 3Dtiles形式、Shapefile形式、GeoJSON形式、MVT形式 | [3dtiles等ファイル命名規則](/plateau-naming-docs/plateau-3dtiles_etc-naming.md) |
| FBX形式 | [plateau-fbx-naming](/plateau-naming-docs/plateau-fbx-naming.md) |
| OBJ形式 | [plateau-obj-naming](/plateau-naming-docs/plateau-obj-naming.md) |
| GeoTIFF形式 | [orthoファイル命名規則](/plateau-naming-docs/plateau-ortho-naming.md) |

### 6. G空間情報センターAPIを利用したダウンロードリストの取得
G空間情報センターでは、APIを利用してダウンロードリストを作成することができる。  
APIの利用方法については、[Ｇ空間情報センターAPI利用マニュアル](https://s3-ap-northeast-1.amazonaws.com/gic-manual/gic-api.pdf)を参照すること。
  
  
#### ダウンロードリスト取得のチュートリアル  
* G空間情報センターAPIを用いてCityGML形式の3D都市モデルのダウンロードリストを作成する方法を紹介します。  
PLATEAUのオープンデータは本ドキュメント等に基づく命名規則によって作成されているため、データセット名称に紐づけた検索を行うことで各データセットのURLを一括して入手可能です。  
*  G空間情報センターAPIのうち、resource_searchを用いてplateau及びcitygmlに紐づけた検索を行います。  
次の文字列をウェブブラウザに入力してください。  
https://www.geospatial.jp/ckan/api/3/action/resource_search?query=name:plateau&query=name:citygml  
* JSON形式のデータが返され、ブラウザに表示あるいはファイルがダウンロードされます。  
これをアプリで直接利用したり、人が利用しやすいように加工することが可能です。
例えば、人が見やすくする加工の方法として、次のサイトでCSVに変換することなどが可能です。  
https://konklone.io/json/  
* このような手順でその時点で公開しているPLATEAUのダウンロードファイルのURLを取得できます。
* 他にも、以下のように、市町村名に紐づけたダウンロードリストの取得等も可能です。  
https://www.geospatial.jp/ckan/api/3/action/resource_search?query=url:tokyo23kufbx


### 7. 特記事項
　東京都23区については、利便性を考慮し、特別区単位ではなく23区全域を対象とした[データセット](https://www.geospatial.jp/ckan/dataset/plateau-tokyo23ku)を提供する。この際の市区町村名は「tokyo23ku」とし、市区町村コードは東京都のコードである130001を採用する。

<dl><dt>例</dt>
<dd>13100_tokyo23ku_2020_citygml_2_op.zip</dd></dl>

　また、データの扱いやすさの観点から、東京都23区については[「JISX0410地域メッシュコード」](http://www.stat.go.jp/data/mesh/index.html)に定められた基準地域メッシュ（第3次地域区画、一辺の長さ約1km）単位のデータセットを別途提供する。

<dl><dt>例</dt>
<dd>13100_tokyo23ku_2020_533925_citygml_2_op.zip</dd></dl>


