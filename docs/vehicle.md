```graphql
"""A vehicle."""
type Vehicle implements InventoryitemableInterface & GenericinventoryitemableInterface & GenericinventoryitemactionloggableInterface & NoteableInterface & LoggableInterface & AccessloggableInterface {
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
  """A geo-point."""
  geopoint: Geopoint
  """Whether or not to always track the vehicle."""
  gps_tracking_always: Boolean!
  """If not always, then track on Friday."""
  gps_tracking_day_friday: Boolean!
  """If not always, then track on Monday."""
  gps_tracking_day_monday: Boolean!
  """If not always, then track on Saturday."""
  gps_tracking_day_saturday: Boolean!
  """If not always, then track on Sunday."""
  gps_tracking_day_sunday: Boolean!
  """If not always, then track on Thursday."""
  gps_tracking_day_thursday: Boolean!
  """If not always, then track on Tuesday."""
  gps_tracking_day_tuesday: Boolean!
  """If not always, then track on Wednesday."""
  gps_tracking_day_wednesday: Boolean!
  """Whether or not GPS Tracking enabled for vehicle."""
  gps_tracking_enabled: Boolean!
  """If not always, end time for tracking."""
  gps_tracking_end_time: Time!
  """A `GpsTrackingProvider` ID."""
  gps_tracking_provider_id: Int64Bit
  """If not always, start time for tracking."""
  gps_tracking_start_time: Time!
  """If not always, timezone for start and end times."""
  gps_tracking_timezone: Timezone
  """A GPS Tracking Provider vehicle unique identifier."""
  gps_tracking_uid: String
  """The manufacturer."""
  manufacturer: String
  """The model."""
  model: String
  """A descriptive name."""
  name: String!
  """The vehicle identification number."""
  vin: String
  """A year."""
  year: Int
  """A `GpsTrackingProvider`."""
  gps_tracking_provider(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): GpsTrackingProvider
  """An inventory item."""
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
  """A generic inventory item."""
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
  """A log of an action taken against a set of generic inventory items."""
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
  """A user that can login to Sonar."""
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
  """A history of where the vehicle has travelled."""
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
}

"""The connection wrapper around the `VehicleConnection` type."""
type VehicleConnection {
  """A list of the entities provided by this connection."""
  entities: [Vehicle]!
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

"""A history of where the vehicle has travelled."""
type VehicleLocationHistory implements LoggableInterface & AccessloggableInterface {
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
  """A decimal latitude."""
  latitude: Latitude!
  """A decimal longitude."""
  longitude: Longitude!
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
  vehicle_id: Int64Bit!
  """A vehicle."""
  vehicle(
    """The ID of the entity."""
    id: Int64Bit
    """
    An ID that uniquely identifies this entity across the whole Sonar system.
    """
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
    """
    Provides the ability to return aggregated mathematical data about your results.
    """
    aggregation: [Aggregator]
    """
    Reverse relation filters allow you to filter the result of a relation, and
    use that filter to affect the returned root elements.
    """
    reverse_relation_filters: [ReverseRelationFilter]
  ): Vehicle
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
The connection wrapper around the `VehicleLocationHistoryConnection` type.
"""
type VehicleLocationHistoryConnection {
  """A list of the entities provided by this connection."""
  entities: [VehicleLocationHistory]!
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
