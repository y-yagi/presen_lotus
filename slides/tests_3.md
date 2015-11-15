
## Test

* Railsのようにテスト用のクラスを提供している訳では無く、普通のRubyファイルに対するテストを行う

アクションのテストの例

```
# spec/web/controllers/dashboard/index_spec.rb
require 'spec_helper'
require_relative '../../../../apps/web/controllers/dashboard/index'

describe Web::Controllers::Dashboard::Index do
  let(:action) { Web::Controllers::Dashboard::Index.new }
  let(:params) { Hash[] }

  it "is successful" do
    response = action.call(params)
    response[0].must_equal 200
  end
end
```
