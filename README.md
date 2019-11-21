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
