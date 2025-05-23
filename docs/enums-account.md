```graphql
"""A bank account processing provider."""
enum BankAccountProvider {
  """Authorize.net CIM (https://authorize.net)"""
  AUTHORIZE
  """Bluepay (https://www.bluepay.com)"""
  BLUEPAY
  """BMO Harris 80 byte Canadian ACH format."""
  BMOHARRISCANADA80BYTE
  """1464 byte Canada ACH"""
  CANADAACH1464BYTE
  """CardConnect (https://cardconnect.com)"""
  CARDCONNECT
  """Canada ACH for Central 1"""
  CENTRAL1ACH
  """GoCardless (https://gocardless.com)"""
  GOCARDLESS
  """IPpay (https://ippay.com)"""
  IPPAY
  """NACHA ACH"""
  NACHAACH
  """ProPay ProtectPay (https://epay.propay.com/protectpay)"""
  PROPAY
  """Canada ACH for Royal Bank of Canada"""
  ROYALBANKOFCANADAACH
  """Canada ACH FTP Upload for Royal Bank of Canada"""
  ROYALBANKOFCANADAACHFTP
  """sonarPay"""
  SONARPAY
  """sonarPay Canada"""
  SONARPAY_CANADA
}

"""Credentials for a bank account provider."""
enum BankAccountProviderCredential {
  """Authorize.net API login ID"""
  AUTHORIZE_API_LOGIN_ID
  """Authorize.net transaction key"""
  AUTHORIZE_TRANSACTION_KEY
  """IPpay terminal ID"""
  IPPAY_TERMINALID
  """Bluepay account ID"""
  BLUEPAY_ACCOUNT_ID
  """Bluepay secret key"""
  BLUEPAY_SECRET_KEY
  """Your CardConnect username."""
  CARDCONNECT_USERNAME
  """Your CardConnect password."""
  CARDCONNECT_PASSWORD
  """Your CardConnect merchant ID."""
  CARDCONNECT_MERCHANTID
  """Your ProPay biller account ID."""
  PROPAY_BILLER_ACCOUNT_ID
  """Your ProPay auth token."""
  PROPAY_AUTH_TOKEN
  """Your ProPay account number."""
  PROPAY_ACCOUNT_NUMBER
  """Your bank account number."""
  BMOHARRISCANADA80BYTE_ACCOUNT_NUMBER
  """Your company name."""
  BMOHARRISCANADA80BYTE_COMPANY_NAME
  """The destination data center code."""
  BMOHARRISCANADA80BYTE_DESTINATION_DATA_CENTER_CODE
  """The institution ID."""
  BMOHARRISCANADA80BYTE_INSTITUTION_ID
  """The originator ID."""
  BMOHARRISCANADA80BYTE_ORIGINATOR_ID
  """Your bank account number."""
  CANADAACH1464BYTE_ACCOUNT_NUMBER
  """Your company name."""
  CANADAACH1464BYTE_COMPANY_NAME
  """The destination data center code."""
  CANADAACH1464BYTE_DESTINATION_DATA_CENTER_CODE
  """The institution ID."""
  CANADAACH1464BYTE_INSTITUTION_ID
  """The originator ID."""
  CANADAACH1464BYTE_ORIGINATOR_ID
  """Your bank account number."""
  CENTRAL1ACH_ACCOUNT_NUMBER
  """Your company name."""
  CENTRAL1ACH_COMPANY_NAME
  """The destination data center code."""
  CENTRAL1ACH_DESTINATION_DATA_CENTER_CODE
  """The institution ID."""
  CENTRAL1ACH_INSTITUTION_ID
  """The originator ID."""
  CENTRAL1ACH_ORIGINATOR_ID
  """Your bank account number."""
  ROYALBANKOFCANADAACH_ACCOUNT_NUMBER
  """Your company name."""
  ROYALBANKOFCANADAACH_COMPANY_NAME
  """The destination data center code."""
  ROYALBANKOFCANADAACH_DESTINATION_DATA_CENTER_CODE
  """The institution ID."""
  ROYALBANKOFCANADAACH_INSTITUTION_ID
  """The originator ID."""
  ROYALBANKOFCANADAACH_ORIGINATOR_ID
  """Your bank account number."""
  NACHAACH_ACCOUNT_NUMBER
  """The company entry description to use in the batch."""
  NACHAACH_COMPANY_ENTRY_DESCRIPTION
  """The company identification to use in the bank."""
  NACHAACH_COMPANY_IDENTIFICATION
  """Your company name."""
  NACHAACH_COMPANY_NAME
  """The immediate destination."""
  NACHAACH_IMMEDIATE_DESTINATION
  """The immediate destination name."""
  NACHAACH_IMMEDIATE_DESTINATION_NAME
  """The immediate origin."""
  NACHAACH_IMMEDIATE_ORIGIN
  """The immediate origin name."""
  NACHAACH_IMMEDIATE_ORIGIN_NAME
  """GoCardless Access Token"""
  GOCARDLESS_ACCESS_TOKEN
  """GoCardless Webhook Endpoint Secret"""
  GOCARDLESS_WEBHOOK_ENDPOINT_SECRET
  """sonarPay Merchant ID"""
  SONARPAY_MERCHANT_ID
}

"""The type of bank account."""
enum BankAccountType {
  """A checking account."""
  CHECKING
  """A savings account."""
  SAVINGS
}
```
