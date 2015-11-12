
## Layout

* Layoutも指定可能
  * デフォルトでは`application.html.erb`が使用される
* Layoutの指定は、グローバル、アクション単位、どちらでも可能
  * アクション単位の場合は、view classで`layout`メソッドを呼び出す
``ruby
module Web::Views::Books
  class New
    include Web::View
    layout 'book'
  end
end
```
