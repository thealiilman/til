# Executing a GraphQL Mutation
To execute a GraphQL mutation, we first need the mutation that we want to execute.

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

Then, we utilise the `useMutation` React hook provided by `@apollo/react-hooks`.
```javascript
import { useMutation } from '@apollo/react-hooks'
const [addBook, mutationResult] = useMutation(addBookMutation)

addBook({
  // The variables property can be considered as the arguments you want to pass to the GraphQL mutation.
  variables: {
    name: 'London',
    genre: 'Historical Fiction',
    authorId: 'abc123xyz',
  }
}
```
The first destructured element (`addBook`) is the mutate function. The second argument is the mutation result, which consist of properties such as `loading` and `data`.

Refer to this (wonderfully organised) [documentation](https://www.apollographql.com/docs/react/data/mutations/#usemutation-api) for more info about the _mutate function_'s arguments and _mutation result_'s properties.
