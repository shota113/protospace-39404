# テーブル設計

## users テーブル

| Column                | Type        | Options                           |
|---------------------- | ----------  | --------------------------------  |
| email                 | string      | null: false                       |
| encrypted_password    | string      | null: false                       |
| name                  | string      | null: false                       |
| profile               | text        | null: false                       |
| occupation            | text        | null: false                       |
| position              | text        | null: false                       |

## prototypes テーブル

| Column                | Type        | Options                           |
|---------------------- | ----------  | -------------------------------   |
| title                 | string      | null: false                       |
| catch_copy            | string      | null: false                       |
| concept               | string      | null: false                       |
| user                  | references  | null: false, foreign_key: true    |

## comments テーブル

| Column                | Type        | Options                           |
|---------------------- | ----------  | -------------------------------   |
| content               | text        | null: false                       |
| prototype             | references  | null: false, foreign_key: true    |
| user                  | string      | null: false, foreign_key: true    |