```graphql
"""
The input object that defines the fields for the createLinkedAddresses mutation.
"""
input CreateLinkedAddressesMutationInput {
  """The address ID for the Anchor address"""
  anchor_address_id: Int64Bit!
  """The unit designator for creating addresses."""
  unit_designator: UnitDesignator!
  """An address range string used in bulk address creation."""
  address_range: String!
  """IDs of `NetworkSite`s."""
  network_site_ids: [Int64Bit]
  """Address status ID."""
  address_status_id: Int64Bit
  """Whether or not shell accounts are to be created."""
  create_shell_account: Boolean!
  """The ID of the company that this entity operates under."""
  company_id: Int64Bit
  """The ID of an AccountStatus."""
  account_status_id: Int64Bit
  """The ID of an AccountType."""
  account_type_id: Int64Bit
  """A list of account group IDs that this account is part of."""
  account_group_ids: [Int64Bit]
  """Data to insert into custom fields."""
  account_custom_field_data: [CustomFieldDataMutationInput]
  """Data to insert into custom fields."""
  custom_field_data: [CustomFieldDataMutationInput]
  """
  If IDs of `CustomField` objects that are associated with this entity are
  provided here, they will be unset and removed. You cannot unset data where the
  `CustomField` property `required` is set to `true`.
  """
  unset_custom_field_data: [Int64Bit]
  """
  A list of file IDs to be associated with this object. These must first have
  been uploaded to the /files endpoint and must be currently unassociated.
  """
  files: [AssociateFileMutationInput]
}
```
