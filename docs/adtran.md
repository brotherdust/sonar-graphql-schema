```graphql
"""An Adtran Mosaic audit record."""
type AdtranMosaicAudit implements NoteableInterface & LoggableInterface & AccessloggableInterface {
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
  """The ID of an AccountService."""
  account_service_id: Int64Bit
  """The Adtran assigned device name."""
  adtran_device_name: String
  """The serial number associated with the Adtran device."""
  adtran_device_serial_number: String
  """The Adtran interface name."""
  adtran_interface_name: String
  """The ID of an Adtran Mosaic setting."""
  adtran_mosaic_setting_id: Int64Bit!
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
  is_visible: Boolean!
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
  """An Adtran Mosaic settings record."""
  adtran_mosaic_setting(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AdtranMosaicSetting
  """An inventory item."""
  inventory_item(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): InventoryItem
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

"""The connection wrapper around the `AdtranMosaicAuditConnection` type."""
type AdtranMosaicAuditConnection {
  """A list of the entities provided by this connection."""
  entities: [AdtranMosaicAudit]!
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

"""types.adtranMosaicCloudListType"""
type AdtranMosaicCloudList {
  """The value."""
  value: String
}

"""The connection wrapper around the `AdtranMosaicCloudList` type."""
type AdtranMosaicCloudListConnection {
  """A list of the entities provided by this connection."""
  entities: [AdtranMosaicCloudList]!
  """
  An object providing information about the page of results being displayed, as
  well as the total amount of pages/records available.
  """
  page_info: PageInfo!
}

"""An Adtran Mosaic Kafka event record."""
type AdtranMosaicKafkaEvent implements NoteableInterface & LoggableInterface & AccessloggableInterface {
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
  """The ID of an Adtran Mosaic setting."""
  adtran_mosaic_setting_id: Int64Bit!
  """The Kafka topic to for the event."""
  kafka_topic: String
  """Key for a specific value."""
  key: String
  """The value."""
  value: String
  """An Adtran Mosaic settings record."""
  adtran_mosaic_setting(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AdtranMosaicSetting
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

"""
The connection wrapper around the `AdtranMosaicKafkaEventConnection` type.
"""
type AdtranMosaicKafkaEventConnection {
  """A list of the entities provided by this connection."""
  entities: [AdtranMosaicKafkaEvent]!
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

"""An Adtran Mosaic settings record."""
type AdtranMosaicSetting implements IntegrationconfigurableInterface & NoteableInterface & NotifiableInterface & LoggableInterface & AccessloggableInterface {
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
  """Controls if Sonar updates the ICMP device status from SMx alarms"""
  alarms_change_device_status: Boolean!
  """Controls if Sonar should add SMx device alarms to inventory item logs"""
  alarms_create_logs: Boolean!
  """The base API URL."""
  api_url: String!
  """Whether or not to suspend unattached services."""
  auto_suspend_unattached_services: Boolean!
  """
  Disable, pause, then re-enable Calix ONT ports after creating or removing
  service.  Recommended for deployments using DHCP within SMx.
  """
  bounce_ports: Boolean!
  """Bounce ports disable profile."""
  bounce_ports_disable_profile: String!
  """Bounce ports enable profile."""
  bounce_ports_enable_profile: String!
  """Commercial account type delinquency profile vector."""
  commercial_delinquency_profile_vector: String
  """Whether or not commercial account type suspends."""
  commercial_delinquency_suspends: Boolean!
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
  default_uplink_outer_tag_vlan: String!
  """Whether or not this is enabled."""
  enabled: Boolean!
  """Government account type delinquency profile vector."""
  government_delinquency_profile_vector: String
  """Whether or not government account type suspends."""
  government_delinquency_suspends: Boolean!
  """Industrial account type delinquency profile vector."""
  industrial_delinquency_profile_vector: String
  """Whether or not industrial account type suspends."""
  industrial_delinquency_suspends: Boolean!
  """The date and time this device was last synchronized."""
  last_synchronized: Datetime
  """A password."""
  password: String!
  """Residential account type delinquency profile vector."""
  residential_delinquency_profile_vector: String
  """Whether or not residential account type suspends."""
  residential_delinquency_suspends: Boolean!
  """Senior citizen account type delinquency profile vector."""
  senior_citizen_delinquency_profile_vector: String
  """Whether or not senior citizen account type suspends."""
  senior_citizen_delinquency_suspends: Boolean!
  """Whether or not a synchronization audit has been run."""
  synchronization_audit_ran: Boolean!
  """Whether or not a synchronization request is queued."""
  synchronization_queued: Boolean!
  """The date/time that synchronization started."""
  synchronization_start: Datetime
  """Status of the synchronization process."""
  synchronization_status: SynchronizationStatus!
  """Details regarding the current synchronization status if any."""
  synchronization_status_message: String
  """A username, used for authentication."""
  username: String!
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
  """An account Adtran Mosaic service detail."""
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
  """
  An entity which maps an inventory model field to a vendor specific integration field type (ie serial number)
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
  """An entity which maps a service to a vendor specific service name"""
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
  """A `Notification`."""
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

"""
The connection wrapper around the `AdtranMosaicSettingConnection` type.
"""
type AdtranMosaicSettingConnection {
  """A list of the entities provided by this connection."""
  entities: [AdtranMosaicSetting]!
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

"""An Adtran Mosaic workflow event record."""
type AdtranMosaicWorkflowEvent implements NoteableInterface & LoggableInterface & AccessloggableInterface {
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
  """The ID of an Adtran Mosaic setting."""
  adtran_mosaic_setting_id: Int64Bit!
  """The completion status of the event."""
  completion_status: String
  """The complete event object of the event."""
  event_object: String!
  """The status of the event."""
  status: String
  """The timestamp of the event."""
  timestamp: Datetime
  """The transaction ID of the event."""
  trans_id: String
  """An Adtran Mosaic settings record."""
  adtran_mosaic_setting(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): AdtranMosaicSetting
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

"""
The connection wrapper around the `AdtranMosaicWorkflowEventConnection` type.
"""
type AdtranMosaicWorkflowEventConnection {
  """A list of the entities provided by this connection."""
  entities: [AdtranMosaicWorkflowEvent]!
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
