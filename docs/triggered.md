```graphql
"""An `Email` that is sent when a particular event occurs."""
type TriggeredEmail implements NoteableInterface & LoggableInterface & AccessloggableInterface {
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
  """Whether or not child accounts are allowed."""
  allow_children: Boolean!
  """
  The count associated with this `TriggeredEmail`. This is defined by the
  trigger, and could be something like a number of days, months, gigabytes, etc.
  """
  count: Int
  """The ID of an EmailMessage."""
  email_message_id: Int64Bit!
  """Whether or not this is enabled."""
  enabled: Boolean!
  """The ID of a `JobType`."""
  job_type_id: Int64Bit
  """A descriptive name."""
  name: String!
  """If an item is protected, it cannot be modified or deleted."""
  protected: Boolean!
  """The trigger for this message."""
  trigger: EmailTrigger!
  """An email message."""
  email_message(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): EmailMessage
  """The type of a `Job`."""
  job_type(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): JobType
  """A categorization of a message by type."""
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
  """A categorization of an `Email` by type."""
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
  """An invoice."""
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
  """Accounts exceeding a data usage triggered email."""
  accounts_exceeding_usage_triggers(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
  ): AccountConnection!
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

"""The connection wrapper around the `TriggeredEmailConnection` type."""
type TriggeredEmailConnection {
  """A list of the entities provided by this connection."""
  entities: [TriggeredEmail]!
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

"""A message that is sent when a specific event occurs."""
type TriggeredMessage implements NoteableInterface & LoggableInterface & AccessloggableInterface {
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
  """Whether or not child accounts are allowed."""
  allow_children: Boolean!
  """
  The count associated with this `TriggeredMessage`. This is defined by the
  trigger, and could be something like a number of days, months, gigabytes, etc.
  """
  count: Int
  """The ID of an EmailMessage."""
  email_message_id: Int64Bit
  """Whether or not this is enabled."""
  enabled: Boolean!
  """The ID of a `JobType`."""
  job_type_id: Int64Bit
  """A descriptive name."""
  name: String!
  """If an item is protected, it cannot be modified or deleted."""
  protected: Boolean!
  """The ID of a signature."""
  signature_id: Int64Bit
  """The ID of the SMS message."""
  sms_message_id: Int64Bit
  """The trigger for this message."""
  trigger: MessageTrigger!
  """An email message."""
  email_message(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): EmailMessage
  """The type of a `Job`."""
  job_type(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): JobType
  """A signature."""
  signature(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): Signature
  """An SMS message."""
  sms_message(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): SmsMessage
  """A categorization of a message by type."""
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
  """A categorization of an `Email` by type."""
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
  """An invoice."""
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
  """Accounts exceeding a data usage triggered email."""
  accounts_exceeding_usage_triggers(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
  ): AccountConnection!
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

"""The connection wrapper around the `TriggeredMessageConnection` type."""
type TriggeredMessageConnection {
  """A list of the entities provided by this connection."""
  entities: [TriggeredMessage]!
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
