```graphql
"""A company that processes `CreditCard`s."""
enum CreditCardProvider {
  """Stripe (https://stripe.com)"""
  STRIPE
  """IPpay (http://ippay.com)"""
  IPPAY
  """BluePay (https://www.bluepay.com)"""
  BLUEPAY
  """Authorize.net CIM (https://authorize.net)"""
  AUTHORIZE
  """Bambora (https://www.bambora.com/en/us/)"""
  BAMBORA
  """CardConnect (https://cardconnect.com)"""
  CARDCONNECT
  """ProPay ProtectPay (https://epay.propay.com/protectpay)"""
  PROPAY
  """Moneris Canada eSelect Vault (https://www.moneris.com)"""
  MONERIS_CA
  """PayGate PayHost/PayVault (https://www.paygate.co.za/)"""
  PAYGATE
  """sonarPay"""
  SONARPAY
  """sonarPay Canada"""
  SONARPAY_CANADA
}

"""Defines the required credentials for a credit card provider."""
enum CreditCardProviderCredential {
  """IPpay terminal ID"""
  IPPAY_TERMINALID
  """Stripe secret key"""
  STRIPE_SECRET_KEY
  """Bluepay account ID."""
  BLUEPAY_ACCOUNT_ID
  """Bluepay secret key."""
  BLUEPAY_SECRET_KEY
  """Moneris store ID."""
  MONERIS_CA_STORE_ID
  """Moneris API token."""
  MONERIS_CA_API_TOKEN
  """Authorize.net API login ID."""
  AUTHORIZE_API_LOGIN_ID
  """Authorize.net transaction key."""
  AUTHORIZE_TRANSACTION_KEY
  """Authorize.net validation mode."""
  AUTHORIZE_VALIDATION_MODE
  """Bambora merchant ID."""
  BAMBORA_MERCHANT_ID
  """Bambora payment profile API key."""
  BAMBORA_PAYMENT_PROFILE_API_KEY
  """Bambora transaction API key."""
  BAMBORA_TRANSACTION_API_KEY
  """CardConnect username."""
  CARDCONNECT_USERNAME
  """CardConnect password."""
  CARDCONNECT_PASSWORD
  """CardConnect merchant ID."""
  CARDCONNECT_MERCHANT_ID
  """ProPay biller account ID."""
  PROPAY_BILLER_ACCOUNT_ID
  """ProPay auth token."""
  PROPAY_AUTH_TOKEN
  """PayGate ID."""
  PAYGATE_ID
  """PayGate PayHost password."""
  PAYGATE_PAYHOST_PASSWORD
  """sonarPay Merchant ID"""
  SONARPAY_MERCHANT_ID
}

"""The type of `CreditCard`."""
enum CreditCardType {
  """Visa Electron"""
  VISAELECTRON
  """Maestro"""
  MAESTRO
  """Forbrugsforeningen"""
  FORBRUGSFORENINGEN
  """Dankort"""
  DANKORT
  """Visa"""
  VISA
  """MasterCard"""
  MASTERCARD
  """American Express"""
  AMEX
  """Diner's Club"""
  DINERSCLUB
  """Discover"""
  DISCOVER
  """Union Pay"""
  UNIONPAY
  """JCB"""
  JCB
}
```
