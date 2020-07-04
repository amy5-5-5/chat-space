# README
## messeageテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foregn_key: true|
|body|text|null: false|
|image|string|

- belongs_to :group
- belongs_to :user