```graphql
"""
Default billing settings that are applied to some accounts on creation.
"""
type BillingDefault implements LoggableInterface & AccessloggableInterface {
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
  """The ID of an AccountType."""
  account_type_id: Int64Bit
  """
  Whether or not to aggregate invoice taxes instead of printing with each charge.
  """
  aggregate_invoice_taxes: Boolean!
  """Whether or not to aggregate linked debits on Anchor invoices."""
  aggregate_linked_debits: Boolean!
  """The ID of a BillingDefault acting as an Anchor default."""
  anchor_default_id: Int64Bit
  """
  Determines if delinquency settings on an Anchor default is applied only to the
  Anchor account or the Linked accounts as well.
  """
  anchor_delinquency_logic: AnchorDelinquencyLogic
  """
  If `invoice_day` is not null, this allows you to select whether
  `auto_pay_days` is calculated from the billing day, or the invoice day.
  """
  auto_pay_day: BillingParameterDayOption!
  """
  The number of days after `auto_pay_day` that autopay runs for an invoice.
  """
  auto_pay_days: Int!
  """The day that billing runs."""
  bill_day: Int
  """
  Whether the account bill and invoice day are fixed, the account activation day
  is used as bill day, or the account activation day is used as the invoice day.
  """
  bill_day_mode: BillDayModeOption!
  """The type of bill this account receives."""
  bill_mode: BillMode!
  """
  If `switch_status_after_delinquency` is `true`, then this is the number of
  days of delinquency to allow before the status switch.
  """
  days_of_delinquency_for_status_switch: Int
  """
  If this is `true`, then this is the default billing default that is used, if
  there is no more specific billing default option for an account.
  """
  default: Boolean!
  """
  Determines if the billing parameters apply by account type or for anchor / linked types.
  """
  default_for: BillingDefaultFor!
  """
  If `switch_status_after_delinquency` is true, this is the account status that
  the account will be moved into after `days_of_delinquency_for_status_switch`
  days of delinquency.
  """
  delinquency_account_status_id: Int64Bit
  """
  If `switch_status_after_delinquency` is `true`, then this is the status the
  account will be moved back into if delinquency is cleared while the account is
  set to the `delinquency_account_status_id` account status.
  """
  delinquency_removal_account_status_id: Int64Bit
  """The number of days after the invoice date that it is due."""
  due_days: Int!
  """
  If `invoice_day` is not null, this allows you to select whether `due_days` is
  calculated from the billing day, or the invoice day.
  """
  due_days_day: BillingParameterDayOption!
  """
  Whether or not to use a fixed bill day, versus anniversary day billing. Use `bill_day_mode` for further customization.
  """
  fixed_bill_day: Boolean
  """
  The number of days after the invoice due date that the invoice is marked delinquent.
  """
  grace_days: Int!
  """
  The day that automatic billing invoices are generated for. If this is `null`, then `bill_day` is used.
  """
  invoice_day: Int
  """
  Whether or not this account participates in the federal Lifeline program.
  """
  lifeline: Boolean!
  """The number of months to bill at a time."""
  months_to_bill: Int!
  """A descriptive name."""
  name: String!
  """Whether this account receives a printed invoice."""
  print_invoice: Boolean!
  """
  Whether or not this account should be moved into another status after being delinquent for a preset period.
  """
  switch_status_after_delinquency: Boolean!
  """Whether or not this account is tax exempt."""
  tax_exempt: Boolean!
  """
  The status that an `Account` is moved into after a certain length of delinquency.
  """
  delinquency_account_status(
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
    """Whether or not this status activates the account."""
    activates_account: Boolean
    """Color."""
    color: HtmlHexColor
    """An icon."""
    icon: Icon
    """A descriptive name."""
    name: String
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
  ): AccountStatus
  """
  The `AccountStatus` an account is moved back into after no longer being
  delinquent, if it is currently in the delinquency account status defined on
  the `AccountBillingParameter`.
  """
  delinquency_removal_account_status(
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
    """Whether or not this status activates the account."""
    activates_account: Boolean
    """Color."""
    color: HtmlHexColor
    """An icon."""
    icon: Icon
    """A descriptive name."""
    name: String
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
  ): AccountStatus
  """The account type."""
  account_type(
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
    """Color."""
    color: HtmlHexColor
    """An icon."""
    icon: Icon
    """The ID of an `InvoiceMessage`."""
    invoice_message_id: Int64Bit
    """A descriptive name."""
    name: String
    """The type."""
    type: AccountTypeEnum
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
  ): AccountType
  """
  Default billing settings that are applied to some accounts on creation.
  """
  billing_default(
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
    """The ID of an AccountType."""
    account_type_id: Int64Bit
    """
    Whether or not to aggregate invoice taxes instead of printing with each charge.
    """
    aggregate_invoice_taxes: Boolean
    """Whether or not to aggregate linked debits on Anchor invoices."""
    aggregate_linked_debits: Boolean
    """The ID of a BillingDefault acting as an Anchor default."""
    anchor_default_id: Int64Bit
    """
    Determines if delinquency settings on an Anchor default is applied only to
    the Anchor account or the Linked accounts as well.
    """
    anchor_delinquency_logic: AnchorDelinquencyLogic
    """
    If `invoice_day` is not null, this allows you to select whether
    `auto_pay_days` is calculated from the billing day, or the invoice day.
    """
    auto_pay_day: BillingParameterDayOption
    """
    The number of days after `auto_pay_day` that autopay runs for an invoice.
    """
    auto_pay_days: Int
    """The day that billing runs."""
    bill_day: Int
    """
    Whether the account bill and invoice day are fixed, the account activation
    day is used as bill day, or the account activation day is used as the invoice day.
    """
    bill_day_mode: BillDayModeOption
    """The type of bill this account receives."""
    bill_mode: BillMode
    """
    If `switch_status_after_delinquency` is `true`, then this is the number of
    days of delinquency to allow before the status switch.
    """
    days_of_delinquency_for_status_switch: Int
    """
    If this is `true`, then this is the default billing default that is used, if
    there is no more specific billing default option for an account.
    """
    default: Boolean
    """
    Determines if the billing parameters apply by account type or for anchor / linked types.
    """
    default_for: BillingDefaultFor
    """
    If `switch_status_after_delinquency` is true, this is the account status
    that the account will be moved into after
    `days_of_delinquency_for_status_switch` days of delinquency.
    """
    delinquency_account_status_id: Int64Bit
    """
    If `switch_status_after_delinquency` is `true`, then this is the status the
    account will be moved back into if delinquency is cleared while the account
    is set to the `delinquency_account_status_id` account status.
    """
    delinquency_removal_account_status_id: Int64Bit
    """The number of days after the invoice date that it is due."""
    due_days: Int
    """
    If `invoice_day` is not null, this allows you to select whether `due_days`
    is calculated from the billing day, or the invoice day.
    """
    due_days_day: BillingParameterDayOption
    """
    Whether or not to use a fixed bill day, versus anniversary day billing. Use `bill_day_mode` for further customization.
    """
    fixed_bill_day: Boolean
    """
    The number of days after the invoice due date that the invoice is marked delinquent.
    """
    grace_days: Int
    """
    The day that automatic billing invoices are generated for. If this is `null`, then `bill_day` is used.
    """
    invoice_day: Int
    """
    Whether or not this account participates in the federal Lifeline program.
    """
    lifeline: Boolean
    """The number of months to bill at a time."""
    months_to_bill: Int
    """A descriptive name."""
    name: String
    """Whether this account receives a printed invoice."""
    print_invoice: Boolean
    """
    Whether or not this account should be moved into another status after being delinquent for a preset period.
    """
    switch_status_after_delinquency: Boolean
    """Whether or not this account is tax exempt."""
    tax_exempt: Boolean
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
  ): BillingDefault
  """A geographical address."""
  addresses(
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
    """Address status ID."""
    address_status_id: Int64Bit
    """The ID of the entity that owns this address."""
    addressable_id: Int64Bit
    """The type of entity that owns this address."""
    addressable_type: AddressableType
    """The address ID for the Anchor address"""
    anchor_address_id: Int64Bit
    """The attainable download speed in kilobits per second."""
    attainable_download_speed: Int
    """The attainable upload speed in kilobits per second."""
    attainable_upload_speed: Int
    """Avalara PCode."""
    avalara_pcode: String
    """The ID of a BillingDefault."""
    billing_default_id: Int64Bit
    """The year used for calculating fips and census tract information."""
    census_year: Int
    """A city."""
    city: String
    """A two character country code."""
    country: Country
    """A US county. Only used for US addresses."""
    county: UsCounty
    """
    Only used in the USA, this is the census tract information used for calculating things like FCC Form 477.
    """
    fips: String
    """Identifies the source used to obtain the FIPS code"""
    fips_source: FipsSource
    """Whether or not this address is an anchor"""
    is_anchor: Boolean
    """A decimal latitude."""
    latitude: Latitude
    """Address line 1."""
    line1: String
    """Address line 2."""
    line2: String
    """A decimal longitude."""
    longitude: Longitude
    """
    Whether or not the address is serviceable, and can be used for new accounts.
    """
    serviceable: Boolean
    """A state, province, or other country subdivision."""
    subdivision: Subdivision
    """The timezone you want times in the system displayed in."""
    timezone: Timezone
    """The type."""
    type: AddressType
    """A ZIP or postal code."""
    zip: String
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
  ): AddressConnection!
  """Parameters that define the billing settings for an `Account`."""
  account_billing_parameters(
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
    """
    Whether or not to aggregate invoice taxes instead of printing with each charge.
    """
    aggregate_invoice_taxes: Boolean
    """Whether or not to aggregate linked debits on Anchor invoices."""
    aggregate_linked_debits: Boolean
    """
    Determines if delinquency settings on an Anchor default is applied only to
    the Anchor account or the Linked accounts as well.
    """
    anchor_delinquency_logic: AnchorDelinquencyLogic
    """
    If `invoice_day` is not null, this allows you to select whether
    `auto_pay_days` is calculated from the billing day, or the invoice day.
    """
    auto_pay_day: BillingParameterDayOption
    """
    The number of days after `auto_pay_day` that autopay runs for an invoice.
    """
    auto_pay_days: Int
    """The day that billing runs."""
    bill_day: Int
    """
    Whether the account bill and invoice day are fixed, the account activation
    day is used as bill day, or the account activation day is used as the invoice day.
    """
    bill_day_mode: BillDayModeOption
    """The type of bill this account receives."""
    bill_mode: BillMode
    """The ID of a BillingDefault."""
    billing_default_id: Int64Bit
    """
    If `switch_status_after_delinquency` is `true`, then this is the number of
    days of delinquency to allow before the status switch.
    """
    days_of_delinquency_for_status_switch: Int
    """
    Determines if the billing parameters apply by account type or for anchor / linked types.
    """
    default_for: BillingDefaultFor
    """
    If `switch_status_after_delinquency` is true, this is the account status
    that the account will be moved into after
    `days_of_delinquency_for_status_switch` days of delinquency.
    """
    delinquency_account_status_id: Int64Bit
    """
    If `switch_status_after_delinquency` is `true`, then this is the status the
    account will be moved back into if delinquency is cleared while the account
    is set to the `delinquency_account_status_id` account status.
    """
    delinquency_removal_account_status_id: Int64Bit
    """The number of days after the invoice date that it is due."""
    due_days: Int
    """
    If `invoice_day` is not null, this allows you to select whether `due_days`
    is calculated from the billing day, or the invoice day.
    """
    due_days_day: BillingParameterDayOption
    """
    The number of days after the invoice due date that the invoice is marked delinquent.
    """
    grace_days: Int
    """
    A temporary override that stops the account becoming delinquent until this date.
    """
    grace_until: Date
    """
    The day that automatic billing invoices are generated for. If this is `null`, then `bill_day` is used.
    """
    invoice_day: Int
    """
    Whether or not this account participates in the federal Lifeline program.
    """
    lifeline: Boolean
    """The number of months to bill at a time."""
    months_to_bill: Int
    """Whether this account receives a printed invoice."""
    print_invoice: Boolean
    """
    Whether or not this account should be moved into another status after being delinquent for a preset period.
    """
    switch_status_after_delinquency: Boolean
    """Whether or not this account is tax exempt."""
    tax_exempt: Boolean
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
  ): AccountBillingParameterConnection!
  """The service items and overrides for linked billing defaults."""
  billing_services(
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
    The amount of the service that will be invoiced to the anchor account.  Cannot exceed price provided.
    """
    anchor_subsidy: Int
    """The ID of a BillingDefault."""
    billing_default_id: Int64Bit
    """
    Overriding the service name will alter the service name printed on an invoice.
    """
    name_override: String
    """The price per unit of this item."""
    price: Int
    """The ID of a Service."""
    service_id: Int64Bit
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
  ): BillingServiceConnection!
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
}

"""The connection wrapper around the `BillingDefaultConnection` type."""
type BillingDefaultConnection {
  """A list of the entities provided by this connection."""
  entities: [BillingDefault]!
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

"""The service items and overrides for linked billing defaults."""
type BillingService implements LoggableInterface & AccessloggableInterface {
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
  """
  The amount of the service that will be invoiced to the anchor account.  Cannot exceed price provided.
  """
  anchor_subsidy: Int
  """The ID of a BillingDefault."""
  billing_default_id: Int64Bit!
  """
  Overriding the service name will alter the service name printed on an invoice.
  """
  name_override: String
  """The price per unit of this item."""
  price: Int
  """The ID of a Service."""
  service_id: Int64Bit!
  """
  Default billing settings that are applied to some accounts on creation.
  """
  billing_default(
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
    """The ID of an AccountType."""
    account_type_id: Int64Bit
    """
    Whether or not to aggregate invoice taxes instead of printing with each charge.
    """
    aggregate_invoice_taxes: Boolean
    """Whether or not to aggregate linked debits on Anchor invoices."""
    aggregate_linked_debits: Boolean
    """The ID of a BillingDefault acting as an Anchor default."""
    anchor_default_id: Int64Bit
    """
    Determines if delinquency settings on an Anchor default is applied only to
    the Anchor account or the Linked accounts as well.
    """
    anchor_delinquency_logic: AnchorDelinquencyLogic
    """
    If `invoice_day` is not null, this allows you to select whether
    `auto_pay_days` is calculated from the billing day, or the invoice day.
    """
    auto_pay_day: BillingParameterDayOption
    """
    The number of days after `auto_pay_day` that autopay runs for an invoice.
    """
    auto_pay_days: Int
    """The day that billing runs."""
    bill_day: Int
    """
    Whether the account bill and invoice day are fixed, the account activation
    day is used as bill day, or the account activation day is used as the invoice day.
    """
    bill_day_mode: BillDayModeOption
    """The type of bill this account receives."""
    bill_mode: BillMode
    """
    If `switch_status_after_delinquency` is `true`, then this is the number of
    days of delinquency to allow before the status switch.
    """
    days_of_delinquency_for_status_switch: Int
    """
    If this is `true`, then this is the default billing default that is used, if
    there is no more specific billing default option for an account.
    """
    default: Boolean
    """
    Determines if the billing parameters apply by account type or for anchor / linked types.
    """
    default_for: BillingDefaultFor
    """
    If `switch_status_after_delinquency` is true, this is the account status
    that the account will be moved into after
    `days_of_delinquency_for_status_switch` days of delinquency.
    """
    delinquency_account_status_id: Int64Bit
    """
    If `switch_status_after_delinquency` is `true`, then this is the status the
    account will be moved back into if delinquency is cleared while the account
    is set to the `delinquency_account_status_id` account status.
    """
    delinquency_removal_account_status_id: Int64Bit
    """The number of days after the invoice date that it is due."""
    due_days: Int
    """
    If `invoice_day` is not null, this allows you to select whether `due_days`
    is calculated from the billing day, or the invoice day.
    """
    due_days_day: BillingParameterDayOption
    """
    Whether or not to use a fixed bill day, versus anniversary day billing. Use `bill_day_mode` for further customization.
    """
    fixed_bill_day: Boolean
    """
    The number of days after the invoice due date that the invoice is marked delinquent.
    """
    grace_days: Int
    """
    The day that automatic billing invoices are generated for. If this is `null`, then `bill_day` is used.
    """
    invoice_day: Int
    """
    Whether or not this account participates in the federal Lifeline program.
    """
    lifeline: Boolean
    """The number of months to bill at a time."""
    months_to_bill: Int
    """A descriptive name."""
    name: String
    """Whether this account receives a printed invoice."""
    print_invoice: Boolean
    """
    Whether or not this account should be moved into another status after being delinquent for a preset period.
    """
    switch_status_after_delinquency: Boolean
    """Whether or not this account is tax exempt."""
    tax_exempt: Boolean
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
  ): BillingDefault
  """A service."""
  service(
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
    """How this is applied."""
    application: ServiceApplication
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """
    If the amount for this service is zero, it will still display on invoices.
    """
    display_if_zero: Boolean
    """Whether or not this is enabled."""
    enabled: Boolean
    """The ID of a GeneralLedgerCode."""
    general_ledger_code_id: Int64Bit
    """A descriptive name."""
    name: String
    """The ID of a tax definition on a reversed transaction."""
    reverse_tax_definition_id: Int64Bit
    """The ID of a tax definition on a transaction."""
    tax_definition_id: Int64Bit
    """The type."""
    type: ServiceType
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
  ): Service
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
}

"""The connection wrapper around the `BillingServiceConnection` type."""
type BillingServiceConnection {
  """A list of the entities provided by this connection."""
  entities: [BillingService]!
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

"""Billing configuration settings."""
type BillingSetting implements LoggableInterface & AccessloggableInterface {
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
  """How often the accounting period automatically closes."""
  accounting_period_auto_close: AccountingPeriodCloseOption!
  """The date that the accounting period was closed."""
  accounting_period_close_date: Date
  """Always round taxes up."""
  always_round_taxes_up: Boolean!
  """Whether or not to apply a late fee to past due invoices."""
  apply_late_fees: Boolean!
  """Whether late fees should be applied to child invoices."""
  apply_late_fees_to_child_invoices: Boolean!
  """The number of times to attempt a bank account automatic payment."""
  autopay_bank_account_attempts: Int!
  """
  The number of days between retries for bank account automatic payments.
  """
  autopay_bank_account_retry_interval_in_days: Int!
  """The number of times to attempt a credit card automatic payment."""
  autopay_credit_card_attempts: Int!
  """The number of days between retries for credit card automatic payments."""
  autopay_credit_card_retry_interval_in_days: Int!
  """Autopay the account disconnect invoice."""
  autopay_disconnect_invoice: Boolean
  """The number of days between invoice date and the Autopay date."""
  autopay_disconnect_invoice_days: Int
  """Autopay the initial invoice."""
  autopay_initial_invoice: Boolean
  """The number of days between invoice date and the Autopay date."""
  autopay_initial_invoice_days: Int
  """
  Whether the automatic payment process should just run the invoice amount, or the entire amount due on the account.
  """
  autopay_runs_entire_amount_due: Boolean!
  """Whether or not the daily billing process is enabled."""
  daily_billing: Boolean!
  """
  The number of days after the due date on a delinquent invoice for a late fee to be applied.
  """
  days_after_invoice_due_for_late_fee_application: Int
  """Whether or not to delete expired credit cards from Sonar."""
  delete_expired_credit_cards: Boolean!
  """Friday."""
  delinquency_check_day_friday: Boolean!
  """Monday."""
  delinquency_check_day_monday: Boolean!
  """Saturday."""
  delinquency_check_day_saturday: Boolean!
  """Sunday."""
  delinquency_check_day_sunday: Boolean!
  """Thursday."""
  delinquency_check_day_thursday: Boolean!
  """Tuesday."""
  delinquency_check_day_tuesday: Boolean!
  """Wednesday."""
  delinquency_check_day_wednesday: Boolean!
  """The `AccountStatus` for disconnected accounts."""
  disconnect_account_status_id: Int64Bit!
  """Whether to exclude inactive accounts from late fee application."""
  exclude_inactive_accounts_from_late_fees: Boolean!
  """
  Generate an invoice on an account when it is first activated, if there are any uninvoiced debits.
  """
  generate_invoice_on_initial_activation: Boolean!
  """Whether or not to include late fee invoices in printed batches."""
  include_late_fee_invoices_in_printed_batches: Boolean!
  """
  Whether to invoice and email late fees immediately, or add them to the next invoice.
  """
  invoice_and_email_late_fees_immediately: Boolean!
  """
  The minimum amount an invoice must be past due for a late fee to be applied.
  """
  late_fee_minimum_delinquency_amount: Int
  """The mode for late fee application."""
  late_fee_mode: LateFeeMode!
  """
  If late fees are applied as a percentage, the percentage of the past due balance to apply.
  """
  late_fee_percentage: Float
  """The ID of a one time `Service` to use for late fee application."""
  late_fee_service_id: Int64Bit
  """
  The minimum account an invoice must be delinquent for before being flagged delinquent.
  """
  minimum_amount_due_for_delinquency: Int!
  """The smallest bank account payment amount allowed."""
  minimum_bank_account_payment: Int!
  """The smallest credit card payment amount allowed."""
  minimum_credit_card_payment: Int!
  """Printed invoice batch duplex."""
  printed_invoice_batch_duplex: Boolean!
  """
  The service ID of a one time `Service` to charge for accounts with
  `print_invoice` enabled in their `AccountBillingParameter`.
  """
  printed_invoice_fee_service_id: Int64Bit
  """
  Whether or not an account going delinquent or no longer delinquent is prorated by default.
  """
  prorate_account_delinquency_status_change: Boolean
  """
  Whether or not changing the status from an active to inactive status is prorated by default.
  """
  prorate_account_status_change: Boolean!
  """Whether or not changing an account bill day is prorated by default."""
  prorate_billing_day_change: Boolean!
  """Whether or not service quantity changes are prorated by default."""
  prorate_service_quantity: Boolean!
  """Whether or not service addition and removal is prorated by default."""
  prorate_services: Boolean!
  """
  Whether or not to round prorated transactions to the nearest major unit (e.g. to the nearest dollar, euro, pound, etc.)
  """
  round_prorated_amounts: Boolean!
  """The `AccountStatus` for unarchived accounts."""
  unarchive_account_status_id: Int64Bit
  """Use modular invoice templates for all invoices."""
  use_invoice_templates: Boolean!
  """The service used for late fee application."""
  late_fee_service(
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
    """How this is applied."""
    application: ServiceApplication
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """
    If the amount for this service is zero, it will still display on invoices.
    """
    display_if_zero: Boolean
    """Whether or not this is enabled."""
    enabled: Boolean
    """The ID of a GeneralLedgerCode."""
    general_ledger_code_id: Int64Bit
    """A descriptive name."""
    name: String
    """The ID of a tax definition on a reversed transaction."""
    reverse_tax_definition_id: Int64Bit
    """The ID of a tax definition on a transaction."""
    tax_definition_id: Int64Bit
    """The type."""
    type: ServiceType
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
  ): Service
  """The service used for printed invoices."""
  printed_invoice_service(
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
    """How this is applied."""
    application: ServiceApplication
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """
    If the amount for this service is zero, it will still display on invoices.
    """
    display_if_zero: Boolean
    """Whether or not this is enabled."""
    enabled: Boolean
    """The ID of a GeneralLedgerCode."""
    general_ledger_code_id: Int64Bit
    """A descriptive name."""
    name: String
    """The ID of a tax definition on a reversed transaction."""
    reverse_tax_definition_id: Int64Bit
    """The ID of a tax definition on a transaction."""
    tax_definition_id: Int64Bit
    """The type."""
    type: ServiceType
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
  ): Service
  """
  The account status used when moving accounts into the post-delinquency state.
  """
  disconnect_account_status(
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
    """Whether or not this status activates the account."""
    activates_account: Boolean
    """Color."""
    color: HtmlHexColor
    """An icon."""
    icon: Icon
    """A descriptive name."""
    name: String
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
  ): AccountStatus
  """The account status used when unarchiving accounts."""
  unarchive_account_status(
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
    """Whether or not this status activates the account."""
    activates_account: Boolean
    """Color."""
    color: HtmlHexColor
    """An icon."""
    icon: Icon
    """A descriptive name."""
    name: String
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
  ): AccountStatus
  """The account type."""
  account_types(
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
    """Color."""
    color: HtmlHexColor
    """An icon."""
    icon: Icon
    """The ID of an `InvoiceMessage`."""
    invoice_message_id: Int64Bit
    """A descriptive name."""
    name: String
    """The type."""
    type: AccountTypeEnum
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
  ): AccountTypeConnection!
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
}
```
