
## Mapping

* エンティティのアトリビュートとDBのテーブルのカラムのマッピングは、自分で行う必要がある
  * Railsのようによしなにはしてくれない

```ruby
# エンティティ
class Book
  include Lotus::Entity
  attributes :name, :price, :code, :author_id
end

# テーブル
create_table :books do
  primary_key :id
  foreign_key :author_id, :authors, on_delete: :cascade, null: false

  column :name, String,   null: false
  column :price, Integer, null: false
  column :code,  String,  null: false, unique: true, size: 128

  check { price > 0 }
end
```
