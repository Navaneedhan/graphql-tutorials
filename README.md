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

GraphQL queries or requests:
mutation {
  createLink (
    url:"https://www.howtographql.com/graphql-ruby/5-new/",
    description: "this link is for new"
  ) {
    id
    url
    description
  }
}

# {
#   allLinks {
#     id
#     url
#     description
#   }
# }

# mutation {
#   createUser (
# 		name: "John Doe"
#     authProvider: {
#       email: {
#       	email: "john.doe@ex.com",
#       	password: "test123"
#     	}
#     }
#   ) {
#     id
#     name
#     email
#   }
# }

# {
#   allUsers {
#     id
#     name
#     email
#   }
# }

# mutation {
#   signinUser(
#     email: {
#     	email: "john.doe@ex.com" ,
#       password: "test123"
#     }
#   ) {
#     token
#     user {
#       id
#       name
#       email
#     }
#   }
# }