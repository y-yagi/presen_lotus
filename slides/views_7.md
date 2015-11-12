
## Layout

* Layoutもクラスで管理されているので、Layoutを追加したい場合、Layout用のクラスを追加する必要がある
```ruby
# apps/web/views/book_layout.rb
module Web::Views
    class BookLayout
      include Web::Layout
    end
end
```
