# model generator
rails g model Skill title:string percent_utilized:integer

# rails c
# populate sample Skill data
Skill.create!(title: "Rails", percent_utilized: 75)
Skill.create!(title: "Rails", percent_utilized: 75)
Skill.create!(title: "Rails", percent_utilized: 75)