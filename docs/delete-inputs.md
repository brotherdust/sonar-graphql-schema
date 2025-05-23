```graphql
"""
The input object that defines the fields for the deleteAccountService mutation.
"""
input DeleteAccountServiceMutationInput {
  """Whether or not to prorate the transaction."""
  prorate: Boolean
  """The date to prorate the transaction as of."""
  proration_date: Date
}

"""
The input object that defines the fields for the deleteGenericInventoryItems mutation.
"""
input DeleteGenericInventoryItemsMutationInput {
  """The quantity for this service."""
  quantity: Int!
}

"""The fields necessary to delete a transaction."""
input DeleteInventoryItemSegmentMutationInput {
  """
  Determines how updates or deletions to a segment will handle the quantity adjustment.
  """
  segment_modifier: InventoryItemSegmentModifierType!
}

"""Provides request options when deleting a reversed payment."""
input DeleteReversedPaymentMutationInput {
  """Apply this payment to any open invoices."""
  apply_to_open_invoices: Boolean!
}

"""The fields necessary to delete a transaction."""
input DeleteTransactionMutationInput {
  """The reason for deletion of this transaction."""
  message: String!
}

"""
The input object that defines the fields for the deleteVoiceServiceGenericParameter mutation.
"""
input DeleteVoiceServiceGenericParameterMutationInput {
  """Whether or not to prorate the transaction."""
  prorate: Boolean
  """The date to prorate the transaction as of."""
  proration_date: Date
}
```
