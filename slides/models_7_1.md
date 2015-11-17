
## Mapping

```ruby
# マッピング
collection :books do
  entity     Book
  repository BookRepository

  attribute :id,        Integer
  attribute :name,      String
  attribute :price,     String
  attribute :code,      String
  attribute :author_id, Integer
end
```
