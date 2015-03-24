## activeadmin

* さくっと管理画面を作るためのgem
* rails_adminとかtypusとかupminとか
* 独自DSL記法

```ruby
ActiveAdmin.register Post do

  form do |f|
    f.inputs 'Details' do
      f.input :title
      f.input :published_at, label: 'Publish Post At'
    end
    f.inputs 'Content', :body
    f.inputs do
      f.has_many :categories, heading: 'Themes', allow_destroy: true, new_record: false do |a|
        a.input :title
      end
    end
    f.inputs do
      f.has_many :comment, new_record: 'Leave Comment' do |b|
        b.input :body
      end
    end
    f.actions
  end

  member_action :comments do
    @comments = resource.comments
    # This will render app/views/admin/posts/comments.html.erb
  end

  page_action :add_event, method: :post do
    redirect_to admin_calendar_path, notice: "Your event was added"
  end

  action_item :add do
    link_to "Add Event", admin_calendar_add_event_path, method: :post
  end
end
```
