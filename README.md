# README
## messageテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foregn_key: true|
|body|text|
|image|string|
### Association
- belongs_to :group
- belongs_to :user

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false, unique: true|
|nickname|string|null: false, unique: true|
### Association
- has_many :groups
- has_many :groups, through: :groups_users
- has_many :messages
- has_many :members

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string| null: false, unique: true|
### Association
- has_many :members
- has_many :messages
- has_many :users


## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foregn_key: true|
### Association
- belongs_to :group
- belongs_to :user
