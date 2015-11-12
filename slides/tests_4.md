
## Test

requestのテストの例

```
# spec/api_v1/requests/users_spec.rb
require 'spec_helper'

describe "API V1 users" do
  include Rack::Test::Methods

  before do
    @user = UserRepository.create(User.new(name: 'Luca'))
  end

  # app is required by Rack::Test
  def app
    Lotus::Container.new
  end

  it "is successful" do
    get "/api/v1/users/#{ @user.id }"

    last_response.must_be :ok?
    last_response.body.must_equal(JSON.generate(@user.to_h))
  end
end
```
featureテストはcapybaraで(デフォルトでcapybaraを使う前提のhelperが生成される)
