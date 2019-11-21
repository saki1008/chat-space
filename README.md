# DB設計

## users table

|Column|Type|Options|
|------|----|-------|
|name|string|index: true, null: false, unique: true|
|mail|string|null: false|
 ### Association
  - has.many :grops, through: menmbers
  - has.many :messages
  - has.many :members

  ## groups table

|Column|Type|Options|
|------|----|-------|
|name|string|index: true, null: false, unipue: true|
### Association
 - has_many :users, through: :group_users
 - has_many :group_users
 - has_many :messages


## message table

|Column|type|Option|
|------|----|------|
|body| text | null: false |
| image    | string  |  |
| group | references | foreign_key: true |
| user  | references | foreign_key: true |
## Association
- belongs_to :user
- belongs_to :group



## group_users table

| Column    | type    | Option |
|-----------|---------|--------|
| group  | references | index: true, foreign_key: true, null: false |
| user   | references | index: true, foreign_key: true, null: false |
## Association
* belongs_to :group
* belongs_to :user