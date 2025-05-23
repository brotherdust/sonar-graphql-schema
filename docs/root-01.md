```graphql
type Query {
  """All access logs for this entity."""
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
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
  """Account Adtran Mosaic service details."""
  account_adtran_mosaic_service_details(
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
    """The ID of an AccountService."""
    account_service_id: Int64Bit
    """The ID of an Adtran Mosaic setting."""
    adtran_mosaic_setting_id: Int64Bit
    """The name of the Adtran Mosaic downlink inner tag vlan."""
    downlink_inner_tag_vlan: String
    """The name of the Adtran Mosaic downlink interface."""
    downlink_interface_name: String
    """The name of the Adtran Mosaic downlink outer tag vlan."""
    downlink_outer_tag_vlan: String
    """The name of the Adtran Mosaic content provider."""
    uplink_content_provider_name: String
    """The name of the Adtran Mosaic uplink inner tag vlan."""
    uplink_inner_tag_vlan: String
    """The name of the Adtran Mosaic uplink outer tag vlan."""
    uplink_outer_tag_vlan: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AccountAdtranMosaicServiceDetailConnection!
  """Account billing parameters."""
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
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
  """Account Calix Service Details."""
  account_calix_service_details(
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
    """The ID of an AccountService."""
    account_service_id: Int64Bit
    """Calix Inegartion ID."""
    calix_integration_id: Int64Bit
    """Custom JSON."""
    custom_json: String
    """C-VLAN."""
    cvlan: Int
    """Global VLAN."""
    global_vlan: String
    """ONT Port ID."""
    ont_port_id: String
    """Policy Map."""
    policy_map: String
    """Use Custom JSON."""
    use_custom_json: Boolean
    """VLAN."""
    vlan: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AccountCalixServiceDetailConnection!
  """Account events."""
  account_events(
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
    """Current data."""
    current: String
    """An event."""
    event: AccountUpdateEvent
    """The date and time of an event sent from Mandrill"""
    event_datetime: Datetime
    """Previous data."""
    previous: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AccountEventConnection!
  """Account groups."""
  account_groups(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AccountGroupConnection!
  """IP assignments associated with account(s)."""
  account_ip_assignments(
    """The ID of the entity."""
    account_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
  ): AccountIpAssignmentsConnection!
  """Services that have been attached to accounts."""
  account_services(
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
    If this service was prorated when added, this is the date it was prorated from.
    """
    addition_prorate_date: Date
    """The date data usage was last calculated."""
    data_usage_last_calculated_date: Date
    """
    Overriding the service name will alter the service name printed on an invoice.
    """
    name_override: String
    """
    The next date this service will bill. If this is null, it will bill on the next account billing date.
    """
    next_bill_date: Date
    """
    The number of billing cycles that have already been consumed by this
    particular service. This is only used for expiring services. NOTE: Typically
    this is the number of times billed but the value may be modified manually to
    adjust service expiration. See also the the `ExpiringServiceDetail`
    `times_to_run` field.
    """
    number_of_times_billed: Int
    """The ID of a `Package`."""
    package_id: Int64Bit
    """
    The amount that this service price has been overridden to. If this is null, then the service price is used.
    """
    price_override: Int
    """The reason that the price of a service has been overridden."""
    price_override_reason: String
    """The quantity for this service."""
    quantity: Int
    """The ID of a Service."""
    service_id: Int64Bit
    """
    A unique ID that describes this unique instance of a `Package` assignment.
    """
    unique_package_relationship_id: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AccountServiceConnection!
  """Account statuses."""
  account_statuses(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AccountStatusConnection!
  """Account types."""
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
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
  """Details of a voice service attached to an account."""
  account_voice_service_details(
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
    """The ID of an AccountService."""
    account_service_id: Int64Bit
    """
    The amount that this service price has been overridden to. If this is null, then the service price is used.
    """
    price_override: Int
    """The reason that the price of a service has been overridden."""
    price_override_reason: String
    """The quantity for this service."""
    quantity: Int
    """The ID of a voice service configuration parameter."""
    voice_service_generic_parameter_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AccountVoiceServiceDetailConnection!
  """Customer accounts."""
  accounts(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AccountConnection!
  """ACH batches."""
  ach_batches(
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
    """The batch ID that gets inserted into the ACH file on generation."""
    ach_sequence: Int64Bit
    """The provider to use when transacting against bank accounts."""
    format: BankAccountProvider
    """This batch includes payments after this date."""
    payments_after: Datetime
    """This batch includes payments before this date."""
    payments_before: Datetime
    """Whether this is a batch of debits or credits."""
    type: AchBatchType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AchBatchConnection!
  """Address lists."""
  address_lists(
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
    The types of account statuses for accounts that are part of this grouping.
    """
    account_status: AddressListAccountStatus
    """The delinquency state for accounts that are part of this grouping."""
    delinquency: AddressListDelinquency
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AddressListConnection!
  """Address statuses."""
  address_statuses(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AddressStatusConnection!
  """Geographical addresses."""
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
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
  """Details related to an adjustment service."""
  adjustment_service_details(
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
    The amount that can be adjusted using this service within the period defined in `adjustment_service_days`.
    """
    amount: Int
    """
    The period of time in which transactions are tracked to calculate against
    the total defined in `adjustment_service_amount`.
    """
    days: Int
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AdjustmentServiceDetailConnection!
  """Adtran Mosaic audits."""
  adtran_mosaic_audits(
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
    """The ID of an AccountService."""
    account_service_id: Int64Bit
    """The Adtran assigned device name."""
    adtran_device_name: String
    """The serial number associated with the Adtran device."""
    adtran_device_serial_number: String
    """The Adtran interface name."""
    adtran_interface_name: String
    """The ID of an Adtran Mosaic setting."""
    adtran_mosaic_setting_id: Int64Bit
    """The Adtran object returned by the API."""
    adtran_object: String
    """The Adtran service ID."""
    adtran_service_id: String
    """The interface name associated with the Adtran service."""
    adtran_service_interface_name: String
    """The audit message describing why item included."""
    audit_message: String
    """The audit reason code of why item included."""
    audit_reason_code: String
    """The ID of an `InventoryItem`."""
    inventory_item_id: Int64Bit
    """is_visible of the information"""
    is_visible: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AdtranMosaicAuditConnection!
  """Adtran Mosaic cloud list."""
  adtran_mosaic_cloud_list(
    """The type."""
    list_type: AdtranMosaicCloudListType!
    """fields.list_type"""
    list_filter: String
    """The ID of an Adtran Mosaic setting."""
    adtran_mosaic_setting_id: Int64Bit
    """The base API URL."""
    api_url: String
    """A username, used for authentication."""
    username: String
    """A password."""
    password: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
  ): AdtranMosaicCloudListConnection!
  """Adtran Mosaic Kafka events."""
  adtran_mosaic_kafka_events(
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
    """The ID of an Adtran Mosaic setting."""
    adtran_mosaic_setting_id: Int64Bit
    """The Kafka topic to for the event."""
    kafka_topic: String
    """Key for a specific value."""
    key: String
    """The value."""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AdtranMosaicKafkaEventConnection!
  """Adtran Mosaic Settings."""
  adtran_mosaic_settings(
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
    """Controls if Sonar updates the ICMP device status from SMx alarms"""
    alarms_change_device_status: Boolean
    """Controls if Sonar should add SMx device alarms to inventory item logs"""
    alarms_create_logs: Boolean
    """The base API URL."""
    api_url: String
    """Whether or not to suspend unattached services."""
    auto_suspend_unattached_services: Boolean
    """
    Disable, pause, then re-enable Calix ONT ports after creating or removing
    service.  Recommended for deployments using DHCP within SMx.
    """
    bounce_ports: Boolean
    """Bounce ports disable profile."""
    bounce_ports_disable_profile: String
    """Bounce ports enable profile."""
    bounce_ports_enable_profile: String
    """Commercial account type delinquency profile vector."""
    commercial_delinquency_profile_vector: String
    """Whether or not commercial account type suspends."""
    commercial_delinquency_suspends: Boolean
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """The name of the default Adtran Mosaic downlink inner tag vlan."""
    default_downlink_inner_tag_vlan: String
    """The name of the default Adtran Mosaic downlink interface."""
    default_downlink_interface_name: String
    """The name of the default Adtran Mosaic downlink outer tag vlan."""
    default_downlink_outer_tag_vlan: String
    """The name of the default Adtran Mosaic content provider."""
    default_uplink_content_provider_name: String
    """The name of the default Adtran Mosaic uplink inner tag vlan."""
    default_uplink_inner_tag_vlan: String
    """The name of the default Adtran Mosaic uplink outer tag vlan."""
    default_uplink_outer_tag_vlan: String
    """Whether or not this is enabled."""
    enabled: Boolean
    """Government account type delinquency profile vector."""
    government_delinquency_profile_vector: String
    """Whether or not government account type suspends."""
    government_delinquency_suspends: Boolean
    """Industrial account type delinquency profile vector."""
    industrial_delinquency_profile_vector: String
    """Whether or not industrial account type suspends."""
    industrial_delinquency_suspends: Boolean
    """The date and time this device was last synchronized."""
    last_synchronized: Datetime
    """A password."""
    password: String
    """Residential account type delinquency profile vector."""
    residential_delinquency_profile_vector: String
    """Whether or not residential account type suspends."""
    residential_delinquency_suspends: Boolean
    """Senior citizen account type delinquency profile vector."""
    senior_citizen_delinquency_profile_vector: String
    """Whether or not senior citizen account type suspends."""
    senior_citizen_delinquency_suspends: Boolean
    """Whether or not a synchronization audit has been run."""
    synchronization_audit_ran: Boolean
    """Whether or not a synchronization request is queued."""
    synchronization_queued: Boolean
    """The date/time that synchronization started."""
    synchronization_start: Datetime
    """Status of the synchronization process."""
    synchronization_status: SynchronizationStatus
    """Details regarding the current synchronization status if any."""
    synchronization_status_message: String
    """A username, used for authentication."""
    username: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AdtranMosaicSettingConnection!
  """Adtran Mosaic workflow events."""
  adtran_mosaic_workflow_events(
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
    """The ID of an Adtran Mosaic setting."""
    adtran_mosaic_setting_id: Int64Bit
    """The completion status of the event."""
    completion_status: String
    """The complete event object of the event."""
    event_object: String
    """The status of the event."""
    status: String
    """The timestamp of the event."""
    timestamp: Datetime
    """The transaction ID of the event."""
    trans_id: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AdtranMosaicWorkflowEventConnection!
  """Alerting rotation days and times."""
  alerting_rotation_days(
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
    """The alerting rotation ID."""
    alerting_rotation_id: Int64Bit
    """A day."""
    day: Day
    """The end time for the day."""
    end_time: Time
    """The start time for the day."""
    start_time: Time
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AlertingRotationDayConnection!
  """Inventory items associated with alerting rotations."""
  alerting_rotation_inventory_items(
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
    """The alerting rotation ID."""
    alerting_rotation_id: Int64Bit
    """The ID of an `InventoryItem`."""
    inventory_item_id: Int64Bit
    """
    The date and time that this rotation was last notified of a status change.
    """
    last_alerted_datetime: Datetime
    """The last monitoring status of an inventory item."""
    last_overall_status: InventoryItemDeviceStatus
    """The date and time that the inventory item status last changed."""
    last_status_change_datetime: Datetime
    """The next date and time to send a status alert for this rotation."""
    next_alert_datetime: Datetime
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AlertingRotationInventoryItemConnection!
  """Alerting rotations."""
  alerting_rotations(
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
    """Whether to include all account equipment in this rotation."""
    all_accounts: Boolean
    """Whether to include all inventory models in this rotation."""
    all_inventory_models: Boolean
    """Whether to include all network site equipment in this rotation."""
    all_network_sites: Boolean
    """
    The number of minutes a device can be in a down state before generating alert.
    """
    down_time_in_minutes_before_alerting: Int
    """
    The number of minutes a device can remain in a down state before sending a repeat alert.
    """
    down_time_in_minutes_before_repeat: Int
    """Whether or not this is enabled."""
    enabled: Boolean
    """Whether this repeats forever or not."""
    infinite_repetitions: Boolean
    """A descriptive name."""
    name: String
    """The number of times this repeats."""
    repetitions: Int
    """The start."""
    start: Date
    """
    The number of minutes a device can be in a warning state before generating alert.
    """
    warning_time_in_minutes_before_alerting: Int
    """
    The number of minutes a device can remain in a warning state before sending a repeat alert.
    """
    warning_time_in_minutes_before_repeat: Int
    """The number of weeks between repetitions."""
    weeks_between_repetitions: Int
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AlertingRotationConnection!
  """Application firewall rules."""
  application_firewall_rules(
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
    """A human readable description."""
    description: String
    """An IPv4/IPv6 subnet."""
    subnet: SubnetScalar
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ApplicationFirewallRuleConnection!
  """Auth providers."""
  auth_providers(
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
    """The Auth0 client ID."""
    auth0_client_id: String
    """Whether or not this is enabled."""
    enabled: Boolean
    """The type."""
    type: AuthProviderType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AuthProviderConnection!
  """Available explores."""
  available_explores: AvailableExploresConnection!
  """Available reports."""
  available_reports: AvailableReportsConnection!
  """Avalara tax categories."""
  avalara_tax_categories(
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
    """A descriptive name."""
    name: String
    """The value."""
    value: Int
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AvalaraTaxCategoryConnection!
  """Avalara tax definitions."""
  avalara_tax_definitions(
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
    """Whether or not this entity is archived."""
    archived: Boolean
    """Whether or not this tax definition is custom."""
    is_custom: Boolean
    """The service name as defined by Avalara."""
    service_name: String
    """The service type as defined by Avalara."""
    service_type: Int
    """The transaction name as defined by Avalara."""
    transaction_name: String
    """The transaction type as defined by Avalara."""
    transaction_type: Int
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AvalaraTaxDefinitionConnection!
  """Bank account processor credentials."""
  bank_account_processor_credentials(
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
    """The ID of a BankProcessor."""
    bank_account_processor_id: Int64Bit
    """The credential name."""
    credential: BankAccountProviderCredential
    """The value."""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): BankAccountProcessorCredentialConnection!
  """Processors of transactions to and from bank accounts."""
  bank_account_processors(
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
    """Whether or not this is enabled."""
    enabled: Boolean
    """Whether or not this is the primary type of entity."""
    primary: Boolean
    """The provider for this processor."""
    provider: BankAccountProvider
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): BankAccountProcessorConnection!
  """Bank accounts."""
  bank_accounts(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): BankAccountConnection!
  """Default billing values for new accounts."""
  billing_defaults(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): BillingDefaultConnection!
  """Services associated with a linked billing default."""
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
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
  """Billing settings."""
  billing_setting: BillingSetting!
  """Cable modem provisioner credentials."""
  cable_modem_provisioner_credentials(
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
    """The ID of a `CableModemProvisioner`."""
    cable_modem_provisioner_id: Int64Bit
    """An individual credential to authenticate to a cable modem provisioner."""
    credential: CableModemProvisionerAuthenticationCredential
    """The credential value (e.g. username, password, etc.)"""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CableModemProvisionerCredentialConnection!
  """Cable modem provisioners."""
  cable_modem_provisioners(
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
    """Whether or not this is enabled."""
    enabled: Boolean
    """Hostname."""
    hostname: String
    """The date and time this device was last synchronized."""
    last_synchronized: Datetime
    """A descriptive name."""
    name: String
    """The status."""
    status: ProvisioningDeviceStatus
    """A message describing what caused the current status of this device."""
    status_message: String
    """Whether or not a synchronization request is queued."""
    synchronization_queued: Boolean
    """The date/time that synchronization started."""
    synchronization_start: Datetime
    """The type."""
    type: CableModemProvisionerType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CableModemProvisionerConnection!
  """Calendar - iCalendar"""
  calendar_icals(
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
    """Whether or not this is enabled."""
    enabled: Boolean
    """A descriptive name."""
    name: String
    """
    The url that can be used on remote calendars for integration of Sonar events.
    """
    url: URL
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CalendarIcalConnection!
  """Calix Cloud audits."""
  calix_cloud_audits(
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
    """The ID of a `CalixCloudSetting`."""
    calix_cloud_setting_id: Int64Bit
    """The Calix Cloud subscriber json object."""
    subscriber: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CalixCloudAuditConnection!
  """Calix Cloud settings."""
  calix_cloud_settings(
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
    """The Auth0 client ID."""
    client_id: String
    """The Auth0 client secret."""
    client_secret: String
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """Whether or not this is enabled."""
    enabled: Boolean
    """The date and time this device was last synchronized."""
    last_synchronized: Datetime
    """An array of Calix service group definitions."""
    service_group_tiers: Text
    """The ID of a `CustomField` that will map to Calix subscriber field1."""
    subscriber_field1_id: Int64Bit
    """The ID of a `CustomField` that will map to Calix subscriber field2."""
    subscriber_field2_id: Int64Bit
    """The ID of a `CustomField` that will map to Calix subscriber field3."""
    subscriber_field3_id: Int64Bit
    """The ID of a `CustomField` that will map to Calix subscriber field4."""
    subscriber_field4_id: Int64Bit
    """The ID of a `CustomField` that will map to Calix subscriber field5."""
    subscriber_field5_id: Int64Bit
    """The area type to be used for the location."""
    subscriber_location: CalixSubscriberAreaType
    """The area type to be used for the region."""
    subscriber_region: CalixSubscriberAreaType
    """Whether or not a synchronization audit has been run."""
    synchronization_audit_ran: Boolean
    """Whether or not a synchronization request is queued."""
    synchronization_queued: Boolean
    """The date/time that synchronization started."""
    synchronization_start: Datetime
    """Status of the synchronization process."""
    synchronization_status: SynchronizationStatus
    """Details regarding the current synchronization status if any."""
    synchronization_status_message: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CalixCloudSettingConnection!
  """Unique Calix SMx server configuration."""
  calix_integrations(
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
    """Controls if Sonar updates the ICMP device status from SMx alarms"""
    alarms_change_device_status: Boolean
    """Controls if Sonar should add SMx device alarms to inventory item logs"""
    alarms_create_logs: Boolean
    """
    Controls if Sonar updates the inventory item's soft IP address from SMx DHCP lease alarms.
    """
    alarms_update_ip_assignment: Boolean
    """
    Disable, pause, then re-enable Calix ONT ports after creating or removing
    service.  Recommended for deployments using DHCP within SMx.
    """
    bounce_ports: Boolean
    """
    The Calix policy map name to use when a commercial account becomes delinquent.
    """
    commercial_delinquency_policy_map: String
    """
    The Calix service template name to use when a commercial account becomes delinquent.
    """
    commercial_delinquency_service_template: String
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """
    Whether or not a default Calix service detail record is created when integration service added.
    """
    create_default_service_detail: Boolean
    """
    Controls whether to turn on synchronization of Calix ONTs and Subscribers, from Sonar Inventory Items and Accounts.
    """
    enable_ont_synchronization: Boolean
    """Whether or not this is enabled."""
    enabled: Boolean
    """
    The Calix policy map name to use when a government account becomes delinquent.
    """
    government_delinquency_policy_map: String
    """
    The Calix service template name to use when a government account becomes delinquent.
    """
    government_delinquency_service_template: String
    """
    The Calix policy map name to use when an industrial account becomes delinquent.
    """
    industrial_delinquency_policy_map: String
    """
    The Calix service template name to use when an industrial account becomes delinquent.
    """
    industrial_delinquency_service_template: String
    """The date and time this device was last synchronized."""
    last_synchronized: Datetime
    """Subscriber organization ID to use for integration"""
    org_id: String
    """
    The Calix policy map name to use when a residential account becomes delinquent.
    """
    residential_delinquency_policy_map: String
    """
    The Calix service template name to use when a residential account becomes delinquent.
    """
    residential_delinquency_service_template: String
    """
    The Calix policy map name to use when a senior citizen account becomes delinquent.
    """
    senior_citizen_delinquency_policy_map: String
    """
    The Calix service template name to use when a senior citizen account becomes delinquent.
    """
    senior_citizen_delinquency_service_template: String
    """The basic auth credentials to use with SMx, username:password"""
    smx_credentials: String
    """
    The URL of the SMx server including the SMx API port, eg. mysmx.org:18443 (SMx uses 18443 as the default API port)
    """
    smx_url: String
    """The software version of SMx that will be used in integration"""
    smx_version: CalixIntegrationVersion
    """The status."""
    status: ProvisioningDeviceStatus
    """A message describing what caused the current status of this device."""
    status_message: String
    """
    The ID of the account custom field which holds the SMx subscriber ID of the account.
    """
    subscriber_custom_field_id: Int64Bit
    """Whether or not a synchronization request is queued."""
    synchronization_queued: Boolean
    """The date/time that synchronization started."""
    synchronization_start: Datetime
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CalixIntegrationConnection!
  """Calix provisioning list."""
  calix_provisioning_list(
    """The type."""
    list_type: CalixProvisioningListType
    """Calix Inegartion ID."""
    calix_integration_id: Int64Bit
    """The ID of an `InventoryItem`."""
    inventory_item_id: Int64Bit
    """
    The URL of the SMx server including the SMx API port, eg. mysmx.org:18443 (SMx uses 18443 as the default API port)
    """
    smx_url: String
    """The basic auth credentials to use with SMx, username:password"""
    smx_credentials: String
    """The software version of SMx that will be used in integration"""
    smx_version: CalixIntegrationVersion
    """Provides the ability to paginate through results."""
    paginator: Paginator
  ): CalixProvisioningListConnection!
  """Call Detail Record Import Recipes"""
  call_detail_record_import_recipes(
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
    """How many records passed validation checks during import."""
    clean_records: Int
    """Any errors encountered for this import."""
    errors: Clob
    """How many records did not pass validation checks during import."""
    failed_records: Int
    """The identifier of a unique batch at Flatfile."""
    flatfile_batch_identifier: String
    """A hash of the data content of an import."""
    hash: String
    """The progress of an import as a percentage."""
    progress: Int
    """The unique identifier of an import at Sonar."""
    sonar_batch_identifier: String
    """The start date and time for the import."""
    start_datetime: Datetime
    """The status."""
    status: ImportStatus
    """The ID of a User."""
    user_id: Int64Bit
    """The ID of a `VoiceProvider`."""
    voice_provider_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CallDetailRecordImportRecipeConnection!
  """Call Detail Record Imports"""
  call_detail_record_imports(
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
    """The ID of a call data record (CDR) import."""
    call_data_record_import_id: Int64Bit
    """How many records passed validation checks during import."""
    clean_records: Int
    """Any errors encountered for this import."""
    errors: Text
    """How many records did not pass validation checks during import."""
    failed_records: Int
    """The status."""
    status: AsyncImportStatus
    """The ID of a `VoiceProvider`."""
    voice_provider_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CallDetailRecordImportConnection!
  """Call Detail Records"""
  call_detail_records(
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
    amount: Float
    """The rate that is charged to a customer."""
    charge_rate: Float
    """
    The prefix description for the call detail record having provider rated prefix.
    """
    description: String
    """The direction of the call."""
    direction: CallDetailRecordDirection
    """The total length of the call in seconds."""
    length_in_seconds: Int
    """The matched prefix of this call record."""
    matched_prefix: String
    """The ID of a `MonthlyBillingCompletion`."""
    monthly_billing_completion_id: Int64Bit
    """The DID that initiated the call."""
    originating_number: String
    """The prefix type of this call record."""
    prefix_type: CallDetailRecordPrefixType
    """The DID that received the call."""
    receiving_number: String
    """The ID of a Service."""
    service_id: Int64Bit
    """When the call was started."""
    started_at: Datetime
    """The ID of a `VoiceProvider`."""
    voice_provider_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CallDetailRecordConnection!
  """Call Logs for accounts."""
  call_logs(
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
    """The body."""
    body: Text
    """The subject."""
    subject: String
    """The time in seconds."""
    time_in_seconds: String
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CallLogConnection!
  """Canned replies."""
  canned_replies(
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
    """The body."""
    body: Text
    """The ID of a `CannedReplyCategory`."""
    canned_reply_category_id: Int64Bit
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CannedReplyConnection!
  """Canned reply categories."""
  canned_reply_categories(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CannedReplyCategoryConnection!
  """Canned reply with variable replacement."""
  canned_reply_with_variable_replacement(
    """fields.canned_reply_id"""
    canned_reply_id: Int64Bit!
    """The ID of a `Ticket`."""
    ticket_id: Int64Bit!
  ): CannedReply!
  """Companies that you do business as."""
  companies(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CompanyConnection!
  """Departments in a company."""
  company_departments(
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
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """A two character country code for this phone number."""
    country: Country
    """The ID of a department."""
    department_id: Int64Bit
    """An email address."""
    email_address: EmailAddress
    """The extension."""
    extension: Numeric
    """The number."""
    number: Numeric
    """A phone number formatted for human readability."""
    number_formatted: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CompanyDepartmentConnection!
  """A contact person."""
  contacts(
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
    """The ID of the entity that owns this contact."""
    contactable_id: Int64Bit
    """The type of entity that owns this contact."""
    contactable_type: ContactableType
    """An email address."""
    email_address: EmailAddress
    """A supported language."""
    language: Language
    """Whether or not marketing messages accepted."""
    marketing_opt_in: Boolean
    """A descriptive name."""
    name: String
    """Whether or not this is the primary type of entity."""
    primary: Boolean
    """The role of the contact, e.g. "CEO" or "Network Engineer"."""
    role: String
    """A username, used for authentication."""
    username: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ContactConnection!
  """Contract templates."""
  contract_templates(
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
    """The body."""
    body: Text
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """Whether or not this is enabled."""
    enabled: Boolean
    """A descriptive name."""
    name: String
    """The term in months."""
    term_in_months: Int
    """The ID of a `TicketGroup`."""
    ticket_group_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ContractTemplateConnection!
  """Contracts."""
  contracts(
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
    """The body."""
    body: Text
    """The ID of the contact that owns this."""
    contact_id: Int64Bit
    """The ID of a `ContractTemplate`."""
    contract_template_id: Int64Bit
    """The custom message."""
    custom_message: Text
    """The expiration date."""
    expiration_date: Date
    """The ID of a `HandwrittenSignature`."""
    handwritten_signature_id: Int64Bit
    """A descriptive name."""
    name: String
    """The term in months."""
    term_in_months: Int
    """Part of the unique URL used for signing."""
    unique_link_key: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ContractConnection!
  """Core credit cards."""
  core_credit_cards(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CreditCardConnection!
  """Core invoices."""
  core_invoices(
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
    """The number of times that autopay has been attempted."""
    auto_pay_attempts: Int
    """The date that autopay will be attempted."""
    auto_pay_date: Date
    """The sum of all due amounts on child invoices."""
    child_invoice_remaining_due: Int
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """A date"""
    date: Date
    """The date that this became delinquent."""
    delinquency_date: Date
    """Whether or not this entity is delinquent."""
    delinquent: Boolean
    """The date this invoice is due by."""
    due_date: Date
    """The date that this ends."""
    end_date: Date
    """
    If an invoice is frozen, payments will not be automatically applied to it, and it cannot be modified.
    """
    frozen: Boolean
    """
    The ID of the Invoice Template Version which was active when this invoice was generated.
    """
    invoice_template_version_id: Int64Bit
    """Whether or not a late fee has been applied."""
    late_fee_applied: Boolean
    """Whether or not the invoice includes only late fees."""
    late_fee_only: Boolean
    """The message."""
    message: Text
    """The number of months of service this invoice was billed for."""
    number_of_months: Int
    """The ID of the `Invoice` that is this `Invoice`s master."""
    parent_invoice_id: Int64Bit
    """
    Used by system to indicate the invoice has been marked to be sent to email contacts.
    """
    pending_email: Boolean
    """The amount remaining to be paid."""
    remaining_due: Int
    """The phase of the invoice moving through creation."""
    status: String
    """Whether this entity's taxes have been committed or not."""
    tax_committed: Boolean
    """The ID of an `TaxProvider`."""
    tax_provider_id: Int64Bit
    """The sum of all debits that make up this invoice."""
    total_debits: Int
    """The sum of all taxes on debits that make up this invoice."""
    total_taxes: Int
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InvoiceConnection!
  """Core transactions."""
  core_transactions(
    """The ID of an Account."""
    account_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
  ): TransactionConnection!
  """Credit card processor credentials."""
  credit_card_processor_credentials(
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
    """The credential name."""
    credential: CreditCardProviderCredential
    """The ID of a CreditCardProcessor."""
    credit_card_processor_id: Int64Bit
    """The value."""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CreditCardProcessorCredentialConnection!
  """Credit card processors configured in Sonar."""
  credit_card_processors(
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
    """American Express."""
    amex: Boolean
    """Dankort."""
    dankort: Boolean
    """Diner's Club."""
    dinersclub: Boolean
    """Discover."""
    discover: Boolean
    """Whether or not this is enabled."""
    enabled: Boolean
    """Forbrugsforeningen."""
    forbrugsforeningen: Boolean
    """JCB"""
    jcb: Boolean
    """Maestro."""
    maestro: Boolean
    """MasterCard."""
    mastercard: Boolean
    """
    Enables processor specific `Mail Or Telephone Order` functionality. Currently only applicable for `Stripe`.
    """
    moto_enabled: Boolean
    """Whether or not this is the primary type of entity."""
    primary: Boolean
    """The company that provides credit card processing services."""
    provider: CreditCardProvider
    """Union Pay."""
    unionpay: Boolean
    """Visa"""
    visa: Boolean
    """VISA Electron."""
    visaelectron: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CreditCardProcessorConnection!
  """Credit cards."""
  credit_cards(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CreditCardConnection!
  """Credits applied to invoices."""
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
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
  """Data in custom fields."""
  custom_field_data(
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
    """The ID of a CustomField that is associated with this type of entity."""
    custom_field_id: Int64Bit
    """The ID of the entity that owns this custom field data."""
    customfielddataable_id: Int64Bit
    """The type of entity that owns this custom field data."""
    customfielddataable_type: CustomfielddataableType
    """The value."""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CustomFieldDataConnection!
  """Custom fields."""
  custom_fields(
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
    """The type of entity this custom field will be associated with."""
    entity_type: CustomfielddataableType
    """
    A list of values that are valid for this field, if this is a TEXT field. If
    this is empty, and the field is a TEXT type, then any value will be allowed.
    """
    enum_options: [String]
    """A descriptive name."""
    name: String
    """Whether or not this field is required."""
    required: Boolean
    """The type."""
    type: CustomFieldType
    """
    Whether or not the value of this custom field must be unique throughout the system.
    """
    unique: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CustomFieldConnection!
  """Custom links."""
  custom_links(
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
    """An icon."""
    icon: String
    """The color of the icon."""
    icon_color: HtmlHexColor
    """A title that will be displayed for this item."""
    label: String
    """The model."""
    model: CustomLinkModel
    """A descriptive name."""
    name: String
    """The URL to navigate to."""
    url: URL
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): CustomLinkConnection!
  """
  Variables that are available to be used in Custom Links. These variables will be URL encoded in the custom link.
  """
  custom_links_allowed_variables(
    """The model."""
    model: CustomLinkModel!
  ): [CustomLinksAllowedVariables]!
  """Custom links that are for a given entity."""
  custom_links_for_entity(
    """The model."""
    model: CustomLinkModel!
    """The ID of the entity."""
    id: Int64Bit!
    """Provides the ability to paginate through results."""
    paginator: Paginator
  ): CustomLinksForEntityConnection!
  """Aggregate values for a given date."""
  daily_aggregate_values(
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
    """Additional context regarding the item."""
    context: Text
    """A date"""
    date: Date
    """Key for a specific value."""
    key: AggregateKey
    """The value."""
    value: Float
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DailyAggregateValueConnection!
  """Details related to a data service."""
  data_service_details(
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
    """How often this service bills, in months."""
    billing_frequency: Int
    """The download speed of the service in kilobits per second."""
    download_speed_kilobits_per_second: Int
    """The ID of a Service."""
    service_id: Int64Bit
    """
    The FCC technology code for the service. Only relevant to US ISPs filing FCC Form 477.
    """
    technology_code: TechnologyCode
    """
    The global service profile name for this service if using Telrad provisioning.
    """
    telrad_global_service_profile_name: String
    """The upload speed of the service in kilobits per second."""
    upload_speed_kilobits_per_second: Int
    """The ID of a `UsageBasedBillingPolicy`."""
    usage_based_billing_policy_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DataServiceDetailConnection!
  """Data usage."""
  data_usage(
    """The date and time that this starts."""
    start_datetime: Datetime
    """The date and time that this ends."""
    end_datetime: Datetime
    """The time."""
    time: Datetime
    """The ID of an Account."""
    account_id: Int64Bit!
    """The approximate number of datapoints to return."""
    datapoints: Int64Bit
  ): [DataUsage]!
  """Data usage history."""
  data_usage_histories(
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
    """The total billable inbound data in bytes."""
    billable_in_bytes: Int64Bit
    """The total billable outbound data in bytes."""
    billable_out_bytes: Int64Bit
    """The end time of this data usage history interval."""
    end_time: Datetime
    """The total free inbound data in bytes."""
    free_in_bytes: Int64Bit
    """The total free outbound data in bytes."""
    free_out_bytes: Int64Bit
    """The policy cap when this data usage history interval was closed."""
    policy_cap_at_close_in_bytes: Int64Bit
    """The total available rollover data in bytes."""
    rollover_available_in_bytes: Int64Bit
    """The total remaining rollover data in bytes."""
    rollover_remainder_bytes: Int64Bit
    """The total unconsumed rollover data in bytes."""
    rollover_unconsumed_bytes: Int64Bit
    """The rollover used when this data usage history interval was closed."""
    rollover_used_at_close_in_bytes: Int64Bit
    """The start time of this data usage history interval."""
    start_time: Datetime
    """The top off total when this data usage history interval was closed."""
    top_off_total_at_close_in_bytes: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DataUsageHistoryConnection!
  """Data usage top offs."""
  data_usage_top_offs(
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
    """The amount of top off data in bytes."""
    amount_in_bytes: Int64Bit
    """The ID of a `DataUsageHistory`."""
    data_usage_history_id: Int64Bit
    """The ID of a `Debit`."""
    debit_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DataUsageTopOffConnection!
  """Shows the data usage total for a given time period."""
  data_usage_totals(
    """The date and time that this starts."""
    start_datetime: Datetime
    """The date and time that this ends."""
    end_datetime: Datetime
    """The ID of an Account."""
    account_id: Int64Bit!
  ): DataUsageTotalConnection!
  """Debits."""
  debits(
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
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """A human readable description."""
    description: String
    """A general ledger code."""
    general_ledger_code: String
    """A general ledger code description."""
    general_ledger_code_description: String
    """The ID of an `Invoice`."""
    invoice_id: Int64Bit
    """The ID of the Debit which is linked to the current Debit."""
    linked_debit_id: Int64Bit
    """The total number of minutes."""
    minutes: Float
    """The number of months of service this invoice was billed for."""
    number_of_months: Int
    """The date this transaction was prorated from."""
    prorated_from: Date
    """The date this transaction was prorated to."""
    prorated_to: Date
    """The quantity for this service."""
    quantity: Int
    """
    The quantity the associated service had before the quantity was changed and prorated.
    """
    quantity_prorated_from: Int
    """
    The quantity the associated service was changed to when the quantity was changed and prorated.
    """
    quantity_prorated_to: Int
    """Whether or not this has been reversed."""
    reversed: Boolean
    """When this was reversed."""
    reversed_at: Datetime
    """The user ID that reversed this."""
    reversed_by_user_id: Int64Bit
    """The ID of a Service."""
    service_id: Int64Bit
    """The name of a service."""
    service_name: String
    """The type of transaction on this service."""
    service_transaction_type: ServiceTransactionType
    """The type."""
    type: ServiceType
    """The ID of the user who created this transaction."""
    user_id: Int64Bit
    """The ID of a voice service configuration parameter."""
    voice_service_generic_parameter_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DebitConnection!
  """Periods of time in which delinquency is not calculated."""
  delinquency_exclusions(
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
    """A day."""
    day: Int
    """A month."""
    month: Int
    """A descriptive name."""
    name: String
    """A year."""
    year: Int
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DelinquencyExclusionConnection!
  """Departments."""
  departments(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DepartmentConnection!
  """Modes in which a piece of inventory can be deployed."""
  deployment_types(
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
    """The ID of an `InventoryModel`."""
    inventory_model_id: Int64Bit
    """A descriptive name."""
    name: String
    """The ID of a `NetworkMonitoringTemplate`."""
    network_monitoring_template_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DeploymentTypeConnection!
  """Deposit slips."""
  deposit_slips(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DepositSlipConnection!
  """Device interface mappings."""
  device_interface_mappings(
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
    """A human readable description."""
    description: String
    """The ID of an `InventoryItem`."""
    inventory_item_id: Int64Bit
    """A MAC address."""
    mac_address: MacAddress
    """The metadata."""
    metadata: Text
    """The interface in speed in Mbps."""
    speed_mbps_in: Int
    """The interface out speed in Mbps."""
    speed_mbps_out: Int
    """The type."""
    type: String
    """Whether or not this interface is up."""
    up: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DeviceInterfaceMappingConnection!
  """DHCP server credentials."""
  dhcp_server_credentials(
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
    """A credential for a `DhcpServer`."""
    credential: DhcpServerAuthenticationCredential
    """The ID of a `DhcpServer`."""
    dhcp_server_id: Int64Bit
    """The value of a credential for a `DhcpServer`."""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DhcpServerCredentialConnection!
  """DHCP sever identifiers."""
  dhcp_server_identifiers(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DhcpServerIdentifierConnection!
  """DHCP servers."""
  dhcp_servers(
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
    """An API key."""
    api_key: String
    """Whether or not this is enabled."""
    enabled: Boolean
    """An IPv4/IPv6 address."""
    ip_address: IP
    """The date and time this device was last synchronized."""
    last_synchronized: Datetime
    """A descriptive name."""
    name: String
    """A TCP port."""
    port: Port
    """Does this `DhcpServer` provide DHCP for all IP pools?"""
    serves_all_pools: Boolean
    """The status."""
    status: ProvisioningDeviceStatus
    """A message describing what caused the current status of this device."""
    status_message: String
    """Whether or not a synchronization request is queued."""
    synchronization_queued: Boolean
    """The date/time that synchronization started."""
    synchronization_start: Datetime
    """The type."""
    type: DhcpServerType
    """
    If this is `true`, then Sonar will use the MAC address of the DHCP relay
    rather than the MAC address of the requesting device when writing a lease.
    This should generally be disabled unless you have a specific reason to enable it.
    """
    use_source_mac_address: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DhcpServerConnection!
  """DID assignment histories."""
  did_assignment_histories(
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
    """The date and time of assignment."""
    assigned_datetime: Datetime
    """The ID of a `DidAssignment`."""
    did_assignment_id: Int64Bit
    """The ID of a `Did`."""
    did_id: Int64Bit
    """The date and time of removal."""
    removed_datetime: Datetime
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DidAssignmentHistoryConnection!
  """DID assignments."""
  did_assignments(
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
    """The ID of a `Did`."""
    did_id: Int64Bit
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DidAssignmentConnection!
  """DID Import Recipes."""
  did_import_recipes(
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
    """How many records passed validation checks during import."""
    clean_records: Int
    """Any errors encountered for this import."""
    errors: Clob
    """How many records did not pass validation checks during import."""
    failed_records: Int
    """The identifier of a unique batch at Flatfile."""
    flatfile_batch_identifier: String
    """A hash of the data content of an import."""
    hash: String
    """The progress of an import as a percentage."""
    progress: Int
    """The ID of a `RateCenter`."""
    rate_center_id: Int64Bit
    """The unique identifier of an import at Sonar."""
    sonar_batch_identifier: String
    """The start date and time for the import."""
    start_datetime: Datetime
    """The status."""
    status: ImportStatus
    """The ID of a User."""
    user_id: Int64Bit
    """The ID of a `VoiceProvider`."""
    voice_provider_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DidImportRecipeConnection!
  """DIDs."""
  dids(
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
    """The number."""
    number: String
    """The ID of a `RateCenter`."""
    rate_center_id: Int64Bit
    """The ID of a `VoiceProvider`."""
    voice_provider_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DidConnection!
  """Disbursement details."""
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
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
  """Disbursements."""
  disbursements(
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
    """The bank account."""
    bank_account: String
    """The ID of a BankProcessor."""
    bank_account_processor_id: Int64Bit
    """The ID of a CreditCardProcessor."""
    credit_card_processor_id: Int64Bit
    """The payment processor's external ID."""
    external_id: String
    """The date and time this entity was processed."""
    processed_at: Datetime
    """The disbursement payout schedule."""
    schedule: DisbursementSchedule
    """The amount scheduled for payout."""
    schedule_amount: Int
    """The disbursement payout scheduling factor."""
    schedule_factor: Int
    """The unit of measurement for this disbursement's payout amount."""
    schedule_unit: SonarPayUnit
    """The status."""
    status: DisbursementStatus
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DisbursementConnection!
  """Disconnection logs."""
  disconnection_logs(
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
    """The date and time that the account was disconnected."""
    disconnected_at: Datetime
    """The `User` that disconnected the `Account`."""
    disconnected_by_user_id: Int64Bit
    """The ID of the serviceable address to use for this account."""
    serviceable_address_id: Int64Bit
    """
    The deleted address object, as a formatted single line, that was
    disconnected. Used for historical reporting when address is deleted.
    """
    serviceable_address_reference_record: Text
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DisconnectionLogConnection!
  """Discounts."""
  discounts(
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
    """The amount of the `Discount`."""
    amount: Int
    """The amount remaining that can be used."""
    amount_remaining: Int
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """
    If this discount was created due to reversal of a `Debit`, this field will link to the reversed `Debit`.
    """
    debit_id: Int64Bit
    """A human readable description."""
    description: String
    """A general ledger code."""
    general_ledger_code: String
    """A general ledger code description."""
    general_ledger_code_description: String
    """The total number of minutes."""
    minutes: Float
    """The date this transaction was prorated from."""
    prorated_from: Date
    """The date this transaction was prorated to."""
    prorated_to: Date
    """The quantity for this service."""
    quantity: Int
    """
    The quantity the associated service had before the quantity was changed and prorated.
    """
    quantity_prorated_from: Int
    """
    The quantity the associated service was changed to when the quantity was changed and prorated.
    """
    quantity_prorated_to: Int
    """Whether or not this has been reversed."""
    reversed: Boolean
    """When this was reversed."""
    reversed_at: Datetime
    """The user ID that reversed this."""
    reversed_by_user_id: Int64Bit
    """The ID of a Service."""
    service_id: Int64Bit
    """The name of a service."""
    service_name: String
    """The type of transaction on this service."""
    service_transaction_type: ServiceTransactionType
    """Whether this entity's taxes have been committed or not."""
    tax_committed: Boolean
    """The ID of an `TaxProvider`."""
    tax_provider_id: Int64Bit
    """The type."""
    type: ServiceType
    """The ID of the user who created this transaction."""
    user_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): DiscountConnection!
  """Disputes."""
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
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
  """Drive times."""
  drive_times(
    """fields.drive_time_locations"""
    locations: [DriveTimeLocation]!
  ): DriveTimeResultWrapper
  """Validate contact email address."""
  email_address_lookup(
    """An email address."""
    email_address: String!
    """
    If true, this checks if the contact does not have a username. If this is
    false, then it will check if the account has a username.
    """
    check_if_available: Boolean = true
  ): Contact!
  """
  Email categories are associated with contacts, and define the types of emails
  those contacts receive. The "default" property determines whether or not the
  category is added to newly created contacts by default.
  """
  email_categories(
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
    """Whether or not this entity is a default entry."""
    default: Boolean
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): EmailCategoryConnection!
  """All clicks for each sent email."""
  email_clicks(
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
    """The ID of an email."""
    email_id: Int64Bit
    """
    The ID of a location associated with a record in EmailClick and EmailOpen.
    """
    email_location_id: Int64Bit
    """The date and time of an event sent from Mandrill"""
    event_datetime: Datetime
    """An IPv4/IPv6 address."""
    ip: IP
    """The URL that a user clicked on in a sent email."""
    url: URL
    """
    The user agent string of a user that opened or clicked on a sent email.
    """
    user_agent: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): EmailClickConnection!
  """Email domains."""
  email_domains(
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
    """Whether or not the DKIM record is valid."""
    dkim: Boolean
    """The DNS requirements for domain validation."""
    dns_requirements: String
    """A domain name."""
    domain: DomainName
    """The domain ID from the email provider."""
    provider_domain_id: Int64Bit
    """Indicates that the domain has been verified for migration."""
    ready_for_migration: Boolean
    """Whether or not the SPF record is valid."""
    spf: Boolean
    """Whether or not the record is verified."""
    verified: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): EmailDomainConnection!
  """Get a list of all locations saved for opened and clicked emails."""
  email_locations(
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
    """A city."""
    city: String
    """A two character country code."""
    country: String
    """A decimal latitude."""
    latitude: Latitude
    """A decimal longitude."""
    longitude: Longitude
    """The zip code of an email location sent by a Mandrill event."""
    postal_code: String
    """The timezone you want times in the system displayed in."""
    timezone: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): EmailLocationConnection!
  """Localized email message details for an EmailMessage container."""
  email_message_contents(
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
    """The body."""
    body: Text
    """The ID of an EmailMessage."""
    email_message_id: Int64Bit
    """
    A short sentence that will be shown as a preview in compatible email clients.
    """
    inbox_preview: String
    """A supported language."""
    language: Language
    """The subject."""
    subject: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): EmailMessageContentConnection!
  """Email message templates."""
  email_messages(
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
    The email address to send from when using this email message. If `null`, then the system default will be used.
    """
    from_email_address: EmailAddress
    """
    The name to send from when using this email message. If `null`, then the system default will be used.
    """
    from_name: String
    """A descriptive name."""
    name: String
    """ID of the Saved Message Category."""
    saved_message_category_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): EmailMessageConnection!
  """All opens for each sent email."""
  email_opens(
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
    """The ID of an email."""
    email_id: Int64Bit
    """
    The ID of a location associated with a record in EmailClick and EmailOpen.
    """
    email_location_id: Int64Bit
    """The date and time of an event sent from Mandrill"""
    event_datetime: Datetime
    """An IPv4/IPv6 address."""
    ip: IP
    """
    The user agent string of a user that opened or clicked on a sent email.
    """
    user_agent: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): EmailOpenConnection!
  """Get a list of valid email variables for a specific email trigger."""
  email_variables(
    """The event that triggers a specific `Email`."""
    trigger: EmailTrigger
  ): [EmailVariable]
  """Emails that have been sent."""
  emails(
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
    """The body."""
    body: Text
    """An email address."""
    email_address: EmailAddress
    """The ID of the entity that this email was sent to."""
    emailable_id: Int64Bit
    """The type of entity that this email was sent to."""
    emailable_type: EmailableType
    """If rejected, the reason for rejection."""
    reject_reason: String
    """The status."""
    status: EmailStatus
    """The subject."""
    subject: String
    """The name of the recipient."""
    to_name: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): EmailConnection!
  """LTE EPCs."""
  epcs(
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
    """The identifier used by the EPC, this is typically numeric."""
    identifier: String
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): EpcConnection!
  """Details related to an expiring service."""
  expiring_service_details(
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
    """How often this service bills, in months."""
    billing_frequency: Int
    """The ID of a Service."""
    service_id: Int64Bit
    """The number of times this expiring service should run."""
    times_to_run: Int
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ExpiringServiceDetailConnection!
  """External marketing provider credentials."""
  external_marketing_provider_credentials(
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
    """The ID of an `ExternalMarketingProvider`."""
    external_marketing_provider_id: Int64Bit
    """Key for a specific value."""
    key: ExternalMarketingProviderAuthCredential
    """The value."""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ExternalMarketingProviderCredentialConnection!
  """External marketing providers."""
  external_marketing_providers(
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
    """Whether or not this is enabled."""
    enabled: Boolean
    """
    The `ExternalMarketingProviderType` for 3rd party external marketing integration.
    """
    provider: ExternalMarketingProviderType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ExternalMarketingProviderConnection!
  """The generated FCC Form 477 report."""
  fcc_form_477_reports(
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
    """A date"""
    date: Date
    """The format of the reporting for FCC Form 477."""
    format: FccForm477Format
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): FccForm477ReportConnection!
  """FiberMap integrations."""
  fibermap_integrations(
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
    """Always create new network sites"""
    always_create_new_network_sites: Boolean
    """An API token."""
    api_token: String
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """Whether or not this is enabled."""
    enabled: Boolean
    """Import plans and contacts"""
    import_accounts_and_contacts: Boolean
    """Import serviceable addresses"""
    import_serviceable_addresses: Boolean
    """The date and time this device was last synchronized."""
    last_synchronized: Datetime
    """A descriptive name."""
    name: String
    """Allow serviceability status to be read from map features"""
    read_serviceability_from_features: Boolean
    """The status."""
    status: ProvisioningDeviceStatus
    """A message describing what caused the current status of this device."""
    status_message: String
    """Whether or not a synchronization request is queued."""
    synchronization_queued: Boolean
    """The date/time that synchronization started."""
    synchronization_start: Datetime
    """Update service locations in Vetro Fibermap"""
    update_service_locations: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): FibermapIntegrationConnection!
  """FiberMap plans."""
  fibermap_plans(
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
    """Build"""
    build: String
    """A two character country code."""
    country: String
    """Drop"""
    drop: String
    """FiberMap integration ID"""
    fibermap_integration_id: Int64Bit
    """FiberMap plan ID"""
    fibermap_plan_id: Int64Bit
    """Fibermap project ID."""
    fibermap_project_id: Int64Bit
    """Fibermap project name."""
    fibermap_project_name: String
    """FiberMap updated at"""
    fibermap_updated_at: Datetime
    """Height in meters."""
    height_in_meters: Int
    """is_visible of the information"""
    is_visible: Boolean
    """A decimal latitude."""
    latitude: Latitude
    """A decimal longitude."""
    longitude: Longitude
    """The ID of a map overlay."""
    map_overlay_id: Int64Bit
    """Mapped at"""
    mapped_at: Datetime
    """Mapping user"""
    mapping_user: String
    """A descriptive name."""
    name: String
    """Network site id."""
    network_site_id: Int64Bit
    """A state, province, or other country subdivision."""
    subdivision: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): FibermapPlanConnection!
  """FiberMap service locations"""
  fibermap_service_locations(
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
    """The ID of the address."""
    address_id: Int64Bit
    """Child properties JSON"""
    child_properties_json: String
    """Child Vetro ID"""
    child_vetro_id: String
    """FiberMap integration ID"""
    fibermap_integration_id: Int64Bit
    """FiberMap plan ID"""
    fibermap_plan_id: Int64Bit
    """is_visible of the information"""
    is_visible: Boolean
    """Properties JSON"""
    properties_json: Text
    """Vetro ID"""
    vetro_id: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): FibermapServiceLocationConnection!
  """Files."""
  files(
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
    """A human readable description."""
    description: String
    """The file size, in bytes."""
    file_size_in_bytes: Int64Bit
    """The ID of the entity that owns this file."""
    fileable_id: Int64Bit
    """The type of entity that owns this file."""
    fileable_type: FileableType
    """The file name."""
    filename: String
    """The MIME type of the file."""
    mime_type: String
    """
    An image file may be set to the primary image. This will be used as the
    displayed image for the object that this file is associated to throughout Sonar.
    """
    primary_image: Boolean
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): FileConnection!
  """Find address by fibermap service location."""
  find_address_by_fibermap_service_location(
    """Fibermap service location ID."""
    fibermap_service_location_id: Int64Bit!
    """country"""
    country: String!
  ): Address!
  """Fractional debits."""
  fractional_debits(
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
    """A date"""
    date: Date
    """The ID of a `Debit`."""
    debit_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): FractionalDebitConnection!
  """Fractional tax transactions."""
  fractional_tax_transactions(
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
    """The amount of this `Debit` that was taxed."""
    amount_taxed: Int
    """A date"""
    date: Date
    """A human readable description."""
    description: String
    """The ID of a `TaxTransactions`."""
    tax_transaction_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): FractionalTaxTransactionConnection!
  """General ledger codes."""
  general_ledger_codes(
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
    """A code."""
    code: String
    """A human readable description."""
    description: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): GeneralLedgerCodeConnection!
  """
  This query provides the ability to perform a general, partial matching search across various entities at the same time.
  """
  general_search(
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """fields.general_search_entities"""
    entities: [String]!
    """fields.general_search_search"""
    search: String!
  ): GeneralSearchConnection!
  """Generic inventory assignees."""
  generic_inventory_assignees(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): GenericInventoryAssigneeConnection!
  """Logs of changes made to generic inventory items."""
  generic_inventory_item_action_logs(
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
    """The action that was performed."""
    action: GenericInventoryItemActionLogAction
    """The ID of the entity that this `GenericInventoryItemActionLog` is for."""
    genericinventoryitemactionloggable_id: Int64Bit
    """The type of entity that this `GenericInventoryItemActionLog` is for."""
    genericinventoryitemactionloggable_type: InventoryitemableType
    """The ID of an `InventoryModel`."""
    inventory_model_id: Int64Bit
    """The purchase price of this item."""
    purchase_price: Float
    """The quantity for this service."""
    quantity: Int
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): GenericInventoryItemActionLogConnection!
  """Generic inventory items."""
  generic_inventory_items(
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
    """The type of entity that owns this generic `InventoryItem`."""
    genericinventoryitemable_id: Int64Bit
    """The ID of the entity that owns this generic `InventoryItem`."""
    genericinventoryitemable_type: InventoryitemableType
    """The ID of an `InventoryModel`."""
    inventory_model_id: Int64Bit
    """The quantity for this service."""
    quantity: Int
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): GenericInventoryItemConnection!
  """Geographical tax zones."""
  geo_tax_zones(
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
    """A city."""
    city: String
    """A two character country code."""
    country: Country
    """A US county. Only used for US addresses."""
    county: UsCounty
    """A descriptive name."""
    name: String
    """The rate."""
    rate: Float
    """A state, province, or other country subdivision."""
    subdivision: Subdivision
    """The ID of a Tax."""
    tax_id: Int64Bit
    """A ZIP or postal code."""
    zip: String
    """Whether to match on partial ZIP/postal codes."""
    zip_partial_match: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): GeoTaxZoneConnection!
  """Geofences."""
  geofences(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): GeofenceConnection!
  """Get list of vehicles from external GPS tracking provider."""
  get_gps_tracking_provider_vehicles(
    """A `GpsTrackingProvider` ID."""
    gps_tracking_provider_id: Int64Bit!
    """Filter out vehicles already assigned from external provider list."""
    filter_assigned: Boolean!
  ): GetGpsTrackingProviderVehiclesConnection
  """Returns the next IP address in the IP pool."""
  get_next_ip_address_in_ip_pool(
    """The ID of an `IpPool`."""
    ip_pool_id: Int64Bit!
  ): NextIpAddress!
  """Returns the next subnet in the subnet."""
  get_next_subnet_in_subnet(
    """The ID of a `Subnet`."""
    subnet_id: Int64Bit!
    """fields.cidr_size"""
    cidr_size: Int!
  ): NextSubnet!
  """
  Returns the next available subnet of the requested size in the supernet.
  """
  get_next_subnet_in_supernet(
    """The ID of a `Supernet`."""
    supernet_id: Int64Bit!
    """fields.cidr_size"""
    cidr_size: Int!
  ): NextSubnet!
  """Global inventory model minimums/maximums."""
  global_inventory_model_min_maxes(
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
    """The ID of an `InventoryModel`."""
    inventory_model_id: Int64Bit
    """Maximum value"""
    maximum: Int
    """Minimum value"""
    minimum: Int
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): GlobalInventoryModelMinMaxConnection!
  """GPS tracking provider credentials."""
  gps_tracking_provider_credentials(
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
    """A `GpsTrackingProvider` ID."""
    gps_tracking_provider_id: Int64Bit
    """Key for a specific value."""
    key: GpsTrackingProviderAuthCredential
    """The value."""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): GpsTrackingProviderCredentialConnection!
  """GPS tracking providers."""
  gps_tracking_providers(
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
    """Whether or not this is enabled."""
    enabled: Boolean
    """Whether OAuth authentication required."""
    oauth_required: Boolean
    """A type of GPS tracking provider."""
    provider: GpsTrackingProviderType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): GpsTrackingProviderConnection!
  """Signatures on signed contracts."""
  handwritten_signatures(
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
    The email address of the contact that the contract was originally sent to.
    """
    contact_email_address: EmailAddress
    """The name of the contact that the contract was originally sent to."""
    contact_name: String
    """The role of the contact that the contract was originally sent to."""
    contact_role: String
    """The IP address of the contract signatory."""
    signer_ip: IP
    """The name provided by the contract signatory."""
    signer_name: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): HandwrittenSignatureConnection!
  """ICMP results."""
  icmp_results(
    """The date and time that this starts."""
    start_datetime: Datetime
    """The date and time that this ends."""
    end_datetime: Datetime
    """The ID of an `InventoryItem`."""
    inventory_item_id: Int64Bit!
  ): IcmpNetworkMonitoringResultConnection!
  """Details related to an ActiveDirectory identity provider."""
  identity_provider_active_directory_details(
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
    """Whether to use client SSL certificate authentication or not."""
    cert_auth: Boolean
    """Whether to disable the cache or not."""
    disable_cache: Boolean
    """The list of domains that can be authenticated."""
    domain_aliases: [String]
    """The ActiveDirectory icon URL."""
    icon_url: URL
    """The ID of an `IdentityProvider`."""
    identity_provider_id: Int64Bit
    """The range of IPs with which to use Windows Integrated Auth (Kerberos)."""
    ips: [String]
    """Whether to use Windows Integrated Auth (Kerberos) or not."""
    kerberos: Boolean
    """The ActiveDirectory provisioning ticket URL."""
    ticket_url: URL
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): IdentityProviderActiveDirectoryDetailConnection!
  """Details related to a Google identity provider."""
  identity_provider_google_details(
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
    """The client ID for this identity provider."""
    client_id: String
    """The client secret for this identity provider."""
    client_secret: String
    """The ID of an `IdentityProvider`."""
    identity_provider_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): IdentityProviderGoogleDetailConnection!
  """Details related to a Microsoft identity provider."""
  identity_provider_microsoft_details(
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
    """The client ID for this identity provider."""
    client_id: String
    """The client secret for this identity provider."""
    client_secret: String
    """The ID of an `IdentityProvider`."""
    identity_provider_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): IdentityProviderMicrosoftDetailConnection!
  """Details related to a SAML identity provider."""
  identity_provider_saml_details(
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
    """Authentication domains."""
    auth_domains: String
    """The X.509 signing certificate contents."""
    certificate: Text
    """
    Whether to include more verbose logging during the authentication process or not.
    """
    debug: Boolean
    """The sign request algorithm digest."""
    digest_algorithm: SamlDigestAlgorithm
    """The ID of an `IdentityProvider`."""
    identity_provider_id: Int64Bit
    """The SAML protocol binding."""
    protocol_binding: SamlProtocolBinding
    """The SAML sign in URL."""
    sign_in_endpoint: URL
    """The SAML sign out URL."""
    sign_out_endpoint: URL
    """Whether to sign the SAML request or not."""
    sign_saml_request: Boolean
    """The sign request algorithm."""
    signature_algorithm: SamlSignatureAlgorithm
    """
    The attribute in the SAML token that will be mapped to the user_id property.
    """
    user_id_attribute: URL
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): IdentityProviderSamlDetailConnection!
  """Identity providers."""
  identity_providers(
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
    """The Auth0 connection ID."""
    auth0_connection_id: String
    """Name of connection in Auth0."""
    auth0_connection_name: String
    """The display name."""
    display_name: String
    """Whether or not this is enabled."""
    enabled: Boolean
    """The type."""
    type: IdentityProviderType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): IdentityProviderConnection!
  """Imports of entities in bulk."""
  imports(
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
    The last date and time this entity was updated, or was the subject of a log.
    """
    global_updated_at: Datetime
    """The ID of the entity that owns this import."""
    importrecipeable_id: Int64Bit
    """The type of entity that owns this import."""
    importrecipeable_type: ImportrecipeableType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ImportConnection!
  """Inbound mailboxes."""
  inbound_mailboxes(
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
    """Whether or not to append a signature."""
    append_signature: Boolean
    """The auto reply to send."""
    auto_reply: Text
    """The ID of an `EmailDomain`."""
    email_domain_id: Int64Bit
    """Whether or not to enable Slack integration."""
    enable_slack_integration: Boolean
    """Whether or not this is enabled."""
    enabled: Boolean
    """The mailbox email is sent from."""
    from_mailbox: String
    """
    The name to send from when using this email message. If `null`, then the system default will be used.
    """
    from_name: String
    """The inbound mailbox."""
    inbound_mailbox: String
    """A descriptive name."""
    name: String
    """
    Whether the email body should be posted to Slack, or just the email subject.
    """
    post_email_body_to_slack: Boolean
    """The priority of this item."""
    priority: TicketPriority
    """Whether or not an auto reply should be sent."""
    send_auto_reply: Boolean
    """
    The signature to append. You can include `[PUBLIC_NAME]` as a variable to
    insert the user's public name when the signature is appended.
    """
    signature: Text
    """
    The URL of a Slack webhook. You can generate one at https://my.slack.com/services/new/incoming-webhook.
    """
    slack_webhook_url: URL
    """The ID of a `TicketGroup`."""
    ticket_group_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InboundMailboxConnection!
  """Inline device credentials."""
  inline_device_credentials(
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
    """An individual credential to authenticate to an inline device."""
    credential: InlineDeviceAuthenticationCredential
    """The ID of an `InlineDevice`."""
    inline_device_id: Int64Bit
    """The credential value (e.g. username, password, etc.)"""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InlineDeviceCredentialConnection!
  """Inline devices."""
  inline_devices(
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
    """Whether this device should write entries for all subnets or not."""
    all_subnets: Boolean
    """Whether or not a bandwidth collection request is queued."""
    bandwidth_collection_queued: Boolean
    """The date/time that bandwidth collection started."""
    bandwidth_collection_start: Datetime
    """Whether or not this is enabled."""
    enabled: Boolean
    """An IPv4/IPv6 address."""
    ip_address: IP
    """The date and time this device was last synchronized."""
    last_synchronized: Datetime
    """A descriptive name."""
    name: String
    """A TCP port."""
    port: Port
    """The status."""
    status: ProvisioningDeviceStatus
    """A message describing what caused the current status of this device."""
    status_message: String
    """Whether or not a synchronization request is queued."""
    synchronization_queued: Boolean
    """The date/time that synchronization started."""
    synchronization_start: Datetime
    """The type."""
    type: InlineDeviceType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InlineDeviceConnection!
  """Instance management requests."""
  instance_management_requests(
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
    """The date until which the authorization is valid."""
    authorization_valid_until: Date
    """The reason."""
    reason: Text
    """The date and time responded."""
    responded_at: Datetime
    """The id of the `User` that responded to the request."""
    responded_by_user_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InstanceManagementRequestConnection!
  """Instance Service Funds"""
  instance_service_funds(
    """The instance service fund type."""
    instance_service_fund_type: InstanceServiceFundType
  ): InstanceServiceFunds!
  """
  Integration field mappings.  Mapping of Sonar model field with vendor specific field.
  """
  integration_field_mappings(
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
    """The vendor specific type for field."""
    integration_field_type: IntegrationFieldType
    """The ID of the configuration entity which owns this mapping."""
    integrationconfigurable_id: Int64Bit
    """The type of the configuration entity which owns this mapping."""
    integrationconfigurable_type: String
    """The ID of an `InventoryModelField`."""
    inventory_model_field_id: Int64Bit
    """The ID of an `InventoryModel`."""
    inventory_model_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): IntegrationFieldMappingConnection!
  """
  Integration service mappings.  One-to-one mapping of Sonar service with vendor service name.
  """
  integration_service_mappings(
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
    """The profile vector name in Adtran Mosaic this mapping refers to."""
    adtran_mosaic_profile_vector: String
    """The ID of the configuration entity which owns this mapping."""
    integrationconfigurable_id: Int64Bit
    """The type of the configuration entity which owns this mapping."""
    integrationconfigurable_type: String
    """Policy Map."""
    policy_map: String
    """The ID of a Service."""
    service_id: Int64Bit
    """The service name in vendor system this mapping refers to."""
    service_template_name: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): IntegrationServiceMappingConnection!
  """
  Internal locations within an inventory location (e.g. a shelf or room.)
  """
  internal_locations(
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
    """The ID of an `InventoryLocation`."""
    inventory_location_id: Int64Bit
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InternalLocationConnection!
  """Inventory item events."""
  inventory_item_events(
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
    """An event."""
    event: InventoryItemUpdateEvent
    """The date and time of an event sent from Mandrill"""
    event_datetime: Datetime
    """The ID of an `InventoryItem`."""
    inventory_item_id: Int64Bit
    """Previous data."""
    previous: Text
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InventoryItemEventConnection!
  """Inventory items."""
  inventory_items(
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
    """The ID of an AccountService."""
    account_service_id: Int64Bit
    """The ID of the `User` that claimed this."""
    claimed_user_id: Int64Bit
    """The ID of a `DeploymentType`."""
    deployment_type_id: Int64Bit
    """Whether this inventory item is flapping or not."""
    flapping: Boolean
    """The current ICMP monitoring status of an `InventoryItem`."""
    icmp_device_status: InventoryItemDeviceStatus
    """The number of times the ICMP status has flapped."""
    icmp_status_flap_count: Int
    """The timestamp of when the ICMP status last changed."""
    icmp_status_last_change: Datetime
    """The ICMP monitoring threshold violation type."""
    icmp_threshold_violation: InventoryItemIcmpThresholdViolation
    """The ID of an `InventoryModel`."""
    inventory_model_id: Int64Bit
    """The ID of the entity that this inventory item is assigned to."""
    inventoryitemable_id: Int64Bit
    """The type of entity that this inventory item is assigned to."""
    inventoryitemable_type: InventoryitemableType
    """A decimal latitude."""
    latitude: Latitude
    """A decimal longitude."""
    longitude: Longitude
    """The metadata."""
    metadata: String
    """
    The overall status of an `InventoryItem` (the worse of ICMP/SNMP status).
    """
    overall_status: InventoryItemDeviceStatus
    """The overridden status of an `InventoryItem`."""
    override_status: InventoryItemDeviceStatus
    """The timestamp of when the override status last changed."""
    override_status_last_change: Datetime
    """The ID of the parent `InventoryItem`."""
    parent_inventory_item_id: Int64Bit
    """The status of the device, as read from Preseem."""
    preseem_status: PreseemStatus
    """The ID of a purchase order item"""
    purchase_order_item_id: Int64Bit
    """The purchase price of this item."""
    purchase_price: Int
    """The quantity of this inventory model."""
    quantity: Int
    """The ID of the `InventoryItem` that this segment is a child of."""
    segment_parent_id: Int64Bit
    """The current SNMP monitoring status of an `InventoryItem`."""
    snmp_device_status: InventoryItemDeviceStatus
    """The number of times the SNMP status has flapped."""
    snmp_status_flap_count: Int
    """The timestamp of when the SNMP status last changed."""
    snmp_status_last_change: Datetime
    """The SNMP monitoring status message."""
    snmp_status_message: String
    """The physical status of this item."""
    status: InventoryItemStatus
    """The unit of measurement price for this inventory item."""
    um_price: Int
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InventoryItemConnection!
  """Locations that inventory can be stored."""
  inventory_locations(
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
    Marks this inventory location as the default shipping location for purchase orders.
    """
    default_shipping_location: Boolean
    """A geo-point."""
    geopoint: Geopoint
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InventoryLocationConnection!
  """Categories of inventory."""
  inventory_model_categories(
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
    """The ID of a GeneralLedgerCode."""
    general_ledger_code_id: Int64Bit
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InventoryModelCategoryConnection!
  """
  Data stored on an inventory field (e.g. a MAC address or serial number.)
  """
  inventory_model_field_data(
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
    """The ID of an `InventoryItem`."""
    inventory_item_id: Int64Bit
    """The ID of an `InventoryModelField`."""
    inventory_model_field_id: Int64Bit
    """The value."""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InventoryModelFieldDataConnection!
  """Fields that contain data about an inventory item."""
  inventory_model_fields(
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
    """The ID of an `InventoryModel`."""
    inventory_model_id: Int64Bit
    """A descriptive name."""
    name: String
    """
    A single inventory model field can be set to be the primary field. This will
    be used as the primary identifier for items of this model throughout Sonar.
    """
    primary: Boolean
    """A PCRE regular expression. Omit the leading and closing /."""
    regexp: String
    """Whether or not this field is required."""
    required: Boolean
    """Secondary types that inventory model fields can be set to."""
    secondary_type: InventoryModelFieldSecondaryType
    """Types that inventory model fields can be set to."""
    type: InventoryModelFieldType
    """Whether or not the field contents must be unique."""
    unique: Uniqueness
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InventoryModelFieldConnection!
  """Inventory model minimums/maximums."""
  inventory_model_min_maxes(
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
    """The ID of an `InventoryLocation`."""
    inventory_location_id: Int64Bit
    """The ID of an `InventoryModel`."""
    inventory_model_id: Int64Bit
    """Maximum value"""
    maximum: Int
    """Minimum value"""
    minimum: Int
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InventoryModelMinMaxConnection!
  """Inventory models."""
  inventory_models(
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
    Sets the default vendor to be used for purchasing this inventory model.
    """
    default_vendor_id: Int64Bit
    """The type of inventory model."""
    device_type: InventoryModelDeviceType
    """Whether or not this is enabled."""
    enabled: Boolean
    """Whether or not this is generic."""
    generic: Boolean
    """An icon."""
    icon: Icon
    """The ID of an InventoryModelCategory."""
    inventory_model_category_id: Int64Bit
    """Whether or not inventory item can be broken down into segments."""
    is_segmentable: Boolean
    """
    If this is a SIM card for LTE provisioning, which provider this SIM is for.
    """
    lte_sim_type: LteProviderType
    """The ID of a Manufacturer."""
    manufacturer_id: Int64Bit
    """The actual model name/part number."""
    model_name: String
    """A descriptive name."""
    name: String
    """The ID of a `NetworkMonitoringTemplate`."""
    network_monitoring_template_id: Int64Bit
    """
    The TCP port that the web interface of this type of device is available on.
    """
    port: Int
    """The protocol used to access the web interface."""
    protocol: Protocol
    """The quantity of this inventory model."""
    quantity: Int
    """The unit of measurement for this inventory model."""
    unit_of_measurement: UnitOfMeasurementType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InventoryModelConnection!
  """Invoice attachments."""
  invoice_attachments(
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
    """The date to stop attaching this PDF to invoices."""
    end: Date
    """A descriptive name."""
    name: String
    """The date to start attaching this PDF to invoices."""
    start: Date
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InvoiceAttachmentConnection!
  """Invoice messages."""
  invoice_messages(
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
    """The message."""
    message: String
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InvoiceMessageConnection!
  """Invoice Template Versions."""
  invoice_template_versions(
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
    """The ID of an Invoice Template."""
    invoice_template_id: Int64Bit
    """The content of an Invoice Template which includes a remittance slip."""
    with_remittance: String
    """
    The content of an Invoice Template which does not include a remittance slip.
    """
    without_remittance: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InvoiceTemplateVersionConnection!
  """Invoice Templates."""
  invoice_templates(
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
    """Whether or not this is enabled."""
    enabled: Boolean
    """A descriptive name."""
    name: String
    """If an item is protected, it cannot be modified or deleted."""
    protected: Boolean
    """The content of an Invoice Template which includes a remittance slip."""
    with_remittance: String
    """
    The content of an Invoice Template which does not include a remittance slip.
    """
    without_remittance: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InvoiceTemplateConnection!
  """Invoices."""
  invoices(
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
    """The number of times that autopay has been attempted."""
    auto_pay_attempts: Int
    """The date that autopay will be attempted."""
    auto_pay_date: Date
    """The sum of all due amounts on child invoices."""
    child_invoice_remaining_due: Int
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """A date"""
    date: Date
    """The date that this became delinquent."""
    delinquency_date: Date
    """Whether or not this entity is delinquent."""
    delinquent: Boolean
    """The date this invoice is due by."""
    due_date: Date
    """The date that this ends."""
    end_date: Date
    """
    If an invoice is frozen, payments will not be automatically applied to it, and it cannot be modified.
    """
    frozen: Boolean
    """
    The ID of the Invoice Template Version which was active when this invoice was generated.
    """
    invoice_template_version_id: Int64Bit
    """Whether or not a late fee has been applied."""
    late_fee_applied: Boolean
    """Whether or not the invoice includes only late fees."""
    late_fee_only: Boolean
    """The message."""
    message: Text
    """The number of months of service this invoice was billed for."""
    number_of_months: Int
    """The ID of the `Invoice` that is this `Invoice`s master."""
    parent_invoice_id: Int64Bit
    """
    Used by system to indicate the invoice has been marked to be sent to email contacts.
    """
    pending_email: Boolean
    """The amount remaining to be paid."""
    remaining_due: Int
    """The phase of the invoice moving through creation."""
    status: String
    """Whether this entity's taxes have been committed or not."""
    tax_committed: Boolean
    """The ID of an `TaxProvider`."""
    tax_provider_id: Int64Bit
    """The sum of all debits that make up this invoice."""
    total_debits: Int
    """The sum of all taxes on debits that make up this invoice."""
    total_taxes: Int
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InvoiceConnection!
  """IP assignment histories."""
  ip_assignment_histories(
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
    """The date and time of assignment."""
    assigned_datetime: Datetime
    """A human readable description."""
    description: String
    """The ID of an `IpAssignment`."""
    ip_assignment_id: Int64Bit
    """The ID of the owner of this `IpAssignment`."""
    ipassignmentable_id: Int64Bit
    """The owner of this `IpAssignment`."""
    ipassignmentable_type: IpassignmentableType
    """The ID of the entity that the IP address was assigned to."""
    ipassignmenthistoryable_id: Int64Bit
    """
    The parent entity that the IP address was assigned to (e.g. `Account`, `NetworkSite`.)
    """
    ipassignmenthistoryable_type: IpassignmenthistoryableType
    """Some reference data regarding this IP assignment."""
    reference: Text
    """The date and time of removal."""
    removed_datetime: Datetime
    """
    If this IP was assigned automatically (e.g. via DHCP or RADIUS) then it will be marked as a soft assignment.
    """
    soft: Boolean
    """An IPv4/IPv6 subnet."""
    subnet: SubnetScalar
    """
    Some unique identifier that was related to the IP (e.g. a MAC address, IMSI, RADIUS username.)
    """
    unique_identifier: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): IpAssignmentHistoryConnection!
  """IP assignments."""
  ip_assignments(
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
    """A human readable description."""
    description: String
    """The ID of an `IpPool`."""
    ip_pool_id: Int64Bit
    """The ID of the owner of this `IpAssignment`."""
    ipassignmentable_id: Int64Bit
    """The owner of this `IpAssignment`."""
    ipassignmentable_type: IpassignmentableType
    """Some reference data regarding this IP assignment."""
    reference: Text
    """
    If this IP was assigned automatically (e.g. via DHCP or RADIUS) then it will be marked as a soft assignment.
    """
    soft: Boolean
    """An IPv4/IPv6 subnet."""
    subnet: SubnetScalar
    """The ID of a `Subnet`."""
    subnet_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): IpAssignmentConnection!
  """IP pools."""
  ip_pools(
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
    """The ID of a `DhcpServerIdentifier`."""
    dhcp_server_identifier_id: Int64Bit
    """A range of IPv4 addresses."""
    ip_range: IpRange
    """The number of IP addresses available."""
    ips_available: Int
    """A descriptive name."""
    name: String
    """The ID of a `Subnet`."""
    subnet_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): IpPoolConnection!
  """Job available times."""
  job_available_times(
    """The ID of a `Job`."""
    job_id: Int64Bit!
    """IDs of `User`s."""
    user_ids: [Int64Bit]
    """
    When true, find times where all `user_ids` are available. When `false`, find
    the availabilities for each individual user.
    """
    require_all_users: Boolean = true
    """The date and time that this starts."""
    start_datetime: Datetime!
    """The date and time that this ends."""
    end_datetime: Datetime!
  ): [JobAvailableTimes]
  """Job check ins."""
  job_check_ins(
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
    """The date and time that this `Job` was checked into."""
    check_in_datetime: Datetime
    """The date and time that this `Job` was checked out of."""
    check_out_datetime: Datetime
    """The ID of the `User` that created this check in."""
    checked_in_by_user_id: Int64Bit
    """
    The ID of the `User` that updated this check in with a check out date and time.
    """
    checked_out_by_user_id: Int64Bit
    """The ID of a `Job`."""
    job_id: Int64Bit
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): JobCheckInConnection!
  """Services associated with jobs."""
  job_services(
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
    """The ID of a `Job`."""
    job_id: Int64Bit
    """The quantity for this service."""
    quantity: Int
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): JobServiceConnection!
  """Job types."""
  job_types(
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
    If this is set, any `Job` using this `JobType` that is completed
    successfully while associated with an `Account` will change the `Account` to
    this `AccountStatus`.
    """
    account_status_id_completion: Int64Bit
    """
    If this is set, any `Job` using this `JobType` that is completed
    unsuccessfully while associated with an `Account` will change the `Account`
    to this `AccountStatus`.
    """
    account_status_id_failure: Int64Bit
    """Completion ticket action."""
    action_on_completion: JobTypeAction
    """Failure ticket action."""
    action_on_failure: JobTypeAction
    """Whether or not this `JobType` is valid for all `Companies`."""
    all_companies: Boolean
    """
    Whether `Job`s associated with this `JobType` should be able to be completed with incomplete tasks.
    """
    allow_completion_with_incomplete_tasks: Boolean
    """Color."""
    color: HtmlHexColor
    """The ID of a `ContractTemplate`."""
    contract_template_id: Int64Bit
    """The default length for a `Job` created using this `JobType`."""
    default_length_in_minutes: Int
    """
    If this is set, any `Job` using this `JobType` that is completed
    successfully while associated with an `Account` will trigger the
    disconnection of the `Account`.
    """
    disconnects_account: Boolean
    """Whether or not this is enabled."""
    enabled: Boolean
    """An icon."""
    icon: Icon
    """A descriptive name."""
    name: String
    """The ID of a `TaskTemplate`."""
    task_template_id: Int64Bit
    """
    If this is set, any `Job` using this `JobType` that is completed
    successfully will create a `Ticket` and assign it to this `TicketGroup`.
    """
    ticket_group_id_completion: Int64Bit
    """
    If this is set, any `Job` using this `JobType` that is completed
    unsuccessfully will create a `Ticket` and assign it to this `TicketGroup`.
    """
    ticket_group_id_failure: Int64Bit
    """Ticket status on completion."""
    ticket_status_on_completion: TicketStatus
    """Ticket status on failure."""
    ticket_status_on_failure: TicketStatus
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): JobTypeConnection!
  """Jobs."""
  jobs(
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
    """The serviceable address where this job was completed."""
    address_on_completion: String
    """Whether or not this is complete."""
    complete: Boolean
    """The `User` that completed this."""
    completed_by_user_id: Int64Bit
    """Whether this `Job` was completed successfully or not."""
    completed_successfully: Boolean
    """The date and time this `Job` was completed."""
    completion_datetime: Datetime
    """Any notes entered when this `Job` was completed."""
    completion_notes: Text
    """The ID of a `JobType`."""
    job_type_id: Int64Bit
    """The ID of the entity that this `Job` is associated with."""
    jobbable_id: Int64Bit
    """The type of entity that this `Job` is associated with."""
    jobbable_type: JobbableType
    """The length in minutes for this `Job`."""
    length_in_minutes: Int
    """The date and time this `Job` is scheduled for."""
    scheduled_datetime: Datetime
    """The ID of the serviceable address account assignment future."""
    serviceable_address_account_assignment_future_id: Int64Bit
    """
    Indicates this entity has skipped the validations which would normally apply.
    """
    skips_validation: Boolean
    """The ID of a `Ticket`."""
    ticket_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): JobConnection!
  """Local prefixes for voice services."""
  local_prefixes(
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
    """A telephone number prefix."""
    prefix: Numeric
    """The ID of the `VoiceServiceDetail`."""
    voice_service_detail_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): LocalPrefixConnection!
  """Log entries for various events throughout Sonar."""
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
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
  """Report builder licenses."""
  looker_explore_licenses(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): LookerExploreLicenseConnection!
  """Report viewer licenses."""
  looker_view_licenses(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): LookerViewLicenseConnection!
  """The credentials for an LTE provider."""
  lte_provider_credentials(
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
    """The credential name."""
    credential: LteProviderAuthenticationCredential
    """The ID of an `LteProvider`."""
    lte_provider_id: Int64Bit
    """The value."""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): LteProviderCredentialConnection!
  """LTE providers."""
  lte_providers(
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
    """Automatically detach UE when account is changed to delinquency status."""
    deactivate_on_delinquency: Boolean
    """Whether or not this is enabled."""
    enabled: Boolean
    """Whether or not a floating license model is used with BreezeVIEW."""
    floating_license: Boolean
    """The date and time this device was last synchronized."""
    last_synchronized: Datetime
    """A descriptive name."""
    name: String
    """The status."""
    status: ProvisioningDeviceStatus
    """A message describing what caused the current status of this device."""
    status_message: String
    """Whether or not a synchronization request is queued."""
    synchronization_queued: Boolean
    """The date/time that synchronization started."""
    synchronization_start: Datetime
    """The type."""
    type: LteProviderType
    """Write PDN address allocation into BreezeVIEW."""
    write_pdn_address_allocation: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): LteProviderConnection!
  """Manufacturers."""
  manufacturers(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ManufacturerConnection!
  """Map Overlays."""
  map_overlays(
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
    """Map Overlay Language (KML) file contents."""
    contents: String
    """file type"""
    file_type: MapOverlayFileType
    """A decimal latitude."""
    latitude: Latitude
    """A decimal longitude."""
    longitude: Longitude
    """A descriptive name."""
    name: String
    """Network site id."""
    network_site_id: Int64Bit
    """Radius in KM."""
    radius: Float
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): MapOverlayConnection!
  """
  Returns all map overlays within a camera view represented by the north, south, east and west arguments
  """
  map_overlays_within_box(
    """North"""
    north: Float!
    """East"""
    east: Float!
    """South"""
    south: Float!
    """West"""
    west: Float!
  ): MapOverlayConnection!
  """Mass email communications."""
  mass_emails(
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
    The email address to send from when using this email message. If `null`, then the system default will be used.
    """
    from_email_address: EmailAddress
    """
    The name to send from when using this email message. If `null`, then the system default will be used.
    """
    from_name: String
    """
    A short sentence that will be shown as a preview in compatible email clients.
    """
    inbox_preview: String
    """The message."""
    message: Text
    """The subject."""
    subject: String
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): MassEmailConnection!
  """Get information about yourself!"""
  me: Me!
  """
  Message categories are associated with contacts, and define the types of
  messages those contacts receive. The "default" property determines whether or
  not the category is added to newly created contacts by default.
  """
  message_categories(
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
    """Whether or not this entity is a default entry."""
    default: Boolean
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): MessageCategoryConnection!
  """Multi-factor authentication admin settings."""
  mfa_admin_setting: MfaAdminSetting!
  """Logs of when billing ran successfully for an `Account`."""
  monthly_billing_completions(
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
    """A date"""
    date: Date
    """The ID of an `Invoice`."""
    invoice_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): MonthlyBillingCompletionConnection!
  """Get your IP address"""
  my_ip_address: MyIpAddress!
  """Netflow allowed subnets."""
  netflow_allowed_subnets(
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
    """The ID of a `NetflowEndpoint`."""
    netflow_endpoint_id: Int64Bit
    """An IPv4/IPv6 subnet."""
    subnet: SubnetScalar
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): NetflowAllowedSubnetConnection!
  """Netflow endpoints."""
  netflow_endpoints(
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
    """Hostname."""
    hostname: DomainName
    """A descriptive name."""
    name: String
    """A TCP port."""
    port: Port
    """Whitelist mode."""
    whitelist_mode: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): NetflowEndpointConnection!
  """Netflow on premises."""
  netflow_on_premises(
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
    """An IPv4/IPv6 address."""
    ip: IP
    """The file name of the last processed records."""
    last_processed_filename: String
    """The size of the last processed records file."""
    last_processed_size: Int
    """The date and time of the last processed records."""
    last_processed_timestamp: Datetime
    """A descriptive name."""
    name: String
    """A JSON object of tracked statistics."""
    statistics: Text
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): NetflowOnPremiseConnection!
  """Netflow whitelists."""
  netflow_whitelists(
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
    """The ID of a `NetflowEndpoint`."""
    netflow_endpoint_id: Int64Bit
    """An IPv4/IPv6 subnet."""
    subnet: SubnetScalar
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): NetflowWhitelistConnection!
  """Network monitoring graphs."""
  network_monitoring_graphs(
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
    """A descriptive name."""
    name: String
    """The ID of a `NetworkMonitoringTemplate`."""
    network_monitoring_template_id: Int64Bit
    """Stacked"""
    stacked: Boolean
    """The type."""
    type: NetworkMonitoringGraphType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): NetworkMonitoringGraphConnection!
  """Network monitoring templates."""
  network_monitoring_templates(
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
    """Whether or not to collect interface statistics."""
    collect_interface_statistics: Boolean
    """ICMP latency threshold (ms)."""
    icmp_latency_threshold: Int
    """ICMP loss threshold (%)."""
    icmp_loss_threshold: Int
    """Whether or not ICMP monitoring is enabled."""
    icmp_monitoring: Boolean
    """A descriptive name."""
    name: String
    """SNMPv3 auth passphrase"""
    snmp3_auth_passphrase: Text
    """SNMPv3 auth protocol"""
    snmp3_auth_protocol: Snmp3AuthProtocol
    """SNMPv3 context engine ID"""
    snmp3_context_engineid: Text
    """SNMPv3 context name"""
    snmp3_context_name: Text
    """SNMPv3 privacy passphrase"""
    snmp3_priv_passphrase: Text
    """SNMPv3 privacy protocol"""
    snmp3_priv_protocol: Snmp3PrivProtocol
    """SNMPv3 security level"""
    snmp3_sec_level: Snmp3SecurityLevel
    """SNMP community/securityName"""
    snmp_community: Text
    """SNMP version"""
    snmp_version: SnmpVersion
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): NetworkMonitoringTemplateConnection!
  """Network site serviceable address lists."""
  network_site_serviceable_address_lists(
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
    """Network site id."""
    network_site_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): NetworkSiteServiceableAddressListConnection!
  """Network sites."""
  network_sites(
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
    """A geo-point."""
    geopoint: Geopoint
    """Height in meters."""
    height_in_meters: Float
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): NetworkSiteConnection!
  """
  Items sold by vendors that are not convertible to an inventory model (i.e. labor charges).
  """
  non_inventory_items(
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
    """The ID of a GeneralLedgerCode."""
    general_ledger_code_id: Int64Bit
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): NonInventoryItemConnection!
  """Notes."""
  notes(
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
    """The message."""
    message: Text
    """The ID of the entity that owns this note."""
    noteable_id: Int64Bit
    """The type of entity that owns this note."""
    noteable_type: NoteableType
    """The priority of this item."""
    priority: NotePriority
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): NoteConnection!
  """Notifications."""
  notifications(
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
    """Whether this notification is read or unread."""
    is_read: Boolean
    """The ID of the entity that the notification is related to."""
    notifiable_id: Int64Bit
    """The type of entity that the notification is related to."""
    notifiable_type: NotifiableType
    """The type."""
    type: NotificationType
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): NotificationConnection!
  """Order group relationships to users."""
  order_group_users(
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
    Whether a user is authorized to approve purchase orders created in this order group.
    """
    is_approver: Boolean
    """The ID of an order group."""
    order_group_id: Int64Bit
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): OrderGroupUserConnection!
  """Order groups."""
  order_groups(
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
    The threshold at which requesters require approval of their purchase orders.
    """
    automatic_approval_threshold: Int
    """
    Disabled order groups cannot be assigned users or used to create purchase orders.
    """
    enabled: Boolean
    """The name of an order group."""
    name: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): OrderGroupConnection!
  """Details related to an overage service."""
  overage_service_details(
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
    """A value in gigabytes."""
    gigabytes: Int
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): OverageServiceDetailConnection!
  """Services associated with a package."""
  package_services(
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
    """The ID of a `Package`."""
    package_id: Int64Bit
    """The quantity for this service."""
    quantity: Int
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): PackageServiceConnection!
  """Packages."""
  packages(
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
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """Whether or not this is enabled."""
    enabled: Boolean
    """A descriptive name."""
    name: String
    """
    Setting to indicate if services in this package should be rolled up into a package total when this package is displayed.
    """
    rollup_services: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
    """
    An account ID used for filtering packages based on common account groups.
    """
    valid_for_account_id: Int64Bit
  ): PackageConnection!
  """The password policy for users."""
  password_policy: PasswordPolicy!
  """PayPal Credentials."""
  pay_pal_credentials(
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
    """The client ID for PayPal."""
    client_id: String
    """The client secret for PayPal."""
    client_secret: String
    """Whether or not this is enabled."""
    enabled: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): PayPalCredentialConnection!
  """Payments."""
  payments(
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
    """The amount of the payment, in the smallest currency value."""
    amount: Int
    """The amount remaining that can be used."""
    amount_remaining: Int
    """The ID of a BankAccount."""
    bank_account_id: Int64Bit
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
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
    payment_datetime: Datetime
    """The unique tracking ID for this payment."""
    payment_tracker_id: String
    """The type of payment (e.g. cash, credit card.)"""
    payment_type: PaymentType
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
    successful: Boolean
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): PaymentConnection!
  """Your personal access tokens."""
  personal_access_tokens: PersonalAccessTokenConnection!
  """Types of phone numbers (e.g. mobile, home, fax.)"""
  phone_number_types(
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
    """A descriptive name."""
    name: String
    """
    Whether or not phone numbers of this type are capable of sending and receiving SMS messages.
    """
    sms_capable: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): PhoneNumberTypeConnection!
  """Phone numbers."""
  phone_numbers(
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
    """The ID of the contact that owns this."""
    contact_id: Int64Bit
    """A two character country code for this phone number."""
    country: Country
    """The extension."""
    extension: Numeric
    """The number."""
    number: Numeric
    """A phone number formatted for human readability."""
    number_formatted: String
    """The ID of the PhoneNumberType associated with this phone number."""
    phone_number_type_id: Int64Bit
    """Whether or not SMS messages accepted."""
    sms_opt_in: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): PhoneNumberConnection!
  """Poller settings."""
  poller_setting: PollerSetting!
  """Pollers."""
  pollers(
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
    """An API key."""
    api_key: String
    """Whether or not this is enabled."""
    enabled: Boolean
    """The amount of time it took to poll ICMP status."""
    icmp_time_taken: Int
    """A descriptive name."""
    name: String
    """When the results were last received."""
    results_last_received: Datetime
    """The amount of time it took to poll SNMP status."""
    snmp_time_taken: Int
    """The UTC timestamp for the last time accounts were polled."""
    time_of_last_account_poll: Datetime
    """The UTC timestamp for the last time infrastructure was polled."""
    time_of_last_infrastructure_poll: Datetime
    """Version."""
    version: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): PollerConnection!
  """Preseem integration."""
  preseem: Preseem!
  """Print to mail batches."""
  print_to_mail_batches(
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
    """How the invoices for the batch were generated."""
    batch_type: PrintToMailBatchType
    """
    The completion date of the billing run if the batch type is 'BILLING_RUN'.
    """
    billing_completion_date: Date
    """The cost associated with the print to mail batch."""
    cost: Int
    """The print method for the print to mail batch."""
    print_method: PrintToMailPrintMethod
    """The print type for the print to mail batch."""
    print_type: PrintToMailPrintType
    """The current status of the print to mail batch."""
    status: PrintToMailBatchStatus
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): PrintToMailBatchConnection!
  """Estimated print to mail document/invoice cost."""
  print_to_mail_document_cost_estimate(
    """The print method for the print to mail batch."""
    print_method: PrintToMailPrintMethod!
    """The print type for the print to mail batch."""
    print_type: PrintToMailPrintType!
    """The number of digital pages in the document/invoice."""
    number_of_digital_pages: Int!
  ): PrintToMailDocumentCostEstimate!
  """Print to mail order errors."""
  print_to_mail_order_errors(
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
    """An error message associated with a print to mail order."""
    error_message: String
    """The error type."""
    error_type: PrintToMailOrderErrorType
    """The ID of the invoice that has the error."""
    invoice_id: Int64Bit
    """The print to mail order ID."""
    print_to_mail_order_id: Int64Bit
    """Whether or not the error has been marked as resolved."""
    resolved: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): PrintToMailOrderErrorConnection!
  """Print to mail orders."""
  print_to_mail_orders(
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
    """The last time the order status was checked."""
    last_status_check: Datetime
    """The name of the print to mail order."""
    name: String
    """The print to mail batch ID."""
    print_to_mail_batch_id: Int64Bit
    """The provider ID."""
    provider_order_id: String
    """The current status of the print to mail order."""
    status: PrintToMailOrderStatus
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): PrintToMailOrderConnection!
  """Print to mail settings."""
  print_to_mail_setting: PrintToMailSetting!
  """Printed invoice batches."""
  printed_invoice_batches(
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
    """A date"""
    date: Date
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): PrintedInvoiceBatchConnection!
  """Purchase order line items."""
  purchase_order_items(
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
    The tax transaction that was created for this purchase order item the last time it was modified.
    """
    calculated_tax: Int
    """
    The quantity of a generic purchase order item that has already been received.
    """
    generic_quantity_received: Int
    """The order this item is shown in a list."""
    list_order: Int
    """A descriptive name."""
    name: String
    """Part number used by the vendor to identify this vendor item."""
    part_number: String
    """
    The price of the vendor item at the time the purchase order was created.
    """
    price: Int64Bit
    """The ID of a purchase order."""
    purchase_order_id: Int64Bit
    """
    Number of inventory models that are included in a single unit of this vendors product.
    """
    quantity_per_unit: Int
    """The current status of a purchase order item."""
    status: PurchaseOrderItemStatus
    """The quantity of a vendor item on a purchase order."""
    units: Int
    """The ID of a vendor item."""
    vendor_item_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): PurchaseOrderItemConnection!
  """Purchase orders."""
  purchase_orders(
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
    """The ID of the user that approved this purchase order."""
    approved_by_user_id: Int64Bit
    """The date/time that this purchase order was cancelled."""
    canceled_at: Datetime
    """The ID of the user that cancelled this purchase order."""
    canceled_by_user_id: Int64Bit
    """
    The ID of the company that will be used in the header of this purchase order.
    """
    company_id: Int64Bit
    """The ID of the user that created this purchase order."""
    created_by_user_id: Int64Bit
    """The currency the system displays money in."""
    currency: Currency
    """A message to be included on purchase orders when sent to vendors."""
    external_message: String
    """The source of the shipping address for a purchase order."""
    inventory_location_id: Int64Bit
    """Whether or not the purchase order has been marked as being paid."""
    is_paid: Boolean
    """The date and time that the inventory item status last changed."""
    last_status_change: Datetime
    """The ID of an order group related to this purchase order."""
    order_group_id: Int64Bit
    """A unique number identifying an approved purchase order."""
    order_number: Int
    """The terms of payment for deliveries from this vendor."""
    payment_terms: PaymentTerm
    """The current status of this purchase order."""
    status: PurchaseOrderStatus
    """The ID of a vendor."""
    vendor_id: Int64Bit
    """The name of a vendor."""
    vendor_name: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): PurchaseOrderConnection!
  """RADIUS accounts."""
  radius_accounts(
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
    """A password."""
    password: Text
    """A username, used for authentication."""
    username: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): RadiusAccountConnection!
  """RADIUS group reply attributes."""
  radius_group_reply_attributes(
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
    """A descriptive name."""
    name: String
    """A RADIUS reply operator."""
    operator: RadiusReplyOperator
    """The ID of a `RadiusGroup`."""
    radius_group_id: Int64Bit
    """A RADIUS reply."""
    reply: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): RadiusGroupReplyAttributeConnection!
  """RADIUS groups."""
  radius_groups(
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
    The types of account statuses for accounts that are part of this grouping.
    """
    account_status: AddressListAccountStatus
    """The delinquency state for accounts that are part of this grouping."""
    delinquency: AddressListDelinquency
    """Whether or not this is a fall through group."""
    fall_through: Boolean
    """A descriptive name."""
    name: String
    """The RADIUS priority."""
    priority: Int
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): RadiusGroupConnection!
  """Radius server credentials."""
  radius_server_credentials(
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
    """The credential name."""
    credential: RadiusServerAuthCredential
    """The ID of a `RadiusServer`."""
    radius_server_id: Int64Bit
    """The value."""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): RadiusServerCredentialConnection!
  """RADIUS servers."""
  radius_servers(
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
    """The secret used to send a change of authorization to this device."""
    coa_secret: String
    """
    Whether or not Sonar should track bandwidth usage data from this RADIUS server.
    """
    collect_bandwidth: Boolean
    """Whether or not this is enabled."""
    enabled: Boolean
    """An IPv4/IPv6 address."""
    ip_address: IP
    """The date and time this device was last synchronized."""
    last_synchronized: Datetime
    """A descriptive name."""
    name: String
    """Send a change of authorization on account delinquency to this device."""
    send_change_auth_on_delinquency: Boolean
    """
    Send a change of authorization on account service change to this device.
    """
    send_change_auth_on_service_change: Boolean
    """
    Send a change of authorization on account status change to this device.
    """
    send_change_auth_on_status_change: Boolean
    """The status."""
    status: ProvisioningDeviceStatus
    """A message describing what caused the current status of this device."""
    status_message: String
    """Whether or not a synchronization request is queued."""
    synchronization_queued: Boolean
    """The date/time that synchronization started."""
    synchronization_start: Datetime
    """The type."""
    type: RadiusServerType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): RadiusServerConnection!
  """RADIUS session histories."""
  radius_session_histories(
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
    """Account session ID."""
    account_session_id: String
    """Called station ID."""
    called_station_id: String
    """Calling station ID."""
    calling_station_id: String
    """The time that a disconnect was requested."""
    disconnect_requested: Datetime
    """The end."""
    end: Datetime
    """An IPv4/IPv6 address."""
    ip_address: IP
    """The IP address of the NAS."""
    nas_ip_address: IP
    """The ID of a `RadiusAccount`."""
    radius_account_id: Int64Bit
    """The real session ID."""
    real_session_id: String
    """The start."""
    start: Datetime
    """The reason for the session termination."""
    terminate_reason: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): RadiusSessionHistoryConnection!
  """Rate Centers."""
  rate_centers(
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
    """Whether or not this entity is a default entry."""
    default: Boolean
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): RateCenterConnection!
  """Details related to a recurring service."""
  recurring_service_details(
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
    """How often this service bills, in months."""
    billing_frequency: Int
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): RecurringServiceDetailConnection!
  """Refunded payments."""
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
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
  """Attempt to translate a latitude and longitude into a street address."""
  reverse_geocode(
    """A decimal latitude."""
    latitude: Latitude
    """A decimal latitude."""
    longitude: Longitude
  ): ValidatedAddress!
  """Reversed payments."""
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
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
  """Roles for users. Roles define the permission set that a user can have."""
  roles(
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
    """A list of permissions associated with this role."""
    applied_permissions: [Permission]
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): RoleConnection!
  """Saved message categories."""
  saved_message_categories(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SavedMessageCategoryConnection!
  """Scheduling data."""
  schedule(
    """A date"""
    date: Date!
  ): ScheduleResult
  """Starting and ending addresses for technician schedules."""
  schedule_addresses(
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
    """A city."""
    city: String
    """A two character country code."""
    country: Country
    """A decimal latitude."""
    latitude: Latitude
    """Address line 1."""
    line1: String
    """Address line 2."""
    line2: String
    """A decimal longitude."""
    longitude: Longitude
    """A descriptive name."""
    name: String
    """A state, province, or other country subdivision."""
    subdivision: Subdivision
    """The timezone you want times in the system displayed in."""
    timezone: Timezone
    """The type."""
    type: ScheduleAddressType
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ScheduleAddressConnection!
  """Schedule availabilities."""
  schedule_availabilities(
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
    Whether this `ScheduleAvailability` creates available time, or blocks available time.
    """
    available: Boolean
    """The ID of a `Geofence`."""
    geofence_id: Int64Bit
    """Whether this repeats forever or not."""
    infinite_repetitions: Boolean
    """A descriptive name."""
    name: String
    """The number of times this repeats."""
    repetitions: Int
    """The start date for this `ScheduleAvailability`."""
    start_date: Date
    """The number of weeks between repetitions."""
    weeks_between_repetitions: Int
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ScheduleAvailabilityConnection!
  """Schedule availability day/times."""
  schedule_availability_day_times(
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
    """Whether this day is available from start to finish."""
    all_day: Boolean
    """A day."""
    day: Day
    """The end time for the day."""
    end_time: Time
    """The ID of a `ScheduleAvailability`."""
    schedule_availability_id: Int64Bit
    """The start time for the day."""
    start_time: Time
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ScheduleAvailabilityDayTimeConnection!
  """Schedule blocker day/times."""
  schedule_blocker_day_times(
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
    """A day."""
    day: Day
    """The end time for the day."""
    end_time: Time
    """The ID of a `ScheduleBlocker`."""
    schedule_blocker_id: Int64Bit
    """The start time for the day."""
    start_time: Time
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ScheduleBlockerDayTimeConnection!
  """Schedule blocker overrides."""
  schedule_blocker_overrides(
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
    """The ID of a `ScheduleBlocker`."""
    schedule_blocker_id: Int64Bit
    """The date and time that this starts."""
    start_datetime: Datetime
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ScheduleBlockerOverrideConnection!
  """Schedule blockers."""
  schedule_blockers(
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
    """Whether this repeats forever or not."""
    infinite_repetitions: Boolean
    """A descriptive name."""
    name: String
    """The number of times this repeats."""
    repetitions: Int
    """The start date for this `ScheduleAvailability`."""
    start_date: Date
    """The number of weeks between repetitions."""
    weeks_between_repetitions: Int
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ScheduleBlockerConnection!
  """Schedule time offs."""
  schedule_time_offs(
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
    """The date and time that this ends."""
    end_datetime: Datetime
    """A descriptive name."""
    name: String
    """The date and time that this starts."""
    start_datetime: Datetime
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ScheduleTimeOffConnection!
  """Scheduled event account Calix service details."""
  scheduled_event_account_calix_service_details(
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
    """Calix Inegartion ID."""
    calix_integration_id: Int64Bit
    """Custom JSON."""
    custom_json: String
    """C-VLAN."""
    cvlan: Int
    """Global VLAN."""
    global_vlan: String
    """ONT Port ID."""
    ont_port_id: String
    """Policy Map."""
    policy_map: String
    """The ID of a `ScheduledEvent`"""
    scheduled_event_id: Int64Bit
    """Use Custom JSON."""
    use_custom_json: Boolean
    """VLAN."""
    vlan: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ScheduledEventAccountCalixServiceDetailConnection!
  """Scheduled event account voice service details."""
  scheduled_event_account_voice_service_details(
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
    The amount that this service price has been overridden to. If this is null, then the service price is used.
    """
    price_override: Int
    """The reason that the price of a service has been overridden."""
    price_override_reason: String
    """The quantity for this service."""
    quantity: Int
    """The ID of a `ScheduledEvent`"""
    scheduled_event_id: Int64Bit
    """The ID of a voice service configuration parameter."""
    voice_service_generic_parameter_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ScheduledEventAccountVoiceServiceDetailConnection!
  """Scheduled events."""
  scheduled_events(
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
    """Whether or not this is complete."""
    complete: Boolean
    """The date and time in UTC."""
    datetime: Datetime
    """A human readable description."""
    description: String
    """An event."""
    event: ScheduledEventEvent
    """The ID of an object described by the `event` field."""
    primary_event_object_id: String
    """Whether or not to prorate the transaction."""
    prorate: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ScheduledEventConnection!
  """User-defined search filters."""
  search_filters(
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
    """Whether the filter is available to every user (admins only)."""
    all_users: Boolean
    """The type of entity this filter belongs to."""
    entity_type: String
    """The actual filter, as JSON."""
    filter: Text
    """The filter's name."""
    name: String
    """The ID of the user that created this entity."""
    user_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SearchFilterConnection!
  """Metadata fields on a service."""
  service_metadata(
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
    """A descriptive name."""
    name: String
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ServiceMetadataConnection!
  """Values entered into service metadata fields."""
  service_metadata_values(
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
    """The ID of an AccountService."""
    account_service_id: Int64Bit
    """The ID of a ServiceMetadata field."""
    service_metadata_id: Int64Bit
    """The value."""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ServiceMetadataValueConnection!
  """Tax definitions that have been assigned to services."""
  service_tax_definitions(
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
    """Whether this tax definition is for a discount or not."""
    discount: Boolean
    """The ID of a Service."""
    service_id: Int64Bit
    """The ID of entity this tax definition is related to."""
    taxdefinitionable_id: Int64Bit
    """The type of entity this tax definition is related to."""
    taxdefinitionable_type: TaxdefinitionableType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ServiceTaxDefinitionConnection!
  """The relationship between a service and a tax."""
  service_taxes(
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
    The amount of the service that is exempt from taxation in the smallest currency value (e.g. cents, pence, pesos.)
    """
    exemption_amount: Int
    """The ID of a Service."""
    service_id: Int64Bit
    """The ID of a Tax."""
    tax_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ServiceTaxConnection!
  """Serviceable address account assignment futures."""
  serviceable_address_account_assignment_futures(
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
    """The ID of the address."""
    address_id: Int64Bit
    """
    A note about this expected change of serviceable address account assignment.
    """
    note: Text
    """The date this is targeted to happen."""
    target_date: Date
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ServiceableAddressAccountAssignmentFutureConnection!
  """Serviceable address account assignment histories."""
  serviceable_address_account_assignment_histories(
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
    """The ID of the address."""
    address_id: Int64Bit
    """The date that this ends."""
    end_date: Date
    """The start date for this `ScheduleAvailability`."""
    start_date: Date
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ServiceableAddressAccountAssignmentHistoryConnection!
  """Services."""
  services(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): ServiceConnection!
  """Signatures."""
  signatures(
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
    """The ID of a department."""
    department_id: Int64Bit
    """Whether or not signature is default for mass messages."""
    mass_default: Boolean
    """A descriptive name."""
    name: String
    """Body of an SMS signature."""
    sms_signature: SmsContactPrefix
    """Whether or not signature is default for triggered messages."""
    triggered_default: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SignatureConnection!
  """SMS message contents."""
  sms_message_contents(
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
    """A supported language."""
    language: Language
    """SMS message body for customers without portal."""
    non_portal_body: String
    """SMS message body for customers with portal."""
    portal_body: String
    """The ID of the SMS message."""
    sms_message_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SmsMessageContentConnection!
  """SMS Messages."""
  sms_messages(
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
    """Whether or not SMS message is used for triggers."""
    is_trigger: Boolean
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SmsMessageConnection!
  """SMS outbound messages."""
  sms_outbound_messages(
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
    """The category of the message."""
    category: SmsOutboundCategory
    """
    The cost associated with the SMS message. Stored as one hundredth of the
    smallest currency value (e.g. cents, pence, pesos.)
    """
    cost_in_hundredths: Int
    """The country code of the destination mobile phone number."""
    destination_country: String
    """The error message."""
    error_message: String
    """The provider message ID."""
    last_status_check: Datetime
    """The message text."""
    message_text: String
    """The destination mobile phone number."""
    mobile_number: String
    """The provider message ID."""
    provider_message_id: String
    """The number of segments needed to deliver message text."""
    segments: Int
    """The ID of the entity that this SMS was sent to."""
    smsable_id: Int64Bit
    """The type of entity that this SMS was sent to."""
    smsable_type: SmsableType
    """The current status of the message."""
    status: SmsOutboundStatus
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SmsOutboundMessageConnection!
  """SMS settings."""
  sms_setting: SmsSetting!
  """All SMTP events for each sent email."""
  smtp_events(
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
    The remote IP address of the server Mandrill was connected to for message relay when attempting to send an email.
    """
    destination_ip: IP
    """The ID of an email."""
    email_id: Int64Bit
    """The date and time of an event sent from Mandrill"""
    event_datetime: Datetime
    """The message of the SMTP response."""
    response: String
    """The size of a SMTP message that Mandrill attempted to relay."""
    size: Int64Bit
    """The IP address of the Mandrill server that attempted to send an email."""
    source_ip: IP
    """The type."""
    type: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SmtpEventConnection!
  """SNMP interface numeric results"""
  snmp_interface_numeric_results(
    """The date and time that this starts."""
    start_datetime: Datetime
    """The date and time that this ends."""
    end_datetime: Datetime
    """The time."""
    time: Datetime
    """The ID of an `InventoryItem`."""
    inventory_item_id: Int64Bit!
  ): [SnmpInterfaceNumericResult]!
  """SNMP OID threshold violations."""
  snmp_oid_threshold_violations(
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
    """The ID of an `InventoryItem`."""
    inventory_item_id: Int64Bit
    """The ID of an `SnmpOidThreshold`."""
    snmp_oid_threshold_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SnmpOidThresholdViolationConnection!
  """SNMP OID thresholds."""
  snmp_oid_thresholds(
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
    """An operator."""
    operator: RangeOperator
    """The ID of an `SnmpOid`."""
    snmp_oid_id: Int64Bit
    """
    The amount of time in minutes that the threshold must be violated before it is triggered.
    """
    time_period_in_minutes: Int
    """The value."""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SnmpOidThresholdConnection!
  """SNMP OIDs."""
  snmp_oids(
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
    """Whether or not to auto scale."""
    auto_scale: Boolean
    """Color."""
    color: HtmlHexColor
    """Display as table"""
    display_as_table: Boolean
    """Divide by"""
    divide_by: Int
    """A descriptive name."""
    name: String
    """The ID of a `NetworkMonitoringGraph`."""
    network_monitoring_graph_id: Int64Bit
    """An OID"""
    oid: String
    """Unit of measurement"""
    unit_of_measurement: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SnmpOidConnection!
  """SNMP Overrides."""
  snmp_overrides(
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
    """Whether or not this is enabled."""
    enabled: Boolean
    """The ID of an `InventoryItem`."""
    inventory_item_id: Int64Bit
    """SNMPv3 auth passphrase"""
    snmp3_auth_passphrase: Text
    """SNMPv3 auth protocol"""
    snmp3_auth_protocol: Snmp3AuthProtocol
    """SNMPv3 context engine ID"""
    snmp3_context_engineid: Text
    """SNMPv3 context name"""
    snmp3_context_name: Text
    """SNMPv3 privacy passphrase"""
    snmp3_priv_passphrase: Text
    """SNMPv3 privacy protocol"""
    snmp3_priv_protocol: Snmp3PrivProtocol
    """SNMPv3 security level"""
    snmp3_sec_level: Snmp3SecurityLevel
    """SNMP community/securityName"""
    snmp_community: Text
    """SNMP version"""
    snmp_version: SnmpVersion
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SnmpOverrideConnection!
  """SNMP results."""
  snmp_results(
    """The date and time that this starts."""
    start_datetime: Datetime
    """The date and time that this ends."""
    end_datetime: Datetime
    """The ID of an `InventoryItem`."""
    inventory_item_id: Int64Bit!
    """The number of buckets into which the results will be grouped"""
    buckets: Int64Bit
  ): SnmpNetworkMonitoringResultConnection!
  """Vetro FiberMap Splice Report."""
  splice_report(
    """The ID of the address."""
    id: Int64Bit
  ): SpliceReport!
  """Stored view filters."""
  stored_filters(
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
    """The field that is being filtered."""
    field: String
    """The operator being applied."""
    operator: StoredFilterOperator
    """The order in which the filter is applied."""
    order: Int
    """The ID of a StoredGroup entity."""
    stored_group_id: Int64Bit
    """The value being filtered against."""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): StoredFilterConnection!
  """Stored view groups."""
  stored_groups(
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
    """The ID of a `StoredView` entity."""
    stored_view_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): StoredGroupConnection!
  """Stored views associated with users."""
  stored_view_users(
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
    """The location in the UI that this view is available."""
    location: String
    """The ID of a `StoredView` entity."""
    stored_view_id: Int64Bit
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): StoredViewUserConnection!
  """Stored views."""
  stored_views(
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
    """The ID of the user that created this entity."""
    created_by_user_id: Int64Bit
    """Whether or not this StoredView is available to all users."""
    is_global: Boolean
    """The location in the UI that this view is available."""
    location: String
    """A name to identify this `StoredView`."""
    name: String
    """The column used to sort the filtered results."""
    sort_column: String
    """The direction to sort in."""
    sort_direction: SortDirection
    """The type of `StoredView`."""
    type: StoredViewType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): StoredViewConnection!
  """Subnets."""
  subnets(
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
    """The largest subnet available, as a CIDR mask."""
    largest_cidr_available: Int
    """A descriptive name."""
    name: String
    """The ID of a `Poller`."""
    poller_id: Int64Bit
    """Polling priority."""
    polling_priority: Int
    """An IPv4/IPv6 subnet."""
    subnet: SubnetScalar
    """The ID of a `Supernet`."""
    supernet_id: Int64Bit
    """The type."""
    type: SubnetType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SubnetConnection!
  """Subscriptions."""
  subscriptions(
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
    When suspended, the subscription will not send notifications. Permission
    changes and other actions may cause a subscription to become suspended.
    """
    is_suspended: Boolean
    """The id of the entity that is being subscribed to."""
    subscribable_id: Int64Bit
    """The type of entity that is being subscribed to."""
    subscribable_type: SubscribableType
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SubscriptionConnection!
  """Supernets."""
  supernets(
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
    """The largest subnet available, as a CIDR mask."""
    largest_cidr_available: Int
    """A descriptive name."""
    name: String
    """An IPv4/IPv6 subnet."""
    subnet: SubnetScalar
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SupernetConnection!
  """The configured credentials for a system backup export destination."""
  system_backup_destination_credentials(
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
    """The credential name."""
    credential: SystemBackupDestinationProviderCredential
    """The ID of a destination that a system backup can be exported to."""
    system_backup_destination_id: Int64Bit
    """The value."""
    value: Text
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SystemBackupDestinationCredentialConnection!
  """All configured destinations to export system backups to."""
  system_backup_destinations(
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
    """The base path to the directory that the file will be stored in."""
    base_path: Text
    """Whether or not this is enabled."""
    enabled: Boolean
    """When last system backup export was attempted."""
    last_export_at: Datetime
    """The status of the last system backup export."""
    last_export_status: SystemBackupExportStatus
    """The service that a system backup will be exported to."""
    provider: SystemBackupDestinationProvider
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SystemBackupDestinationConnection!
  """A history of all system backup export attempts."""
  system_backup_exports(
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
    """Indicates that this entity has been deleted as part of a pruning."""
    pruned: Boolean
    """The message of the SMTP response."""
    response: Text
    """The status."""
    status: SystemBackupExportStatus
    """The ID of a destination that a system backup can be exported to."""
    system_backup_destination_id: Int64Bit
    """The ID of a system backup."""
    system_backup_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SystemBackupExportConnection!
  """System backup settings."""
  system_backup_setting: SystemBackupSetting!
  """Your system backups."""
  system_backups(
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
    """A descriptive name."""
    name: String
    """A password."""
    password: Text
    """The status."""
    status: SystemBackupStatus
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SystemBackupConnection!
  """System environment."""
  system_environment: SystemEnvironment!
  """System settings."""
  system_setting: SystemSetting!
  """Task template items."""
  task_template_items(
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
    """The ID of the entity that completes or completed this task."""
    completable_id: Int64Bit
    """The type of entity that completes this task."""
    completable_type: CompletableType
    """How this task gets marked as completed."""
    completion_type: TaskCompletionType
    """The order this item is shown in a list."""
    list_order: Int
    """The task to be performed."""
    task: String
    """The ID of a `TaskTemplate`."""
    task_template_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TaskTemplateItemConnection!
  """Task templates."""
  task_templates(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TaskTemplateConnection!
  """Tasks."""
  tasks(
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
    """The ID of the entity that completes or completed this task."""
    completable_id: Int64Bit
    """The type of entity that completes this task."""
    completable_type: CompletableType
    """Whether or not this is complete."""
    complete: Boolean
    """The date and time this was completed."""
    completed_at: Datetime
    """The `User` that completed this."""
    completed_by_user_id: Int64Bit
    """How this task gets marked as completed."""
    completion_type: TaskCompletionType
    """The date on which the task is due."""
    due: Date
    """The order this item is shown in a list."""
    list_order: Int
    """The task to be performed."""
    task: Text
    """The ID of the entity that the task is associated with."""
    taskable_id: Int64Bit
    """The entity that the task is associated with."""
    taskable_type: TaskableType
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TaskConnection!
  """Tax exemptions."""
  tax_exemptions(
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
    """The jurisdictions of this `TaxExemption`."""
    jurisdictions: [TaxJurisdiction]
    """A descriptive name."""
    name: String
    """The ID of an `TaxProvider`."""
    tax_provider_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TaxExemptionConnection!
  """Overrides of specific taxes on a per account basis."""
  tax_overrides(
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
    """The rate."""
    rate: Float
    """The ID of a Tax."""
    tax_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TaxOverrideConnection!
  """The credentials for a tax provider."""
  tax_provider_credentials(
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
    """The credential name."""
    credential: TaxProviderCredentialType
    """The ID of an `TaxProvider`."""
    tax_provider_id: Int64Bit
    """The value."""
    value: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TaxProviderCredentialConnection!
  """Tax providers."""
  tax_providers(
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
    """Whether or not this is enabled."""
    enabled: Boolean
    """A descriptive name."""
    name: String
    """The list of subdivisions where this tax provider will collect taxes."""
    subdivisions: [Subdivision]
    """The type."""
    type: TaxProviderType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TaxProviderConnection!
  """Tax transactions."""
  tax_transactions(
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
    """The amount of this `Debit` that was taxed."""
    amount_taxed: Int
    """A human readable description."""
    description: Text
    """The ID of an `TaxProvider`."""
    tax_provider_id: Int64Bit
    """The ID of entity this tax definition is related to."""
    taxdefinitionable_id: Int64Bit
    """The type of entity this tax definition is related to."""
    taxdefinitionable_type: TaxdefinitionableType
    """The ID of the entity this tax transaction is related to."""
    taxtransactionable_id: Int64Bit
    """The type of entity this tax transaction is related to."""
    taxtransactionable_type: TaxtransactionableType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TaxTransactionConnection!
  """Taxes."""
  taxes(
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
    Whether this `Tax` is applied as a percentage of the `Service` charge, or as a flat rate.
    """
    application: TaxApplication
    """A descriptive name."""
    name: String
    """
    The rate for a tax. For a percentage based tax, this is a percentage. For a
    flat tax, it is a currency value in the smallest currency unit (e.g. cents, pence, pesos.)
    """
    rate: Float
    """
    Whether this tax is applied based on the account being in a specific
    geography, or whether it is applied to all accounts.
    """
    type: TaxType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TaxConnection!
  """Ticket categories."""
  ticket_categories(
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
    """Whether or not this is enabled."""
    enabled: Boolean
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TicketCategoryConnection!
  """Ticket comments."""
  ticket_comments(
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
    """The body."""
    body: Text
    """The ID of a `Ticket`."""
    ticket_id: Int64Bit
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TicketCommentConnection!
  """Ticket groups."""
  ticket_groups(
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
    """Whether or not this is enabled."""
    enabled: Boolean
    """A descriptive name."""
    name: String
    """
    If a group is private, only members of the group can view emails within it.
    """
    private: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TicketGroupConnection!
  """Ticket recipients."""
  ticket_recipients(
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
    """An email address."""
    email_address: EmailAddress
    """A descriptive name."""
    name: String
    """The ID of a `Ticket`."""
    ticket_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TicketRecipientConnection!
  """Ticket replies."""
  ticket_replies(
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
    """The author."""
    author: String
    """The email address of the author."""
    author_email: EmailAddress
    """The body."""
    body: Text
    """The email headers."""
    headers: Text
    """
    Whether or not the reply was incoming (from an external party) or outgoing (from a Sonar `User`.)
    """
    incoming: Boolean
    """The raw body, before any Sonar parsing."""
    raw_body: Text
    """
    The signature to append. You can include `[PUBLIC_NAME]` as a variable to
    insert the user's public name when the signature is appended.
    """
    signature: Text
    """The ID of a `Ticket`."""
    ticket_id: Int64Bit
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TicketReplyConnection!
  """Ticketing settings."""
  ticketing_setting: TicketingSetting!
  """Tickets."""
  tickets(
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
    The last date and time this entity was updated, or was the subject of a log.
    """
    global_updated_at: Datetime
    """The time this was closed at."""
    closed_at: Datetime
    """The ID of the `User` that closed this."""
    closed_by_user_id: Int64Bit
    """The ID of the company that this entity operates under."""
    company_id: Int64Bit
    """A human readable description."""
    description: Text
    """The date this invoice is due by."""
    due_date: Date
    """The ID of an `InboundMailbox`."""
    inbound_mailbox_id: Int64Bit
    """Indicates if this ticket is marked as spam."""
    is_spam: Boolean
    """The ID of the `Ticket` that this `Ticket` is a child of."""
    parent_ticket_id: Int64Bit
    """The priority of this item."""
    priority: TicketPriority
    """Mail processor's spam rating for whether or not this is spam."""
    spam_score: Float
    """The status."""
    status: TicketStatus
    """The subject."""
    subject: String
    """The ID of a `TicketGroup`."""
    ticket_group_id: Int64Bit
    """The ID of the entity that this `Ticket` is associated with."""
    ticketable_id: Int64Bit
    """The type of entity that this `Ticket` is associated with."""
    ticketable_type: TicketableType
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TicketConnection!
  """TowerCoverage integration."""
  towercoverage_configuration: TowercoverageConfiguration!
  """TowerCoverage submissions."""
  towercoverage_submissions(
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
    """An email address."""
    email_address: EmailAddress
    """The full name."""
    full_name: String
    """is_visible of the information"""
    is_visible: Boolean
    """The message."""
    message: Text
    """A note about this TowerCoverage submission."""
    note: Text
    """A telephone number."""
    phone_number: Numeric
    """The raw XML."""
    raw_xml: Text
    """The time that the TowerCoverage submission was received."""
    received_at: Datetime
    """The ID of the serviceable address to use for this account."""
    serviceable_address_id: Int64Bit
    """Will be true if the operation succeeded."""
    success: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TowercoverageSubmissionConnection!
  """A list of transactions for display on an account."""
  transactions(
    """The ID of an Account."""
    account_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
  ): TransactionConnection!
  """Emails that are sent when specific conditions are met."""
  triggered_emails(
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
    """Whether or not child accounts are allowed."""
    allow_children: Boolean
    """
    The count associated with this `TriggeredEmail`. This is defined by the
    trigger, and could be something like a number of days, months, gigabytes, etc.
    """
    count: Int
    """The ID of an EmailMessage."""
    email_message_id: Int64Bit
    """Whether or not this is enabled."""
    enabled: Boolean
    """The ID of a `JobType`."""
    job_type_id: Int64Bit
    """A descriptive name."""
    name: String
    """If an item is protected, it cannot be modified or deleted."""
    protected: Boolean
    """The trigger for this message."""
    trigger: EmailTrigger
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TriggeredEmailConnection!
  """Messages that are sent when specific conditions are met."""
  triggered_messages(
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
    """Whether or not child accounts are allowed."""
    allow_children: Boolean
    """
    The count associated with this `TriggeredMessage`. This is defined by the
    trigger, and could be something like a number of days, months, gigabytes, etc.
    """
    count: Int
    """The ID of an EmailMessage."""
    email_message_id: Int64Bit
    """Whether or not this is enabled."""
    enabled: Boolean
    """The ID of a `JobType`."""
    job_type_id: Int64Bit
    """A descriptive name."""
    name: String
    """If an item is protected, it cannot be modified or deleted."""
    protected: Boolean
    """The ID of a signature."""
    signature_id: Int64Bit
    """The ID of the SMS message."""
    sms_message_id: Int64Bit
    """The trigger for this message."""
    trigger: MessageTrigger
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): TriggeredMessageConnection!
  """Uninventoried MAC addresses."""
  uninventoried_mac_addresses(
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
    """A MAC address."""
    mac_address: MacAddress
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): UninventoriedMacAddressConnection!
  """Usage based billing policies."""
  usage_based_billing_policies(
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
    Whether or not a customer can purchase additional data usage capacity during a billing period.
    """
    allow_purchase_of_additional_capacity_during_billing_period: Boolean
    """
    Whether or not to assess charges for usage over the bandwidth limit at the end of the billing period.
    """
    assess_charges_at_end_of_billing_period: Boolean
    """The available data usage in this policy, measured in gigabytes."""
    cap_in_gigabytes: Int
    """A descriptive name."""
    name: String
    """Whether or not rollover is enabled."""
    rollover_enabled: Boolean
    """Whether or not rollover expiration is enabled."""
    rollover_expiration_enabled: Boolean
    """
    Rollover expires after this many months, if rollover expiration is enabled.
    """
    rollover_expiration_months: Int
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): UsageBasedBillingPolicyConnection!
  """Usage based billing policy free periods."""
  usage_based_billing_policy_free_periods(
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
    """A day."""
    day: Day
    """The end."""
    end: Time
    """The start."""
    start: Time
    """The ID of a `UsageBasedBillingPolicy`."""
    usage_based_billing_policy_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): UsageBasedBillingPolicyFreePeriodConnection!
  """Users that can login to Sonar."""
  users(
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
    """Whether or not the user has completed the setup process."""
    completed_setup: Boolean
    """An email address."""
    email_address: EmailAddress
    """Whether or not this is enabled."""
    enabled: Boolean
    """Whether or not this user is a Sonar employee."""
    is_sonar_staff: Boolean
    """A supported language."""
    language: Language
    """A mobile phone number. This will be used to send SMS messages."""
    mobile_number: Numeric
    """A descriptive name."""
    name: String
    """The publicly viewable name of this user."""
    public_name: String
    """The ID of a Role."""
    role_id: Int64Bit
    """
    Super admins receive all system permissions automatically, regardless of their role.
    """
    super_admin: Boolean
    """A username, used for authentication."""
    username: String
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): UserConnection!
  """
  Validate an address. This will attempt to resolve the subdivision, geocode if
  necessary, etc. The more information you input, the more accurate the output
  is likely to be.
  """
  validate_address(
    """Address line 1."""
    line1: String!
    """Address line 2."""
    line2: String
    """A city."""
    city: String
    """A state, province, or other country subdivision."""
    subdivision: String
    """A ZIP or postal code."""
    zip: String
    """A two character country code."""
    country: Country!
    """A decimal latitude."""
    latitude: Latitude
    """A decimal latitude."""
    longitude: Longitude
  ): ValidatedAddress!
  """Validate contact portal credentials."""
  validate_credential(
    """A username, used for authentication."""
    username: String!
    """A password."""
    password: String!
  ): Contact!
  """Vehicle location histories."""
  vehicle_location_histories(
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
    """A decimal latitude."""
    latitude: Latitude
    """A decimal longitude."""
    longitude: Longitude
    """Odometer without unit of measure."""
    odometer: Int
    """Unit of measure for odometer."""
    odometer_um: String
    """Speed without unit of measure."""
    speed: Int
    """Unit of measure for speed."""
    speed_um: String
    """The status."""
    status: String
    """The ID of a `Vehicle`."""
    vehicle_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): VehicleLocationHistoryConnection!
  """Vehicles."""
  vehicles(
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
    """A geo-point."""
    geopoint: Geopoint
    """Whether or not to always track the vehicle."""
    gps_tracking_always: Boolean
    """If not always, then track on Friday."""
    gps_tracking_day_friday: Boolean
    """If not always, then track on Monday."""
    gps_tracking_day_monday: Boolean
    """If not always, then track on Saturday."""
    gps_tracking_day_saturday: Boolean
    """If not always, then track on Sunday."""
    gps_tracking_day_sunday: Boolean
    """If not always, then track on Thursday."""
    gps_tracking_day_thursday: Boolean
    """If not always, then track on Tuesday."""
    gps_tracking_day_tuesday: Boolean
    """If not always, then track on Wednesday."""
    gps_tracking_day_wednesday: Boolean
    """Whether or not GPS Tracking enabled for vehicle."""
    gps_tracking_enabled: Boolean
    """If not always, end time for tracking."""
    gps_tracking_end_time: Time
    """A `GpsTrackingProvider` ID."""
    gps_tracking_provider_id: Int64Bit
    """If not always, start time for tracking."""
    gps_tracking_start_time: Time
    """If not always, timezone for start and end times."""
    gps_tracking_timezone: Timezone
    """A GPS Tracking Provider vehicle unique identifier."""
    gps_tracking_uid: String
    """The manufacturer."""
    manufacturer: String
    """The model."""
    model: String
    """A descriptive name."""
    name: String
    """The vehicle identification number."""
    vin: String
    """A year."""
    year: Int
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): VehicleConnection!
  """Items sold by vendors."""
  vendor_items(
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
    Archived vendor items may not be used for creating new purchase orders or product requests.
    """
    archived: Boolean
    """A descriptive name."""
    name: String
    """Part number used by the vendor to identify this vendor item."""
    part_number: String
    """The purchase price of this item from the vendor."""
    price: Int
    """
    Number of inventory models that are included in a single unit of this vendors product.
    """
    quantity_per_unit: Int
    """
    Flag for vendor items that should create a one-time service for retail sale to customers.
    """
    retail_item: Boolean
    """The price of the one-time service created for this vendor item"""
    retail_item_price: Int
    """
    The ID of the one-time service created when this vendor item was created.
    """
    retail_item_service_id: Int64Bit
    """The ID of the vendor that sells this item"""
    vendor_id: Int64Bit
    """The ID of the entity that is referred to by this vendor item."""
    vendoritemable_id: Int64Bit
    """The type of entity that is referred to by this vendor item."""
    vendoritemable_type: VendoritemableType
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): VendorItemConnection!
  """Third party vendors."""
  vendors(
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
    Archived vendors may not be used for creating new Purchase Orders or Product Requests.
    """
    archived: Boolean
    """
    Determines if approved purchase orders for this vendor should automatically dispatch an email to the vendor.
    """
    automate_approved_purchase_orders: Boolean
    """The currency used for all transactions with this vendor."""
    currency: Currency
    """A descriptive name."""
    name: String
    """The terms of payment for deliveries from this vendor."""
    payment_terms: PaymentTerm
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): VendorConnection!
  """Voice Provider Rate Import Recipes"""
  voice_provider_rate_import_recipes(
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
    """The percentage over the base rate to charge the customer."""
    charge_percent: Float
    """How many records passed validation checks during import."""
    clean_records: Int
    """Any errors encountered for this import."""
    errors: Clob
    """How many records did not pass validation checks during import."""
    failed_records: Int
    """The identifier of a unique batch at Flatfile."""
    flatfile_batch_identifier: String
    """A hash of the data content of an import."""
    hash: String
    """The progress of an import as a percentage."""
    progress: Int
    """The unique identifier of an import at Sonar."""
    sonar_batch_identifier: String
    """The start date and time for the import."""
    start_datetime: Datetime
    """The status."""
    status: ImportStatus
    """The ID of a User."""
    user_id: Int64Bit
    """The ID of a `VoiceProvider`."""
    voice_provider_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): VoiceProviderRateImportRecipeConnection!
  """Voice Provider Rate Imports"""
  voice_provider_rate_imports(
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
    """The percentage over the base rate to charge the customer."""
    charge_percent: Float
    """How many records passed validation checks during import."""
    clean_records: Int
    """Any errors encountered for this import."""
    errors: Text
    """How many records did not pass validation checks during import."""
    failed_records: Int
    """The status."""
    status: AsyncImportStatus
    """The ID of a `VoiceProvider`."""
    voice_provider_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): VoiceProviderRateImportConnection!
  """Voice Provider Rates."""
  voice_provider_rates(
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
    """The rate that is imported from a rate deck."""
    base_rate: Float
    """The percentage over the base rate to charge the customer."""
    charge_percent: Float
    """The rate that is charged to a customer."""
    charge_rate: Float
    """The description for the rate."""
    description: String
    """The prefix for the rate."""
    prefix: String
    """The ID of a `VoiceProvider`."""
    voice_provider_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): VoiceProviderRateConnection!
  """Voice Providers."""
  voice_providers(
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): VoiceProviderConnection!
  """Details related to a voice service."""
  voice_service_details(
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
    """How often this service bills, in months."""
    billing_frequency: Int
    """
    The cost per minute for local calls, in thousandths of the smallest currency value (e.g. cents, pence, pesos.).
    """
    cost_per_minute_local_in_thousandths: Int
    """
    The cost per minute for long distance calls, in thousandths of the smallest currency value (e.g. cents, pence, pesos.).
    """
    cost_per_minute_long_distance_in_thousandths: Int
    """A two character country code."""
    country: Country
    """
    This is the minimum amount of time the customer will be charged for a call.
    """
    first_interval_in_seconds: Int
    """
    If a customer has a toll free number, this is the rate charged to them for
    inbound calls, in thousandths of the smallest currency value (e.g. cents,
    pence, pesos.).
    """
    inbound_toll_free_rate_per_minute_in_thousandths: Int
    """
    The quantity of free local minutes provided, if `unlimited_local_minutes` is false.
    """
    local_minutes: Int
    """
    The quantity of free long distance minutes provided, if `unlimited_long_distance_minutes` is false.
    """
    long_distance_minutes: Int
    """
    Hide parameters of this service on customer invoices/statements and in the customer portal.
    """
    rollup_generic_parameters: Boolean
    """The ID of a Service."""
    service_id: Int64Bit
    """
    Indicates if Call Detail Records (CDRs) for this service should be displayed on an invoice.
    """
    show_call_detail_records_on_invoice: Boolean
    """
    After the `first_interval_in_seconds` time is exceeded, this is the minimum
    amount of subsequent time. For example, if `first_interval_in_seconds` is
    30, and `sub_interval_in_seconds` is 6, then a 31 second call would be
    charged at 36 seconds, and a 37 second call would be charged at 42 seconds.
    """
    sub_interval_in_seconds: Int
    """The sub type of this voice service."""
    sub_type: VoiceServiceDetailSubType
    """Whether this service provides unlimited local minutes."""
    unlimited_local_minutes: Boolean
    """Whether this service provides unlimited long distance minutes."""
    unlimited_long_distance_minutes: Boolean
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): VoiceServiceDetailConnection!
  """
  Tax definitions that have been assigned to voice service generic parameters.
  """
  voice_service_generic_parameter_tax_definitions(
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
    """Whether this tax definition is for a discount or not."""
    discount: Boolean
    """The ID of entity this tax definition is related to."""
    taxdefinitionable_id: Int64Bit
    """The type of entity this tax definition is related to."""
    taxdefinitionable_type: TaxdefinitionableType
    """The ID of a voice service configuration parameter."""
    voice_service_generic_parameter_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): VoiceServiceGenericParameterTaxDefinitionConnection!
  """The relationship between a service and a tax."""
  voice_service_generic_parameter_taxes(
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
    The amount of the service that is exempt from taxation in the smallest currency value (e.g. cents, pence, pesos.)
    """
    exemption_amount: Int
    """The ID of a Tax."""
    tax_id: Int64Bit
    """The ID of a voice service configuration parameter."""
    voice_service_generic_parameter_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): VoiceServiceGenericParameterTaxConnection!
  """Parameters attached to a voice service."""
  voice_service_generic_parameters(
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
    If this service was prorated when added, this is the date it was prorated from.
    """
    addition_prorate_date: Date
    """A human readable description."""
    description: String
    """The price per unit of this item."""
    price: Int
    """Indicates if changes to this entity trigger proration."""
    proratable: Boolean
    """The ID of a tax definition on a reversed transaction."""
    reverse_tax_definition_id: Int64Bit
    """The ID of a tax definition on a transaction."""
    tax_definition_id: Int64Bit
    """The type."""
    type: VoiceServiceGenericParameterType
    """The ID of the `VoiceServiceDetail`."""
    voice_service_detail_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): VoiceServiceGenericParameterConnection!
  """Voided payments."""
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
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
  """All attempts made to send dispatched webhooks for models and events."""
  webhook_endpoint_event_dispatch_attempts(
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
    """The message of the SMTP response."""
    response: Text
    """The date and time of when a response was received."""
    response_at: Datetime
    """The HTTP status code of the last response."""
    response_code: Int
    """The status."""
    status: WebhookEndpointEventDispatchAttemptStatus
    """The ID of a dispatch for a webhook model event."""
    webhook_endpoint_event_dispatch_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): WebhookEndpointEventDispatchAttemptConnection!
  """All dispatched webhooks for models and events."""
  webhook_endpoint_event_dispatches(
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
    """The date and time of when this was last attempted to be sent."""
    last_attempted_at: Datetime
    """The last status of the last send attempt."""
    last_status: WebhookEndpointEventDispatchAttemptStatus
    """The request payload of a fired webhook being sent to an endpoint."""
    payload: Text
    """The date and time of when this was successfully sent."""
    sent_at: Datetime
    """Indicates of this is a test or not."""
    test: Boolean
    """The model and event attached to the webhook endpoint"""
    webhook_endpoint_event_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): WebhookEndpointEventDispatchConnection!
  """Webhooks models and their events."""
  webhook_endpoint_events(
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
    """An event."""
    event: WebhookEndpointModelEvent
    """The model."""
    model: String
    """The ID of a webhook endpoint."""
    webhook_endpoint_id: Int64Bit
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): WebhookEndpointEventConnection!
  """Webhook endpoints."""
  webhook_endpoints(
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
    """Whether or not this is enabled."""
    enabled: Boolean
    """The URL to the remote resource that webhooks will be sent to."""
    endpoint: HttpsUrl
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
    """The mode to use for general search requests."""
    general_search_mode: GeneralSearchMode = ROOT
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): WebhookEndpointConnection!
  """Webhook model events."""
  webhook_model_events: WebhookModelEventResultConnection
}

"""A subscription to notifications for an entity."""
type Subscription implements LoggableInterface & AccessloggableInterface {
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
  When suspended, the subscription will not send notifications. Permission
  changes and other actions may cause a subscription to become suspended.
  """
  is_suspended: Boolean!
  """The id of the entity that is being subscribed to."""
  subscribable_id: Int64Bit!
  """The type of entity that is being subscribed to."""
  subscribable_type: SubscribableType!
  """The ID of a User."""
  user_id: Int64Bit!
  """A user that can login to Sonar."""
  user(
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
    """Whether or not the user has completed the setup process."""
    completed_setup: Boolean
    """An email address."""
    email_address: EmailAddress
    """Whether or not this is enabled."""
    enabled: Boolean
    """Whether or not this user is a Sonar employee."""
    is_sonar_staff: Boolean
    """A supported language."""
    language: Language
    """A mobile phone number. This will be used to send SMS messages."""
    mobile_number: Numeric
    """A descriptive name."""
    name: String
    """The publicly viewable name of this user."""
    public_name: String
    """The ID of a Role."""
    role_id: Int64Bit
    """
    Super admins receive all system permissions automatically, regardless of their role.
    """
    super_admin: Boolean
    """A username, used for authentication."""
    username: String
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
  ): User
  """The entity that this `Subscription` is associated with."""
  subscribable(
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
    """Provides the ability to paginate through results."""
    paginator: Paginator
    """Provides the ability to sort results."""
    sorter: [Sorter]
    """Complex search parameters."""
    search: [Search]
    """Search across all string fields with partial matching."""
    general_search: String
    """Whether or not to include archived entities in the results."""
    include_archived: Boolean
  ): SubscribableInterface
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
