
## Migrations

```ruby
Lotus::Model.migration do
  change do
    create_table :books do
      primary_key :id
      foreign_key :author_id, :authors, on_delete: :cascade, null: false

      column :code,  String,  null: false, unique: true, size: 128
      column :title, String,  null: false
      column :price, Integer, null: false, default: 100 # cents

      check { price > 0 }
    end
  end
end
```
* `change`はRails同様、リバーシブルでよしなにやってくれる
* `up`/`down`も使える
* migrationはSequel のメソッドを使用しているだけなので、詳細はSequelのdoc([schema_modification.rdoc](http://sequel.jeremyevans.net/rdoc/files/doc/schema_modification_rdoc.html))参照
