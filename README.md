# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

# テーブル設計

## user テーブル

| Column       | Type       | Options         |
| ____________ | __________ | _______________ |
| nickname     | string     | null: false     |

### Association
- has_many :bookmark
- has_many :shops


## bookmark テーブル

| Column       | Type       | Options         |
| ____________ | __________ | _______________ |
| favorite     | string     |                 |
| user_id      | integer    | null: false     |
| shop_id      | integer    | null: false     |

### Association
- belongs_to :shop
- belings_to :user




## shop テーブル

| Column          | Type       | Optons          |
| _______________ | __________ | _______________ |
| name            | string     | null: false     |
| address         | string     | null: false     |
| phone_number    | integer    | null: false     |
| image           | string     | null: false     |
| business_hours  | string     | null: false     |
| regular_holiday | string     | null: false     |
| home_page       | string     | null: false     |
| user_id         | integer    | null: false     |

### Association
- belongs_to :user
- has_many :bookmark