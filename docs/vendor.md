```graphql
"""A third party vendor of inventory models."""
type Vendor implements AddressableInterface & ContactableInterface & EmailableInterface & NoteableInterface & FileableInterface & LoggableInterface & AccessloggableInterface {
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
  Archived vendors may not be used for creating new Purchase Orders or Product Requests.
  """
  archived: Boolean!
  """
  Determines if approved purchase orders for this vendor should automatically dispatch an email to the vendor.
  """
  automate_approved_purchase_orders: Boolean!
  """The currency used for all transactions with this vendor."""
  currency: Currency!
  """A descriptive name."""
  name: String!
  """The terms of payment for deliveries from this vendor."""
  payment_terms: PaymentTerm!
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
  """An email."""
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
  """A note."""
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
  """A file."""
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
  """An item that can be purchased from a particular vendor."""
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
  """A purchase order for items from a third party vendor."""
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
  """A tax."""
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
}

"""The connection wrapper around the `VendorConnection` type."""
type VendorConnection {
  """A list of the entities provided by this connection."""
  entities: [Vendor]!
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

"""An item that can be purchased from a particular vendor."""
type VendorItem implements NoteableInterface & LoggableInterface & AccessloggableInterface {
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
  Archived vendor items may not be used for creating new purchase orders or product requests.
  """
  archived: Boolean!
  """A descriptive name."""
  name: String!
  """Part number used by the vendor to identify this vendor item."""
  part_number: String
  """The purchase price of this item from the vendor."""
  price: Int!
  """
  Number of inventory models that are included in a single unit of this vendors product.
  """
  quantity_per_unit: Int!
  """
  Flag for vendor items that should create a one-time service for retail sale to customers.
  """
  retail_item: Boolean!
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
  """An entity that is associated to a vendor item."""
  vendoritemable(
    """The ID of the entity."""
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
  ): VendoritemableInterface
  """A third party vendor of inventory models."""
  vendor(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): Vendor
  """A one-time service associated with a vendor item."""
  retail_item_service(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
  """The relationship between an `Account` and a `Service`."""
  account_service(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AccountService
  """The relationship between a `Package` and a `Service`."""
  package_service(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): PackageService
  """A line item on a purchase order."""
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
  """A note."""
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

"""The connection wrapper around the `VendorItemConnection` type."""
type VendorItemConnection {
  """A list of the entities provided by this connection."""
  entities: [VendorItem]!
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
