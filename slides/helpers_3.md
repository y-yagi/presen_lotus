
## Formの例

```erb
<h2>Add book</h2>
<% unless params.valid? %>
  <div class="errors">
    <h3>There was a problem with your submission</h3>
    <ul>
      <% params.errors.each do |error| %>
        <li><%= error.attribute_name %> is required</li>
      <% end %>
    </ul>
  </div>
<% end %>
<%=
  form_for :book, routes.books_path do
    div class: 'input' do
      label      :name
      text_field :name
    end

    div class: 'controls' do
      submit 'Create Book'
    end
  end
%>
```
