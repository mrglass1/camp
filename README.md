# README

#rails tutorial

# create new rails projects without tests
# and specify database 
rails new projectname -T --database=postgresql

# scaffold a feature
rails g scaffold Blog string:title text:body

# display current routes
rake routes

# markdown tutorial
markdowntutorial.com
leanpub.com

# controller create
rails g controller Pages home about contact

# model generator
rails g model Skill title:string percent_utilized:integer

# rails console
# populate sample Skill data
Skill.create!(title: "Rails", percent_utilized: 75)
Skill.create!(title: "Rails", percent_utilized: 75)
Skill.create!(title: "Rails", percent_utilized: 75)

# rails resource generator
rails g resource Portfolio title:string subtitle:string body:text main_image:text thumbnail:text

# seeds file with iterator
# sample data : placeholder image : "http://via.placeholder.com/600x400"


# delete data from dev env
rails db:setup

# views - render images
<%= image_tag portfolio_item.thumbnail %>

# creating links
<%= link_to "Create New Item", new_portfolio_path %>
<a href="portfolios/new" title="">Create New Item</a>
<%= new_portfolio_url, subdomain: 'my subdomain'%> # url to use sub domain

# sample index with link_to
<% @portfolio_items.each do |portfolio_item| %>
  <p><%= link_to portfolio_item.title, portfolio_path(portfolio_item)  %></p> # .id not required
  <p><%= portfolio_item.subtitle %></p>
  <p><%= portfolio_item.body %></p>
  <%= image_tag portfolio_item.thumbnail unless portfolio_item.thumbnail.nil? %>
  <%= link_to "Edit", edit_portfolio_path(portfolio_item) %>
<% end %>

# deleting and destroying records
# portfolio_path the verb is GET by default, you have to pass the method for other verbs
<%= link_to 'Delete portfolio item', portfolio_path(portfolio_item), method: :delete, data: { confirm: 'Are you sure?' } %><

# routes
# setting root to home in routes.rb
root to: 'pages#home'
# other, left hand side is the controller, right hand side is the method
get 'about', to: 'pages#about'
get 'contact', to: 'pages#contact'