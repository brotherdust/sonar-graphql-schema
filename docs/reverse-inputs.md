```graphql
"""
The input object that defines the fields for the reversePayment mutation.
"""
input ReversePaymentMutationInput {
  """The amount to reverse."""
  amount: Int!
  """Why this reversal was performed."""
  description: String
}

"""
This filter type allows you to filter the root entity by a relation. For
example, you could search for all `Account`s that have an `Address` with a specific city.
"""
input ReverseRelationFilter {
  """
  The relation you wish to apply the reverse relation filter on. Should be a
  string that is the exact relation name (e.g. `contacts`, `addresses`,
  `account_status`.) You can filter on a deeper relation by using periods to
  separate the relation names (e.g. `contacts.phone_numbers`.)
  """
  relation: String!
  """Complex search parameters."""
  search: [Search]
  """Search across all string fields with partial matching."""
  general_search: String
  """Only include results where this relation is unset."""
  is_empty: Boolean = false
  """
  Every reverse relation filter in the same query that is in the same group will
  be treated as an `AND`. Reverse relation filters in other groups will be
  treated as an `OR`.
  """
  group: String = "1"
}

"""The fields necessary to reverse a transaction."""
input ReverseTransactionMutationInput {
  """
  A log entry to store to describe why this transaction is being reversed.
  """
  message: String!
}
```
