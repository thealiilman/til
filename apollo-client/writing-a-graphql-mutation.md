# Writing a GraphQL Mutation
Just like writing a GraphQL query, we need to use `gql`. `gql` is used to write GraphQL operations. More info is available in [apollo-server's documentation](apollographql.com/docs/apollo-server/api/apollo-server/#gql).

```javascript
import { gql } from 'apollo-boost'
const addBookMutation = gql`
  mutation($title: String!, $genre: String!, $authorId: ID!) {
    addBook(title: $title, genre: $genre, authorId: $authorId) {
      id
      title
      genre
    }
  }
`
```
