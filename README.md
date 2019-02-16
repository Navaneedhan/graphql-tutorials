Commands to Execute:

rails new graphql-tutorials
cd graphql-tutorials/
rails db:create
rails s
rails generate graphql:install

sqlite3 dependency:
gem 'sqlite3', '~> 1.3', '< 1.4'

Adding graphQL gem:
gem 'graphql', '1.8.13'

Changing graphql-rails gem for dev:
gem 'graphiql-rails', '1.5.0', group: :development

Creating links model:
rails generate model Link url:string description:text

Creating links from console:
Link.create url: 'http://graphql.org/', description: 'The Best Query Language'
Link.create url: 'http://dev.apollodata.com/', description: 'Awesome GraphQL Client'
exit