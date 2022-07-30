##  usersテーブル
| Column              | Type       | Options                        |
| ------------------- | ---------- | ------------------------------ |
| email               | string     | null: false,  foreign_key:true |
| encrypted_password  | string     | null: false,                   |
| name                | string     | null: false,                   |
| profile             | text       | null: false,                   |
| occupation          | text       | null: false,                   |
| position            | text       | null: false,                   |

### Association 
- has_many :commens
- has_many :prototypes

##  commetsテーブル
| Column              | Type       | Options                        |
|content              | text       | null: false                    |
|prototype            | refernces  | null: false                    |
|user                 | refernces  | null: false                    |


### Association
- belongs_to :prototypes
- belongs_to :users

## prototypesテーブル
| Column              | Type       | Options                        |
|title                | string     | null:false                     |
|catch_copy           | text       | null: false                    |
|concept              | text       | null: false                    |
|user                 | references | null: false                    |
### Association
- belongs_to :users
- has_many   :commets

