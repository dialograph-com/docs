# docs
dialograph documentation - docs.dialograph.com



## tools [Dgraph Cloud Quick Start - Dgraphcloud](https://dgraph.io/docs/dgraphcloud/cloud-quick-start/)



+ [Vega Editor](https://vega.github.io/editor/#/custom/vega)
+ [Dgraph Cloud](https://cloud.dgraph.io/_/explorer)

> ## The Schema
> 
> The schema for our “to-do” app has only two types: `Tasks` and `Users`. The schema itself is pretty simple: it’s a standard GraphQL schema, with a few additional directives (such as `@search`) which are specific to Dgraph Cloud.
> 
> Let’s define the Dgraph Cloud schema for our app:
> 
>     type Task {
>       id: ID!
>       title: String! @search(by: [fulltext])
>       completed: Boolean! @search
>       user: User!
>     }
>     
>     type User {
>       username: String! @id @search(by: [hash])
>       name: String @search(by: [exact])
>       tasks: [Task] @hasInverse(field: user)
>     }


