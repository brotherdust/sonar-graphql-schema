```graphql
"""A payment."""
type Payment implements CreditableInterface & DisbursableInterface & LoggableInterface & AccessloggableInterface {
  """The ID of the entity."""
  id: Int64Bit!
  """
  An ID that uniquely identifies this entity across the whole Sonar system.
  """
  sonar_unique_id: ID!
  """The date and time this entity was created."""
  created_at: Datetime!
  """The last date and time this entity was modified."""
  updated_at: Datetime!
  """
  A string that shows the version of this entity. It will be incremented whenever the entity is modified.
  """
  _version: String!
  """The ID of an Account."""
  account_id: Int64Bit!
  """The amount of the payment, in the smallest currency value."""
  amount: Int!
  """The amount remaining that can be used."""
  amount_remaining: Int!
  """The ID of a BankAccount."""
  bank_account_id: Int64Bit
  """The ID of the company that this entity operates under."""
  company_id: Int64Bit!
  """A token sent to the payment provider during payment creation."""
  creation_token: String
  """The ID of a CreditCard."""
  credit_card_id: Int64Bit
  """The deposit slip ID."""
  deposit_slip_id: Int64Bit
  """A description of the payment, used for internal reference."""
  description: String
  """The fee for this transaction."""
  fee: Int
  """The fee for this transaction in fractional cents"""
  fractional_fee: Int
  """
  The entire response back from the company that processed the transaction. Not typically human readable.
  """
  full_processor_response: String
  """Whether or not this was an autopay payment."""
  is_autopay: Boolean
  """Whether or not this payment passed the 3DS security check."""
  passed_3ds_check: Boolean
  """Whether or not this payment passed the AVS security check."""
  passed_avs_check: Boolean
  """Whether or not this payment passed the CVV security check."""
  passed_cvv_check: Boolean
  """The date and time the payment was made."""
  payment_datetime: Datetime!
  """The unique tracking ID for this payment."""
  payment_tracker_id: String
  """The type of payment (e.g. cash, credit card.)"""
  payment_type: PaymentType!
  """
  The message returned back from the company that processed the transaction.
  """
  processor_message: String
  """The status of the payment provided by the payment processor."""
  processor_status: String
  """
  A payment reference like a check number, or wire transfer confirmation number.
  """
  reference: String
  """The status."""
  status: PaymentStatus
  """Whether or not this was successful."""
  successful: Boolean!
  """The transaction ID from the credit card provider."""
  transaction_id: String
  """The ID of a User."""
  user_id: Int64Bit
  """A credit card."""
  credit_card(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
    sonar_unique_id: ID
    """The date and time this entity was created."""
    created_at: Datetime
    """The last date and time this entity was modified."""
    updated_at: Datetime
    """
    A string that shows the version of this entity. It will be incremented whenever the entity is modified.
    """
    _version: String
    """The ID of an Account."""
    account_id: Int64Bit
    """Whether or not this payment method is enabled for automatic payments."""
    auto: Boolean
    """The type of payment made by the card (e.g. Credit, Debit, Prepaid)."""
    card_payment_type: CardPaymentType
    """The ID of a CreditCardProcessor."""
    credit_card_processor_id: Int64Bit
    """The type of a credit card (e.g. Visa, Mastercard.)"""
    credit_card_type: CreditCardType
    """The profile ID provided by a credit card processing service."""
    customer_profile_id: String
    """The month the credit card expires."""
    expiration_month: Int
    """The year the credit card expires."""
    expiration_year: Int
    """A partial credit card number that can be used for identification."""
    masked_number: String
    """The name on the credit card."""
    name_on_card: String
    """
    The tokenized value that represents a credit card, provided by a credit card processing service.
    """
    token: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CreditCard
  """A bank account."""
  bank_account(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
    sonar_unique_id: ID
    """The date and time this entity was created."""
    created_at: Datetime
    """The last date and time this entity was modified."""
    updated_at: Datetime
    """
    A string that shows the version of this entity. It will be incremented whenever the entity is modified.
    """
    _version: String
    """The ID of an Account."""
    account_id: Int64Bit
    """Whether or not this payment method is enabled for automatic payments."""
    auto: Boolean
    """The ID of a BankProcessor."""
    bank_account_processor_id: Int64Bit
    """The type of bank account this is."""
    bank_account_type: BankAccountType
    """The profile ID provided by a credit card processing service."""
    customer_profile_id: String
    """A partial account number that can be used for identification."""
    masked_account_number: String
    """The name on the account."""
    name_on_account: String
    """The bank routing number."""
    routing_number: String
    """
    The tokenized value that represents a credit card, provided by a credit card processing service.
    """
    token: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): BankAccount
  """A customer account."""
  account(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
    sonar_unique_id: ID
    """The date and time this entity was created."""
    created_at: Datetime
    """The last date and time this entity was modified."""
    updated_at: Datetime
    """
    A string that shows the version of this entity. It will be incremented whenever the entity is modified.
    """
    _version: String
    """The ID of an AccountStatus."""
    account_status_id: Int64Bit
    """The ID of an AccountType."""
    account_type_id: Int64Bit
    """The date an account was first activated."""
    activation_date: Date
    """The time an account was first activated."""
    activation_time: Time
    """The date and time this entity was archived."""
    archived_at: Datetime
    """The ID of the `User` that archived this entity."""
    archived_by_user_id: Int64Bit
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """
    The percentage of the data usage cap that this account has consumed this
    month, taking into account any data usage top offs.
    """
    data_usage_percentage: Int
    """A geo-point."""
    geopoint: Geopoint
    """Whether or not this account is delinquent."""
    is_delinquent: Boolean
    """
    Whether or not the Account meets the eligibility criteria for archiving.
    """
    is_eligible_for_archive: Boolean
    """A descriptive name."""
    name: String
    """
    The next date this service will bill. If this is null, it will bill on the next account billing date.
    """
    next_bill_date: Date
    """
    The next recurring charge amount for an account. This is the sum of data,
    expiring, recurring, and voice services of an account for this billing
    cycle, including tax.
    """
    next_recurring_charge_amount: Int
    """The ID of the `Account` that is this `Account`s master."""
    parent_account_id: Int64Bit
    """Whether or not to include archived entities in the results."""
    include_archived: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): Account
  """A company you do business as."""
  company(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
    sonar_unique_id: ID
    """The date and time this entity was created."""
    created_at: Datetime
    """The last date and time this entity was modified."""
    updated_at: Datetime
    """
    A string that shows the version of this entity. It will be incremented whenever the entity is modified.
    """
    _version: String
    """
    The daily end time of the period during which billing communication e.g. new
    invoices, delinquency, etc. will not be sent.
    """
    billing_communication_delay_end_local_time: Time
    """
    The daily start time of the period during which billing communication e.g.
    new invoices, delinquency, etc. will not be sent.
    """
    billing_communication_delay_start_local_time: Time
    """On an enabled remittance slip, who should checks be made payable to?"""
    checks_payable_to: String
    """A two character country code."""
    country: Country
    """The URL to your customer portal."""
    customer_portal_url: URL
    """Whether or not this entity is a default entry."""
    default: Boolean
    """Whether or not this is enabled."""
    enabled: Boolean
    """The ISP type of this `Company`."""
    isp_type: IspType
    """A descriptive name."""
    name: String
    """A telephone number."""
    phone_number: Numeric
    """The primary color to use in Sonar."""
    primary_color: HtmlHexColor
    """The secondary color to use in Sonar."""
    secondary_color: HtmlHexColor
    """Whether or not to include a detachable remittance slip on the invoice."""
    show_remittance_slip: Boolean
    """
    A tax identification number. Should only be entered if you are required to
    share some type of tax identification information with your customers.
    """
    tax_identification: String
    """The address of the company website."""
    website_address: URL
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): Company
  """A deposit slip."""
  deposit_slip(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
    sonar_unique_id: ID
    """The date and time this entity was created."""
    created_at: Datetime
    """The last date and time this entity was modified."""
    updated_at: Datetime
    """
    A string that shows the version of this entity. It will be incremented whenever the entity is modified.
    """
    _version: String
    """The bank account name/number"""
    bank_account_line: String
    """A date"""
    date: Date
    """The memo."""
    memo: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DepositSlip
  """The application of a `Discount` or `Payment` against an `Invoice`."""
  credits(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
    sonar_unique_id: ID
    """The date and time this entity was created."""
    created_at: Datetime
    """The last date and time this entity was modified."""
    updated_at: Datetime
    """
    A string that shows the version of this entity. It will be incremented whenever the entity is modified.
    """
    _version: String
    """The ID of an Account."""
    account_id: Int64Bit
    """The amount, in the smallest currency value (e.g. cents, pence, pesos.)"""
    amount: Int
    """The ID the transaction that created this credit."""
    creditable_id: Int64Bit
    """The type of transaction that created this credit."""
    creditable_type: CreditableType
    """The ID of an `Invoice`."""
    invoice_id: Int64Bit
    """Whether or not this entity has been voided."""
    void: Boolean
    """When this was voided."""
    voided_at: Datetime
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CreditConnection!
  """A disbursement detail."""
  disbursement_details(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
    sonar_unique_id: ID
    """The date and time this entity was created."""
    created_at: Datetime
    """The last date and time this entity was modified."""
    updated_at: Datetime
    """
    A string that shows the version of this entity. It will be incremented whenever the entity is modified.
    """
    _version: String
    """The amount, in the smallest currency value (e.g. cents, pence, pesos.)"""
    amount: Int
    """The amount used."""
    amount_used: Int
    """The id of the entity that the disbusement applies to."""
    disbursable_id: Int64Bit
    """The type of entity that the disbursement applies to."""
    disbursable_type: DisbursableType
    """The ID of a `Disbursement`."""
    disbursement_id: Int64Bit
    """The event associated with the disbursement detail record."""
    event: DisbursementDetailEvent
    """The payment processor's external ID."""
    external_id: String
    """The amount for this fee."""
    fee_amount: Int
    """The unit of measurement for this fee's amount."""
    fee_unit: SonarPayUnit
    """The fractional portion of the amount."""
    fractional_amount: Int
    """The fractional portion of the amount used."""
    fractional_amount_used: Int
    """
    The portion of the interchange fee that is a fixed amount. This is stored as
    the smallest currency value (e.g. cents, pence, pesos.).
    """
    interchange_flat_rate_fee: Int
    """
    The portion of the interchange fee that is based on a percentage of the
    transaction amount. This is stored as basis points (e.g. 260 represents 2.6%).
    """
    interchange_percent_fee: Int
    """The name of the interchange fee type."""
    interchange_type: String
    """Whether or not this record is a fee."""
    is_fee: Boolean
    """The transaction ID from the credit card provider."""
    transaction_id: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DisbursementDetailConnection!
  """A log entry."""
  logs(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
    sonar_unique_id: ID
    """The date and time this entity was created."""
    created_at: Datetime
    """The last date and time this entity was modified."""
    updated_at: Datetime
    """
    A string that shows the version of this entity. It will be incremented whenever the entity is modified.
    """
    _version: String
    """Current data."""
    current: Text
    """
    Whether or not this log was transferred from a Sonar v1 instance. If so, the
    formatting will not match current version logs.
    """
    legacy: Boolean
    """
    A title which is only populated on logs that were imported from Sonar v1.
    """
    legacy_title: String
    """The severity level."""
    level: LogLevel
    """The ID of the entity that this log is attached to."""
    loggable_id: Int64Bit
    """The type of entity that this log is attached to."""
    loggable_type: String
    """The entity ID that triggered the log."""
    logged_entity_id: Int64Bit
    """The entity that triggered the log."""
    logged_entity_type: String
    """The message."""
    message: Text
    """Previous data."""
    previous: Text
    """Data from objects related to this change."""
    relation_data: Text
    """The type."""
    type: LogType
    """The ID of a User."""
    user_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): LogConnection!
  """An access log history on an entity."""
  access_logs(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
    sonar_unique_id: ID
    """The date and time this entity was created."""
    created_at: Datetime
    """The last date and time this entity was modified."""
    updated_at: Datetime
    """
    A string that shows the version of this entity. It will be incremented whenever the entity is modified.
    """
    _version: String
    """The date and time that this entity was accessed."""
    access_datetime: Datetime
    """The ID of the entity that this access log belongs to."""
    accessloggable_id: Int64Bit
    """The entity that this access log belongs to."""
    accessloggable_type: String
    """The ID of the entity that this access log belongs to."""
    entity_id: Int64Bit
    """The entity that this access log belongs to."""
    entity_name: String
    """The ID of the user that accessed this entity."""
    user_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AccessLogConnection!
  """A record a `Payment` reversal."""
  reversed_payments(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
    sonar_unique_id: ID
    """The date and time this entity was created."""
    created_at: Datetime
    """The last date and time this entity was modified."""
    updated_at: Datetime
    """
    A string that shows the version of this entity. It will be incremented whenever the entity is modified.
    """
    _version: String
    """The amount, in the smallest currency value (e.g. cents, pence, pesos.)"""
    amount: Int
    """A human readable description."""
    description: String
    """The ID of a `Payment`."""
    payment_id: Int64Bit
    """The ID of a User."""
    user_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ReversedPaymentConnection!
  """A record of a refund applied to a `Payment`."""
  refunded_payments(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
    sonar_unique_id: ID
    """The date and time this entity was created."""
    created_at: Datetime
    """The last date and time this entity was modified."""
    updated_at: Datetime
    """
    A string that shows the version of this entity. It will be incremented whenever the entity is modified.
    """
    _version: String
    """The amount, in the smallest currency value (e.g. cents, pence, pesos.)"""
    amount: Int
    """A human readable description."""
    description: String
    """The ID of a `Payment`."""
    payment_id: Int64Bit
    """The unique tracking ID for this payment."""
    payment_tracker_id: String
    """
    The response from the payment processor when this payment was submitted.
    """
    processor_response_message: String
    """The transaction ID from the credit card provider."""
    transaction_id: String
    """The ID of a User."""
    user_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): RefundedPaymentConnection!
  """A record of a `Payment` that was voided."""
  voided_payments(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
    sonar_unique_id: ID
    """The date and time this entity was created."""
    created_at: Datetime
    """The last date and time this entity was modified."""
    updated_at: Datetime
    """
    A string that shows the version of this entity. It will be incremented whenever the entity is modified.
    """
    _version: String
    """The amount, in the smallest currency value (e.g. cents, pence, pesos.)"""
    amount: Int
    """A human readable description."""
    description: String
    """The ID of a `Payment`."""
    payment_id: Int64Bit
    """The unique tracking ID for this payment."""
    payment_tracker_id: String
    """
    The response from the payment processor when this payment was submitted.
    """
    processor_response_message: String
    """The transaction ID from the credit card provider."""
    transaction_id: String
    """The ID of a User."""
    user_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): VoidedPaymentConnection!
  """A dispute."""
  disputes(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
    sonar_unique_id: ID
    """The date and time this entity was created."""
    created_at: Datetime
    """The last date and time this entity was modified."""
    updated_at: Datetime
    """
    A string that shows the version of this entity. It will be incremented whenever the entity is modified.
    """
    _version: String
    """The amount, in the smallest currency value (e.g. cents, pence, pesos.)"""
    amount: Int
    """The dispute's case ID."""
    case_id: String
    """The current dispute cycle."""
    cycle: String
    """The date the dispute was issued."""
    dispute_date: Date
    """The payment processor's external ID."""
    external_id: String
    """The ID of a `Payment`."""
    payment_id: Int64Bit
    """The reason."""
    reason: Text
    """The date the dispute must be replied to by."""
    reply_by_date: Date
    """The status."""
    status: DisputeStatus
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DisputeConnection!
}

"""The connection wrapper around the `PaymentConnection` type."""
type PaymentConnection {
  """A list of the entities provided by this connection."""
  entities: [Payment]!
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

"""A payment."""
type PaymentResult {
  """The value."""
  value: String!
}

"""Payment Result Connection"""
type PaymentResultConnection {
  """A list of the entities provided by this connection."""
  entities: [PaymentResult]!
  """
  An object providing information about the page of results being displayed, as
  well as the total amount of pages/records available.
  """
  page_info: PageInfo!
}
```
