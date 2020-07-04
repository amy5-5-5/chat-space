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

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false, unique: true|
|nickname|string|null: false, unique: true|

- has_many: groups
- has_many: messages
- has_many: members

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foregn_key: true|
|name|string| null: false, unique: true|

- has_many: members
- has_many: messages
