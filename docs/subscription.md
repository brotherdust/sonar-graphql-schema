```graphql
"""The connection wrapper around the `SubscriptionConnection` type."""
type SubscriptionConnection {
  """A list of the entities provided by this connection."""
  entities: [Subscription]!
  """
  An object providing information about the page of results being displayed, as
  well as the total amount of pages/records available.
  """
  page_info: PageInfo!
  """
  Provides the ability to return aggregated mathematical data about your results.
  """
  aggregations: [Aggregation]!
}
```
