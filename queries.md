# queries for compose faq screen

graphql url: `http://localhost:1337/graphql`

## get questions by category id

```graphql
query {
  faqCategory(id: 1) {
    data {
      id
      attributes {
        title
        description
        faq_questions {
          data {
            id
            attributes {
              title
              short_description
            }
          }
        }
      }
    }
  }
}
```

## get questions by tag id

```graphql
query {
  faqSearchTag(id: 1) {
    data {
      attributes {
        title
        faq_questions {
          data {
            id
            attributes {
              title
              short_description
            }
          }
        }
      }
    }
  }
}
```
