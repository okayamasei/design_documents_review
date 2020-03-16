# アプリケーション詳細設計_レビュー

## 全体
- deviseのルーティングがない。
- 使用するgemの記載がない。

## public
### 共通
- URLに顧客のidを含んでいる。
- 注文情報確認画面、注文完了画面、退会確認画面に相当するアクションがない。

### end_users
- 退会処理のメソッドがDELETEになっている。
 
### cart_items
- 不要なアクションeditがある。
- "カートを空にする"に相当するアクションがない。
 
### order_items
- orders#index,showであるべきなのにorder_items#index,showになっている。

### address
- 複数形になっていない。x address → o addresses


## admin
### 共通
- 管理者のトップページがない。
- 製作ステータスの更新に相当するアクションがない。

### items
- newアクションのURLが不適当。
- 不要なアクションdestroyがある。

### genres
- updateアクションがない。

### order_items
- publicと同じく、注文履歴はorder_itemsではなくordersである。

# 注意
* マークダウン形式で記入してください。
* 全体を通しての指摘事項の場合、テーブル名の部分を「全体」「共通」などとしてください。
