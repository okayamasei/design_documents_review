# テーブル定義書問題指摘
## 全体
- テーブル名がスネークケースじゃない。また、複数形じゃない
- テーブル名_idではなく、idというカラムだけでいい

## admins
- 主キーにindexがない
- メールアドレスとパスワードはテーブル名から判断できるので、頭にadmin_はつけなくていい

## users
- member_statusは何のステータスかわからないので、わかりやすい名前にする
	>データ型はintegerで、enumは備考欄にのみかけばいい
- 名前（性）、名前（名）、名前(性カナ)、名前(名カナ)のカラム名は略語を使わない
	>また、性ではなく姓

## ships
- 主キーにindexがない
- ship_name, ship_address, ship_tel, ship_codeはテーブル名から判断できるので、頭にship_はつけなくていい

## products
- 主キーにsをつけない
- cd_titleのindexは不要

## discs
- disc_numのdisc_は不要
- 外部キーであるproducts_idはproduct_idにする

## songs
- 曲名だとわかるようなわかりやすいカラム名にする

## labels
- レーベル名だとわかるようなわかりやすいカラム名にする

## artists
- アーティスト名とわかるようなわかりやすいカラム名にする

## genres
- ジャンル名だとわかるようなわかりやすいカラム名にする

## cart items
- テーブル名をcart_itemsにして、空白に_を挿入する。また、indexをつける
- buy numはスネークケースにする
	>また、カラム名から内容が推測できないのでわかりやすい名前にする。
- products_idはproduct_idにする


## order_detail
- order_details_Idは、sをとる。また、Iは小文字
- products_idはsをとる
	>Fkをつける

## order
- 主キーにindexがない
- totalは何のtotalかわからない。

# 注意
* マークダウン形式で記入してください。
* 全体を通しての指摘事項の場合、テーブル名の部分を「全体」「共通」などとしてください。
