# DB設計
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|email|string|null: false|
|password|string|null: false|

### Association
- has_many :users_groups
- has_many :messages

## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|text|text||
|image|text||
|user_id|integer|null: false, foreign_key: true|

### Association
- belong_to :user
- belong_to :group

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|member|string||

### Association
- has_many :users_groups
- has_many :massages

## users_groupsテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user


