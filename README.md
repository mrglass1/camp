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

# rails c
# populate sample Skill data
Skill.create!(title: "Rails", percent_utilized: 75)
Skill.create!(title: "Rails", percent_utilized: 75)
Skill.create!(title: "Rails", percent_utilized: 75)

