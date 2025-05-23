```graphql
"""The event that triggers a specific `Email`."""
enum EmailTrigger {
  """A user forgets their password and requests a new one"""
  USER_FORGOT_PASSWORD
  """A new user is created"""
  NEW_USER_CREATED
  """A credit card is expiring"""
  CREDIT_CARD_EXPIRING
  """An automatic payment succeeds"""
  AUTOPAY_SUCCESS
  """An automatic payment fails"""
  AUTOPAY_FAILURE
  """A payment succeeded"""
  PAYMENT_SUCCESS
  """A payment failed"""
  PAYMENT_FAILURE
  """Billing runs successfully for an account"""
  MONTHLY_BILLING
  """An initial invoice is generated for a newly activated account"""
  INITIAL_INVOICE
  """An account becomes delinquent"""
  ACCOUNT_BECOMES_DELINQUENT
  """An invoice is due in X days"""
  INVOICE_DUE_IN_X_DAYS
  """An invoice will become delinquent in X days"""
  INVOICE_DELINQUENT_IN_X_DAYS
  """An invoice is past due for X days."""
  INVOICE_PAST_DUE_FOR_X_DAYS
  """An invoice has been delinquent for X days"""
  INVOICE_DELINQUENT_FOR_X_DAYS
  """An account is activated for the first time"""
  ACCOUNT_FIRST_ACTIVATED
  """A contract pending signature is emailed to a contact"""
  SEND_UNSIGNED_CONTRACT
  """A late fee is applied to an account"""
  LATE_FEE_APPLIED
  """A credit card or bank account payment is refunded"""
  PAYMENT_REFUNDED
  """A job is scheduled"""
  JOB_SCHEDULED
  """An account hits X% of their bandwidth cap"""
  ACCOUNT_AT_X_PERCENTAGE_OF_BANDWIDTH_CAP
  """A signed contract is emailed to a contact"""
  SEND_SIGNED_CONTRACT
  """An invoice is manually emailed to a contact"""
  EMAIL_INVOICE
  """A receipt for a payment."""
  PAYMENT_RECEIPT
  """An account address is changed."""
  ACCOUNT_ADDRESS_CHANGED
  """A contact's password is changed."""
  CONTACT_PASSWORD_CHANGED
}

"""The event that triggers a specific message."""
enum MessageTrigger {
  """A new user is created"""
  NEW_USER_CREATED
  """A user forgets their password and requests a new one"""
  USER_FORGOT_PASSWORD
  """A credit card is expiring"""
  CREDIT_CARD_EXPIRING
  """An automatic payment succeeds"""
  AUTOPAY_SUCCESS
  """An automatic payment fails"""
  AUTOPAY_FAILURE
  """A payment succeeded"""
  PAYMENT_SUCCESS
  """A payment failed"""
  PAYMENT_FAILURE
  """Billing runs successfully for an account"""
  MONTHLY_BILLING
  """An initial invoice is generated for a newly activated account"""
  INITIAL_INVOICE
  """An account becomes delinquent"""
  ACCOUNT_BECOMES_DELINQUENT
  """An invoice is due in X days"""
  INVOICE_DUE_IN_X_DAYS
  """An invoice will become delinquent in X days"""
  INVOICE_DELINQUENT_IN_X_DAYS
  """An invoice is past due for X days."""
  INVOICE_PAST_DUE_FOR_X_DAYS
  """An invoice has been delinquent for X days"""
  INVOICE_DELINQUENT_FOR_X_DAYS
  """An account is activated for the first time"""
  ACCOUNT_FIRST_ACTIVATED
  """A contract pending signature is emailed to a contact"""
  SEND_UNSIGNED_CONTRACT
  """A late fee is applied to an account"""
  LATE_FEE_APPLIED
  """A credit card or bank account payment is refunded"""
  PAYMENT_REFUNDED
  """A job is scheduled"""
  JOB_SCHEDULED
  """An account hits X% of their bandwidth cap"""
  ACCOUNT_AT_X_PERCENTAGE_OF_BANDWIDTH_CAP
  """A signed contract is emailed to a contact"""
  SEND_SIGNED_CONTRACT
  """An invoice is manually emailed to a contact"""
  EMAIL_INVOICE
  """A receipt for a payment."""
  PAYMENT_RECEIPT
  """An account address is changed."""
  ACCOUNT_ADDRESS_CHANGED
  """A contact's password is changed."""
  CONTACT_PASSWORD_CHANGED
}
```
