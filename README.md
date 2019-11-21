# DB設計

<<<<<<< HEAD
## users table
=======
## users table 
>>>>>>> 3e1b275bcdf57f9e03a3b6411c1447f2e0f67c06

|Column|Type|Options|
|------|----|-------|
|name|string|index: true, null: false, unique: true|
|mail|string|null: false|

 ### Association
  - has.many :grops, through: menmbers
  - has.many :messages
  - has.many :members
<<<<<<< HEAD

  ## groups_users table

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## posts table
|Column|Type|Options|
|------|----|-------|
|title|text|null: false|
|text|text|null: false|
|user_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user
- has_many :comments
- has_many :posts_tags
- has_many  :tags,  through:  :posts_tags

## tags table
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
### Association
- has_many :posts_tags
- has_many  :posts,  through:  :posts_tags

## comments table
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :post
- belongs_to :user
=======
>>>>>>> 3e1b275bcdf57f9e03a3b6411c1447f2e0f67c06
