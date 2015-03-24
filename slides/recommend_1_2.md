## rambulance

* Railsエラー画面生成用gem
* HTTP Statuses と Exceptionをマッピングして使用するテンプレートファイルを設定出来る

```ruby
Rambulance.setup do |config|
  config.rescue_responses = {
    "ActiveRecord::RecordNotUnique" => :unprocessable_entity,
    "CanCan::AccessDenied"          => :forbidden,
    "Pundit::NotAuthorizedError"    => :forbidden,
    "YourCustomException"           => :not_found
  }

  # The template name for the layout of the error pages. The default value is
  # 'application'. For exmaple, if this value is set to "error_page", Rambulance uses
  # 'app/views/layout/error_page.html.erb' as a layout for all the error pages.
  config.layout_name = "login"

  # The directry name to organize error page templates. The default value is
  # 'errors'. For exmaple, if this value is set to "error_pages", Rambulance
  # uses e.g. 'app/views/error_pages/not_found.html.erb'.
  config.view_path = "errors"

end
```
* エラーページ確認用URLも生成してくれるので、簡単に確認出来て便利
