
## Adapters

* adapterの指定はこんな感じ

```ruby
# lib/bookshelf.rb

#  * File System adapter
adapter type: :file_system, uri: 'file:///db/bookshelf_development'

#  * Memory adapter
adapter type: :memory, uri: 'memory://localhost/bookshelf_development'

#  * SQL adapter
adapter type: :sql, uri: 'sqlite://db/bookshelf_development.sqlite3'
adapter type: :sql, uri: 'postgres://localhost/bookshelf_development'
adapter type: :sql, uri: 'mysql://localhost/bookshelf_development'
```
