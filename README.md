# DB設計

## users tab 

|Column|Type|Options|
|------|----|-------|
|name|string|index: true, null: false, unique: true|
|mail|string|null: false|

 ### Association
  - has.many :grops, through: menmbers
  - has.many :messages
  - has.many :members