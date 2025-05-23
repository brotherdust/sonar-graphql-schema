```graphql
type Mutation {
  """Make additional funds available to the instance service fund."""
  addInstanceServiceFunds(input: AddInstanceServiceFundsMutationInput): InstanceServiceFunds!
  """Add a package to an account."""
  addPackageToAccount(input: AddPackageToAccountMutationInput): [AccountService]
  """Add a recurring or expiring service to an account."""
  addServiceToAccount(input: AddServiceToAccountMutationInput): AccountService
  """Allocate a report builder license to a user."""
  allocateLookerExploreLicenseToUser(input: AllocateLookerExploreLicenseToUserMutationInput): LookerExploreLicense
  """Allocate a report viewer license to a user."""
  allocateLookerViewLicenseToUser(input: AllocateLookerViewLicenseToUserMutationInput): LookerViewLicense
  """Apply a credit to an invoice with a due balance."""
  applyCreditToInvoice(
    input: ApplyCreditToInvoiceMutationInput
    """The ID of an `Invoice`."""
    id: Int64Bit!
  ): Invoice
  """Archive an account."""
  archiveAccount(
    """The ID of the entity."""
    id: Int64Bit!
  ): Account
  """Assign generic inventory items to an assignee."""
  assignGenericInventoryItems(
    input: AssignGenericInventoryItemsMutationInput
    """fields.generic_inventory_item_id"""
    id: Int64Bit!
  ): GenericInventoryItem
  """Assign one or more inventory items to a new assignee."""
  assignInventoryItems(
    input: AssignInventoryItemsMutationInput
    """The ID of an `InventoryItem`."""
    ids: [Int64Bit!]!
  ): [InventoryItem]
  """Perform manual Adtran Mosaic audit."""
  auditAdtranMosaic(input: AuditAdtranMosaicMutationInput): AdtranMosaicSetting
  """Audit Calix Cloud subscribers to Sonar accounts."""
  auditCalixCloud(input: AuditCalixCloudMutationInput): CalixCloudSetting
  """Perform manual repair of Adtran Mosaic Cloud audit entries."""
  auditRepairAdtranMosaic(
    """The ID of an Adtran Mosaic audit record."""
    id: Int64Bit!
  ): SuccessResponse
  """Cancel a print to mail batch."""
  cancelPrintToMailBatch(
    """The ID of the print to mail batch."""
    id: Int64Bit!
  ): SuccessResponse
  """Check in to a job."""
  checkInToJob(input: CheckInToJobMutationInput): JobCheckIn
  """Check out of a job."""
  checkOutOfJob(input: CheckOutOfJobMutationInput): JobCheckIn
  """Claim one or many inventory items."""
  claimInventoryItems(input: ClaimInventoryItemsMutationInput): SuccessResponse
  """Complete a task that requires a file for a completion type."""
  completeFileTask(
    input: CompleteFileTaskMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): Task
  """Complete a job."""
  completeJob(input: CompleteJobMutationInput): Job
  """Complete or uncomplete a task."""
  completeTask(
    input: CompleteTaskMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): Task
  """Consume generic inventory items."""
  consumeGenericInventoryItems(
    input: ConsumeGenericInventoryItemsMutationInput
    """fields.generic_inventory_item_id"""
    id: Int64Bit!
  ): GenericInventoryItem
  """Create an access log entry on an entity for the current user."""
  createAccessLog(input: CreateAccessLogMutationInput): AccessLog
  """Create a new account."""
  createAccount(input: CreateAccountMutationInput): Account
  """
  Create a one time transaction from an adjustment service for an account.
  """
  createAccountAdjustmentTransaction(input: CreateAccountAdjustmentTransactionMutationInput): TransactionInterface
  """Create account Adtran Mosaic service details."""
  createAccountAdtranMosaicServiceDetail(input: CreateAccountAdtranMosaicServiceDetailMutationInput): AccountAdtranMosaicServiceDetail
  """Create an account calix service detail."""
  createAccountCalixServiceDetail(input: CreateAccountCalixServiceDetailMutationInput): AccountCalixServiceDetail
  """Create a new account group."""
  createAccountGroup(input: CreateAccountGroupMutationInput): AccountGroup
  """Create a one time transaction for an account."""
  createAccountOneTimeTransaction(input: CreateAccountOneTimeTransactionMutationInput): [TransactionInterface]
  """Create a new account status."""
  createAccountStatus(input: CreateAccountStatusMutationInput): AccountStatus
  """Create a new account type."""
  createAccountType(input: CreateAccountTypeMutationInput): AccountType
  """Create a new ACH batch."""
  createAchBatch(input: CreateAchBatchMutationInput): [AchBatch]!
  """Create an address list."""
  createAddressList(input: CreateAddressListMutationInput): AddressList
  """Create a new address status."""
  createAddressStatus(input: CreateAddressStatusMutationInput): AddressStatus
  """Create a new adjustment service."""
  createAdjustmentService(input: CreateAdjustmentServiceMutationInput): Service
  """Create Adtran Mosaic settings."""
  createAdtranMosaicSetting(input: CreateAdtranMosaicSettingMutationInput): AdtranMosaicSetting
  """Create a new alerting rotation."""
  createAlertingRotation(input: CreateAlertingRotationMutationInput): AlertingRotation
  """Create a new alerting rotation day."""
  createAlertingRotationDay(input: CreateAlertingRotationDayMutationInput): AlertingRotationDay
  """Create a new application firewall rule."""
  createApplicationFirewallRule(input: CreateApplicationFirewallRuleMutationInput): ApplicationFirewallRule
  """Create an authentication factor."""
  createAuthenticationFactor(input: CreateAuthenticationFactorMutationInput): AuthenticationFactor
  """Create an Avalara bundled tax definition."""
  createAvalaraTaxDefinition(input: CreateAvalaraTaxDefinitionMutationInput): AvalaraTaxDefinition
  """Create a new bank account."""
  createBankAccount(input: CreateBankAccountMutationInput): BankAccount
  """Create a payment using a bank account."""
  createBankAccountPayment(input: CreateBankAccountPaymentMutationInput): Payment
  """Create a new bank account processor."""
  createBankAccountProcessor(input: CreateBankAccountProcessorMutationInput): BankAccountProcessor
  """Create a new billing default."""
  createBillingDefault(input: CreateBillingDefaultMutationInput): BillingDefault
  """Create a cable modem provisioner."""
  createCableModemProvisioner(input: CreateCableModemProvisionerMutationInput): CableModemProvisioner
  """Create a calendar - iCalendar."""
  createCalendarIcal(input: CreateCalendarIcalMutationInput): CalendarIcal
  """Create a Calix Cloud setting."""
  createCalixCloudSetting(input: CreateCalixCloudSettingMutationInput): CalixCloudSetting
  """Create a Calix integration"""
  createCalixIntegration(input: CreateCalixIntegrationMutationInput): CalixIntegration
  """Create a call detail record (CDR)."""
  createCallDetailRecord(input: CreateCallDetailRecordMutationInput): CallDetailRecord
  """Create a Flatfile import of call detail records (CDRs)."""
  createCallDetailRecordImportFlatfile(input: CreateCallDetailRecordImportFlatfileMutationInput): CallDetailRecordImportRecipe
  """Create a call log."""
  createCallLog(input: CreateCallLogMutationInput): CallLog
  """Create a new canned reply."""
  createCannedReply(input: CreateCannedReplyMutationInput): CannedReply
  """Create a new canned reply category."""
  createCannedReplyCategory(input: CreateCannedReplyCategoryMutationInput): CannedReplyCategory
  """Create a new company."""
  createCompany(input: CreateCompanyMutationInput): Company
  """Create a new contact."""
  createContact(input: CreateContactMutationInput): Contact
  """Create a new contract."""
  createContract(input: CreateContractMutationInput): Contract
  """Create a new contract template."""
  createContractTemplate(input: CreateContractTemplateMutationInput): ContractTemplate
  """Create a Core credit card."""
  createCoreCreditCard(input: CreateCoreCreditCardMutationInput): CoreCreditCard
  """Create a Core payment."""
  createCorePayment(input: CreateCorePaymentMutationInput): CorePayment
  """Create a new credit card."""
  createCreditCard(input: CreateCreditCardMutationInput): CreditCard
  """Create a credit card."""
  createCreditCardPayment(input: CreateCreditCardPaymentMutationInput): Payment
  """Create a new credit card processor."""
  createCreditCardProcessor(input: CreateCreditCardProcessorMutationInput): CreditCardProcessor
  """Create a new custom field."""
  createCustomField(input: CreateCustomFieldMutationInput): CustomField
  """Create a new custom link."""
  createCustomLink(input: CreateCustomLinkMutationInput): CustomLink
  """Create a data service."""
  createDataService(input: CreateDataServiceMutationInput): Service
  """Create a data usage top off."""
  createDataUsageTopOff(input: CreateDataUsageTopOffMutationInput): DataUsageTopOff
  """
  Create data usage entries.  This will also update each account last
  aggregation date to the earliest datetime in the submitted recordset. 
  """
  createDataUsages(input: [CreateDataUsageMutationInput]): SuccessResponse
  """Create a delinquency exclusion."""
  createDelinquencyExclusion(input: CreateDelinquencyExclusionMutationInput): DelinquencyExclusion
  """Create a department."""
  createDepartment(input: CreateDepartmentMutationInput): Department
  """Create a new deployment type."""
  createDeploymentType(input: CreateDeploymentTypeMutationInput): DeploymentType
  """Create a new deposit slip."""
  createDepositSlip(input: CreateDepositSlipMutationInput): DepositSlip
  """Create a DHCP server."""
  createDhcpServer(input: CreateDhcpServerMutationInput): DhcpServer
  """Create a DHCP server identifier."""
  createDhcpServerIdentifier(input: CreateDhcpServerIdentifierMutationInput): DhcpServerIdentifier
  """Create a DID."""
  createDid(input: CreateDidMutationInput): Did
  """Create a DID assignment."""
  createDidAssignment(input: CreateDidAssignmentMutationInput): DidAssignment
  """Create a Flatfile import of DIDs."""
  createDidImportFlatfile(input: CreateDidImportFlatfileMutationInput): DidImportRecipe
  """Create a new messaging category."""
  createEmailCategory(input: CreateEmailCategoryMutationInput): EmailCategory
  """Create a new email domain."""
  createEmailDomain(input: CreateEmailDomainMutationInput): EmailDomain
  """Create a new saved message."""
  createEmailMessage(input: CreateEmailMessageMutationInput): EmailMessage
  """Create new saved message contents."""
  createEmailMessageContent(input: CreateEmailMessageContentMutationInput): EmailMessageContent
  """Create an LTE EPC."""
  createEpc(input: CreateEpcMutationInput): Epc
  """Create a new expiring service."""
  createExpiringService(input: CreateExpiringServiceMutationInput): Service
  """Create an external marketing integration."""
  createExternalMarketingProvider(input: CreateExternalMarketingProviderMutationInput): ExternalMarketingProvider
  """Create a FCC Form 477 report."""
  createFccForm477Report(input: CreateFccForm477ReportMutationInput): FccForm477Report
  """Create a FiberMap Integration."""
  createFibermapIntegration(input: CreateFibermapIntegrationMutationInput): FibermapIntegration
  """Create a new general ledger code."""
  createGeneralLedgerCode(input: CreateGeneralLedgerCodeMutationInput): GeneralLedgerCode
  """Create a generic inventory assignee."""
  createGenericInventoryAssignee(input: CreateGenericInventoryAssigneeMutationInput): GenericInventoryAssignee
  """Create new generic inventory items."""
  createGenericInventoryItems(input: CreateGenericInventoryItemsMutationInput): GenericInventoryItem
  """Create a new geo tax zone."""
  createGeoTaxZone(input: CreateGeoTaxZoneMutationInput): GeoTaxZone
  """Create a geofence."""
  createGeofence(input: CreateGeofenceMutationInput): Geofence
  """Create a Global Inventory Model Min/Max."""
  createGlobalInventoryModelMinMax(input: CreateGlobalInventoryModelMinMaxMutationInput): GlobalInventoryModelMinMax
  """Create a GPS tracking provider."""
  createGpsTrackingProvider(input: CreateGpsTrackingProviderMutationInput): GpsTrackingProvider
  """Create an ActiveDirectory identity provider."""
  createIdentityProviderActiveDirectory(input: CreateIdentityProviderActiveDirectoryMutationInput): IdentityProvider
  """Create a Google identity provider."""
  createIdentityProviderGoogle(input: CreateIdentityProviderGoogleMutationInput): IdentityProvider
  """Create a Microsoft identity provider."""
  createIdentityProviderMicrosoft(input: CreateIdentityProviderMicrosoftMutationInput): IdentityProvider
  """Create a SAML identity provider."""
  createIdentityProviderSaml(input: CreateIdentityProviderSamlMutationInput): IdentityProvider
  """Create a new inbound mailbox."""
  createInboundMailbox(input: CreateInboundMailboxMutationInput): InboundMailbox
  """Create an inline device."""
  createInlineDevice(input: CreateInlineDeviceMutationInput): InlineDevice
  """Create a new internal location."""
  createInternalLocation(input: CreateInternalLocationMutationInput): InternalLocation
  """Create an internal ticket."""
  createInternalTicket(input: CreateInternalTicketMutationInput): Ticket
  """Create an inventory item segment."""
  createInventoryItemSegment(input: CreateInventoryItemSegmentMutationInput): InventoryItem
  """Create one or many inventory items."""
  createInventoryItems(input: CreateInventoryItemsMutationInput): [InventoryItem]
  """Create a new inventory location."""
  createInventoryLocation(input: CreateInventoryLocationMutationInput): InventoryLocation
  """Create a new inventory model."""
  createInventoryModel(input: CreateInventoryModelMutationInput): InventoryModel
  """Create a new inventory model category."""
  createInventoryModelCategory(input: CreateInventoryModelCategoryMutationInput): InventoryModelCategory
  """Create a new inventory model field."""
  createInventoryModelField(input: CreateInventoryModelFieldMutationInput): InventoryModelField
  """Create an Inventory Model Min/Max."""
  createInventoryModelMinMax(input: CreateInventoryModelMinMaxMutationInput): InventoryModelMinMax
  """Create a new invoice."""
  createInvoice(input: CreateInvoiceMutationInput): Invoice
  """Create an invoice attachment."""
  createInvoiceAttachment(input: CreateInvoiceAttachmentMutationInput): InvoiceAttachment
  """Create an invoice message."""
  createInvoiceMessage(input: CreateInvoiceMessageMutationInput): InvoiceMessage
  """Create an invoice template."""
  createInvoiceTemplate(input: CreateInvoiceTemplateMutationInput): InvoiceTemplate
  """Create a new IP assignment."""
  createIpAssignment(input: CreateIpAssignmentMutationInput): IpAssignment
  """Create a new IP assignment from a MAC/IP address pair."""
  createIpAssignmentFromDhcpReservation(input: CreateIpAssignmentFromDhcpReservationMutationInput): SuccessResponse
  """Create a new IP pool."""
  createIpPool(input: CreateIpPoolMutationInput): IpPool
  """Create a job."""
  createJob(input: CreateJobMutationInput): Job
  """Associate a service with a job."""
  createJobService(input: CreateJobServiceMutationInput): JobService
  """Create a job type."""
  createJobType(input: CreateJobTypeMutationInput): JobType
  """Create linked addresses in bulk."""
  createLinkedAddresses(input: CreateLinkedAddressesMutationInput): CreateLinkedAddressesResponse
  """Create a new local prefix."""
  createLocalPrefix(input: CreateLocalPrefixMutationInput): LocalPrefix
  """Create an LTE provider."""
  createLteProvider(input: CreateLteProviderMutationInput): LteProvider
  """Create a new account mailing address."""
  createMailingAddress(input: CreateMailingAddressMutationInput): Address
  """Create a new manufacturer."""
  createManufacturer(input: CreateManufacturerMutationInput): Manufacturer
  """Create a map overlay."""
  createMapOverlay(input: CreateMapOverlayMutationInput): MapOverlay
  """Create a mass email communication."""
  createMassEmail(input: CreateMassEmailMutationInput): MassEmail
  """Create a mass message communication."""
  createMassMessage(input: CreateMassMessageMutationInput): SuccessResponseWithId
  """Create a messaging category."""
  createMessageCategory(input: CreateMessageCategoryMutationInput): MessageCategory
  """Create a Netflow allowed subnet."""
  createNetflowAllowedSubnet(input: CreateNetflowAllowedSubnetMutationInput): NetflowAllowedSubnet
  """Create a Netflow endpoint."""
  createNetflowEndpoint(input: CreateNetflowEndpointMutationInput): NetflowEndpoint
  """Create a Netflow on premise record."""
  createNetflowOnPremise(input: CreateNetflowOnPremiseMutationInput): NetflowOnPremise
  """Create a Netflow whitelist."""
  createNetflowWhitelist(input: CreateNetflowWhitelistMutationInput): NetflowWhitelist
  """Create a Network Monitoring Graph."""
  createNetworkMonitoringGraph(input: CreateNetworkMonitoringGraphMutationInput): NetworkMonitoringGraph
  """Create a Network Monitoring Template."""
  createNetworkMonitoringTemplate(input: CreateNetworkMonitoringTemplateMutationInput): NetworkMonitoringTemplate
  """Create a network site."""
  createNetworkSite(input: CreateNetworkSiteMutationInput): NetworkSite
  """Create a non-inventory item."""
  createNonInventoryItem(input: CreateNonInventoryItemMutationInput): NonInventoryItem
  """Create a new note."""
  createNote(input: CreateNoteMutationInput): Note
  """Create a new one time service."""
  createOneTimeService(input: CreateOneTimeServiceMutationInput): Service
  """Create an order group."""
  createOrderGroup(input: CreateOrderGroupMutationInput): OrderGroup
  """Create an overage service."""
  createOverageService(input: CreateOverageServiceMutationInput): Service
  """Create a package."""
  createPackage(input: CreatePackageMutationInput): Package
  """Create a new PayPal credential."""
  createPayPalCredential(input: CreatePayPalCredentialMutationInput): PayPalCredential
  """Create a new payment without a payment method."""
  createPayment(input: CreatePaymentMutationInput): Payment
  """Create a multiple new payment without a payment method."""
  createPayments(input: CreatePaymentsMutationInput): PaymentResultConnection!
  """Create a personal access token."""
  createPersonalAccessToken(input: CreatePersonalAccessTokenMutationInput): PersonalAccessToken
  """Create a new phone number."""
  createPhoneNumber(input: CreateContactPhoneNumberMutationInput): PhoneNumber
  """Create a new phone number type."""
  createPhoneNumberType(input: CreatePhoneNumberTypeMutationInput): PhoneNumberType
  """Create a poller."""
  createPoller(input: CreatePollerMutationInput): Poller
  """Create a new printed invoice batch."""
  createPrintedInvoiceBatch(input: CreatePrintedInvoiceBatchMutationInput): SuccessResponse
  """Create a public ticket."""
  createPublicTicket(input: CreatePublicTicketMutationInput): Ticket
  """Create a purchase order."""
  createPurchaseOrder(input: CreatePurchaseOrderMutationInput): PurchaseOrder
  """Create a new RADIUS account."""
  createRadiusAccount(input: CreateRadiusAccountMutationInput): RadiusAccount
  """Create a RADIUS group."""
  createRadiusGroup(input: CreateRadiusGroupMutationInput): RadiusGroup
  """Create a RADIUS group reply attribute."""
  createRadiusGroupReplyAttribute(input: CreateRadiusGroupReplyAttributeMutationInput): RadiusGroupReplyAttribute
  """Create a RADIUS server."""
  createRadiusServer(input: CreateRadiusServerMutationInput): RadiusServer
  """Create a rate center."""
  createRateCenter(input: CreateRateCenterMutationInput): RateCenter
  """Add an entity to your recent items list."""
  createRecentItem(input: CreateRecentItemMutationInput): [RecentItem]
  """Create a new recurring service."""
  createRecurringService(input: CreateRecurringServiceMutationInput): Service
  """Create a report."""
  createReport(input: CreateReportMutationInput): AvailableReport
  """Create a new role."""
  createRole(input: CreateRoleMutationInput): Role
  """Create a saved message category."""
  createSavedMessageCategory(input: CreateSavedMessageCategoryMutationInput): SavedMessageCategory
  """Create a schedule address."""
  createScheduleAddress(input: CreateScheduleAddressMutationInput): ScheduleAddress
  """Create a schedule availability."""
  createScheduleAvailability(input: CreateScheduleAvailabilityMutationInput): ScheduleAvailability
  """Create a schedule availability day/time."""
  createScheduleAvailabilityDayTime(input: CreateScheduleAvailabilityDayTimeMutationInput): ScheduleAvailabilityDayTime
  """Create a schedule blocker."""
  createScheduleBlocker(input: CreateScheduleBlockerMutationInput): ScheduleBlocker
  """Create a schedule blocker day/time."""
  createScheduleBlockerDayTime(input: CreateScheduleBlockerDayTimeMutationInput): ScheduleBlockerDayTime
  """Create a schedule time off."""
  createScheduleTimeOff(input: CreateScheduleTimeOffMutationInput): ScheduleTimeOff
  """Create a scheduled event."""
  createScheduledEvent(input: CreateScheduledEventMutationInput): ScheduledEvent
  """Create a saved search filter for the current user."""
  createSearchFilter(input: CreateSearchFilterMutationInput): SearchFilter
  """Create service metadata."""
  createServiceMetadata(input: CreateServiceMetadataMutationInput): ServiceMetadata
  """Create a new serviceable address."""
  createServiceableAddress(input: CreateServiceableAddressMutationInput): Address
  """Create a serviceable address account assignment future"""
  createServiceableAddressAccountAssignmentFuture(input: CreateServiceableAddressAccountAssignmentFutureMutationInput): ServiceableAddressAccountAssignmentFuture
  """Create a Signature."""
  createSignature(input: CreateSignatureMutationInput): Signature
  """Create an SNMP OID."""
  createSnmpOid(input: CreateSnmpOidMutationInput): SnmpOid
  """Create an SNMP OID threshold."""
  createSnmpOidThreshold(input: CreateSnmpOidThresholdMutationInput): SnmpOidThreshold
  """Create an SNMP override."""
  createSnmpOverride(input: CreateSnmpOverrideMutationInput): SnmpOverride
  """Create a Sonar Import."""
  createSonarImport(input: CreateSonarImportMutationInput): ImportRecipe
  """Create a stored view."""
  createStoredView(input: CreateStoredViewMutationInput): StoredView
  """Create a new subnet."""
  createSubnet(input: CreateSubnetMutationInput): Subnet
  """Create a subscription."""
  createSubscription(input: CreateSubscriptionMutationInput): Subscription
  """Create a new supernet."""
  createSupernet(input: CreateSupernetMutationInput): Supernet
  """Directly trigger a system backup of all database tables."""
  createSystemBackup(input: CreateSystemBackupMutationInput): SystemBackup
  """Create a destination that system backups can be exported to."""
  createSystemBackupDestination(input: CreateSystemBackupDestinationMutationInput): SystemBackupDestination
  """Create a new task."""
  createTask(input: CreateTaskMutationInput): Task
  """Create a task template."""
  createTaskTemplate(input: CreateTaskTemplateMutationInput): TaskTemplate
  """Create a task template item."""
  createTaskTemplateItem(input: CreateTaskTemplateItemMutationInput): TaskTemplateItem
  """Create a new tax."""
  createTax(input: CreateTaxMutationInput): Tax
  """Create a tax exemption."""
  createTaxExemption(input: CreateTaxExemptionMutationInput): TaxExemption
  """Create a tax override."""
  createTaxOverride(input: CreateTaxOverrideMutationInput): TaxOverride
  """Create a tax provider."""
  createTaxProvider(input: CreateTaxProviderMutationInput): TaxProvider
  """Create a new ticket category."""
  createTicketCategory(input: CreateTicketCategoryMutationInput): TicketCategory
  """Create a ticket comment."""
  createTicketComment(input: CreateTicketCommentMutationInput): TicketComment
  """Create a new ticket group."""
  createTicketGroup(input: CreateTicketGroupMutationInput): TicketGroup
  """Create a ticket recipient."""
  createTicketRecipient(input: CreateTicketRecipientMutationInput): TicketRecipient
  """Create a new ticket reply."""
  createTicketReply(input: CreateTicketReplyMutationInput): TicketReply
  """Create a new bank account that has already been tokenized."""
  createTokenizedBankAccount(input: CreateTokenizedBankAccountMutationInput): BankAccount
  """Create a new credit card that has already been tokenized."""
  createTokenizedCreditCard(input: CreateTokenizedCreditCardMutationInput): CreditCard
  """
  DEPRECATED: Create a new triggered email. See createTriggeredMessageMutation.
  """
  createTriggeredEmail(input: CreateTriggeredEmailMutationInput): TriggeredEmail
  """Create a triggered message."""
  createTriggeredMessage(input: CreateTriggeredMessageMutationInput): TriggeredMessage
  """Create a new uninventoried MAC address."""
  createUninventoriedMacAddress(input: CreateUninventoriedMacAddressMutationInput): UninventoriedMacAddress
  """Create a usage based billing policy."""
  createUsageBasedBillingPolicy(input: CreateUsageBasedBillingPolicyMutationInput): UsageBasedBillingPolicy
  """Create a free period in a `UsageBasedBillingPolicy`."""
  createUsageBasedBillingPolicyFreePeriod(input: CreateUsageBasedBillingPolicyFreePeriodMutationInput): UsageBasedBillingPolicyFreePeriod
  """
  Create a new user. The user will be sent an email with a temporary password after creation.
  """
  createUser(input: CreateUserMutationInput): User
  """Create a new vehicle."""
  createVehicle(input: CreateVehicleMutationInput): Vehicle
  """Create a vendor."""
  createVendor(input: CreateVendorMutationInput): Vendor
  """Create a vendor item."""
  createVendorItem(input: CreateVendorItemMutationInput): VendorItem
  """Create a voice provider."""
  createVoiceProvider(input: CreateVoiceProviderMutationInput): VoiceProvider
  """Create a voice provider rate."""
  createVoiceProviderRate(input: CreateVoiceProviderRateMutationInput): VoiceProviderRate
  """Create a Flatfile import of voice provider rates."""
  createVoiceProviderRateImportFlatfile(input: CreateVoiceProviderRateImportFlatfileMutationInput): VoiceProviderRateImportRecipe
  """Create a voice service."""
  createVoiceService(input: CreateVoiceServiceMutationInput): Service
  """Create a single voice service configuration parameter."""
  createVoiceServiceGenericParameter(input: CreateVoiceServiceGenericParameterMutationInput): VoiceServiceGenericParameter
  """Create a webhook endpoint."""
  createWebhookEndpoint(input: CreateWebhookEndpointMutationInput): WebhookEndpoint
  """Create a webhook endpoint event."""
  createWebhookEndpointEvent(input: CreateWebhookEndpointEventMutationInput): WebhookEndpointEvent
  """Delete account Adtran Mosaic service details."""
  deleteAccountAdtranMosaicServiceDetail(
    """fields.account_adtran_mosaic_service_detail_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an account calix service detail."""
  deleteAccountCalixServiceDetail(
    """fields.account_calix_service_detail_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an account group."""
  deleteAccountGroup(id: Int64Bit!): SuccessResponse
  """Delete a package from an account."""
  deleteAccountPackage(
    """
    A unique ID that describes this unique instance of a `Package` assignment.
    """
    unique_package_relationship_id: String!
    input: DeleteAccountServiceMutationInput
  ): SuccessResponse
  """Delete a service from an account."""
  deleteAccountService(
    """The ID of an AccountService."""
    id: Int64Bit!
    input: DeleteAccountServiceMutationInput
  ): SuccessResponse
  """Delete an account status."""
  deleteAccountStatus(id: Int64Bit!): SuccessResponse
  """Delete an account type."""
  deleteAccountType(id: Int64Bit!): SuccessResponse
  """Delete an account voice service detail."""
  deleteAccountVoiceServiceDetail(
    """The ID of an account voice service detail."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an ACH batch."""
  deleteAchBatch(
    """fields.ach_batch_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an address list."""
  deleteAddressList(
    """fields.address_list_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an address status."""
  deleteAddressStatus(
    """Address status ID."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete Adtran Mosaic settings."""
  deleteAdtranMosaicSetting(
    """The ID of an Adtran Mosaic setting."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an alerting rotation."""
  deleteAlertingRotation(
    """The alerting rotation ID."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an alerting rotation day."""
  deleteAlertingRotationDay(
    """The alerting rotation day and time ID."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an application firewall rule."""
  deleteApplicationFirewallRule(
    """fields.application_firewall_rule_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an authentication factor."""
  deleteAuthenticationFactor(
    """The ID of an `AuthenticationFactor`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a bank account."""
  deleteBankAccount(
    """The ID of a BankAccount."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a bank account processor."""
  deleteBankAccountProcessor(
    """The ID of a BankProcessor."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a billing default."""
  deleteBillingDefault(id: Int64Bit!): SuccessResponse
  """Delete a cable modem provisioner."""
  deleteCableModemProvisioner(
    """The ID of a `CableModemProvisioner`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a calendar - iCalendar."""
  deleteCalendarIcal(
    """fields.calendar_ical_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a Calix Cloud setting."""
  deleteCalixCloudSetting(
    """The ID of a `CalixCloudSetting`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a Calix integration"""
  deleteCalixIntegration(
    """Calix Inegartion ID."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a call detail record (CDR)."""
  deleteCallDetailRecord(
    """fields.call_detail_record_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a call log."""
  deleteCallLog(id: Int64Bit!): SuccessResponse
  """Delete a canned reply."""
  deleteCannedReply(
    """fields.canned_reply_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a canned reply category."""
  deleteCannedReplyCategory(
    """The ID of a `CannedReplyCategory`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a contact."""
  deleteContact(
    """The ID of the entity."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an unsigned contract."""
  deleteContract(
    """fields.contract_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a contract template."""
  deleteContractTemplate(
    """The ID of a `ContractTemplate`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a credit card."""
  deleteCreditCard(
    """The ID of the entity."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a credit card processor."""
  deleteCreditCardProcessor(
    """The ID of a CreditCardProcessor."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a custom field."""
  deleteCustomField(
    """The ID of the entity."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a custom link."""
  deleteCustomLink(
    """fields.custom_link_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a debit."""
  deleteDebit(
    input: DeleteTransactionMutationInput
    """The ID of a `Debit`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a delinquency exclusion."""
  deleteDelinquencyExclusion(
    """fields.delinquency_exclusion_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a department."""
  deleteDepartment(
    """The ID of a department."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a deployment type."""
  deleteDeploymentType(
    """The ID of a `DeploymentType`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a deposit slip."""
  deleteDepositSlip(
    """The deposit slip ID."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a DHCP server."""
  deleteDhcpServer(
    """The ID of a `DhcpServer`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a DHCP server identifier."""
  deleteDhcpServerIdentifier(
    """The ID of a `DhcpServerIdentifier`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a DID."""
  deleteDid(
    """The ID of a `Did`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a DID assignment."""
  deleteDidAssignment(
    """The ID of a `DidAssignment`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a discount."""
  deleteDiscount(
    input: DeleteTransactionMutationInput
    """The ID of a `Discount`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete n messaging category."""
  deleteEmailCategory(id: Int64Bit!): SuccessResponse
  """Delete an email domain."""
  deleteEmailDomain(
    """The ID of an `EmailDomain`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a saved message."""
  deleteEmailMessage(id: Int64Bit!): SuccessResponse
  """Delete saved message contents."""
  deleteEmailMessageContent(id: Int64Bit!): SuccessResponse
  """Delete an LTE EPC."""
  deleteEpc(
    """fields.epc_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an external marketing integration."""
  deleteExternalMarketingProvider(
    """The ID of an `ExternalMarketingProvider`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a FiberMap Integration."""
  deleteFibermapIntegration(
    """FiberMap integration ID"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a file."""
  deleteFile(
    """The ID of a `File`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a general ledger code."""
  deleteGeneralLedgerCode(id: Int64Bit!): SuccessResponse
  """Delete a generic inventory assignee."""
  deleteGenericInventoryAssignee(
    """fields.generic_inventory_assignee_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete generic inventory items."""
  deleteGenericInventoryItems(
    """fields.generic_inventory_item_id"""
    id: Int64Bit!
    input: DeleteGenericInventoryItemsMutationInput
  ): GenericInventoryItem
  """Delete a geo tax zone."""
  deleteGeoTaxZone(id: Int64Bit!): SuccessResponse
  """Delete a geofence."""
  deleteGeofence(
    """The ID of a `Geofence`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a Global Inventory Model Min/Max."""
  deleteGlobalInventoryModelMinMax(
    """fields.global_inventory_model_min_max_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a GPS tracking provider."""
  deleteGpsTrackingProvider(
    """A `GpsTrackingProvider` ID."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an identity provider."""
  deleteIdentityProvider(
    """The ID of an `IdentityProvider`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an inbound mailbox."""
  deleteInboundMailbox(
    """The ID of an `InboundMailbox`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an inline device."""
  deleteInlineDevice(
    """The ID of an `InlineDevice`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an internal location."""
  deleteInternalLocation(
    """fields.internal_location_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an inventory item."""
  deleteInventoryItem(
    """The ID of an `InventoryItem`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an inventory item segment."""
  deleteInventoryItemSegment(
    input: DeleteInventoryItemSegmentMutationInput
    """The ID of an `InventoryItem`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an inventory location."""
  deleteInventoryLocation(
    """The ID of an `InventoryLocation`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an inventory model."""
  deleteInventoryModel(
    """The ID of an `InventoryModel`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an inventory model category."""
  deleteInventoryModelCategory(
    """The ID of an InventoryModelCategory."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an inventory model field."""
  deleteInventoryModelField(
    """The ID of an `InventoryModelField`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an Inventory Model Min/Max."""
  deleteInventoryModelMinMax(
    """fields.inventory_model_min_max_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an invoice."""
  deleteInvoice(
    input: DeleteTransactionMutationInput
    """The ID of an `Invoice`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an invoice attachment."""
  deleteInvoiceAttachment(
    """fields.invoice_attachment_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an invoice message."""
  deleteInvoiceMessage(
    """The ID of an `InvoiceMessage`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an invoice template."""
  deleteInvoiceTemplate(
    """The ID of an Invoice Template."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an IP assignment."""
  deleteIpAssignment(
    """The ID of an `IpAssignment`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an IP pool."""
  deleteIpPool(
    """The ID of an `IpPool`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a job."""
  deleteJob(
    """The ID of a `Job`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a service from a job."""
  deleteJobService(
    """fields.job_service_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a job type."""
  deleteJobType(
    """The ID of a `JobType`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a local prefix."""
  deleteLocalPrefix(
    """The ID of a local prefix."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an LTE provider."""
  deleteLteProvider(
    """The ID of an `LteProvider`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an account mailing address."""
  deleteMailingAddress(
    """The ID of the address."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a manufacturer."""
  deleteManufacturer(
    """The ID of a Manufacturer."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a map overlay."""
  deleteMapOverlay(
    """The ID of a map overlay."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a messaging category."""
  deleteMessageCategory(
    """The ID of the entity."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a Netflow allowed subnet."""
  deleteNetflowAllowedSubnet(
    """fields.netflow_allowed_subnet_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a Netflow endpoint."""
  deleteNetflowEndpoint(
    """The ID of a `NetflowEndpoint`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a Netflow on premise record."""
  deleteNetflowOnPremise(
    """The ID of a `NetflowOnPremise` record."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a Netflow whitelist."""
  deleteNetflowWhitelist(
    """fields.netflow_whitelist_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a Network Monitoring Graph."""
  deleteNetworkMonitoringGraph(
    """The ID of a `NetworkMonitoringGraph`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a Network Monitoring Template."""
  deleteNetworkMonitoringTemplate(
    """The ID of a `NetworkMonitoringTemplate`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a network site."""
  deleteNetworkSite(
    """Network site id."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a non-inventory item."""
  deleteNonInventoryItem(
    """fields.non_inventory_item_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a note."""
  deleteNote(
    """The ID of the entity."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an order group."""
  deleteOrderGroup(
    """The ID of an order group."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a package."""
  deletePackage(
    """The ID of a `Package`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a PayPal credential."""
  deletePayPalCredential(
    """The ID of the entity."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a payment that was created without a payment method."""
  deletePayment(
    """The ID of a `Payment`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a personal access token."""
  deletePersonalAccessToken(
    """fields.personal_access_token_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a phone number."""
  deletePhoneNumber(
    """The ID of the entity."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a phone number type."""
  deletePhoneNumberType(id: Int64Bit!): SuccessResponse
  """Delete a poller."""
  deletePoller(
    """The ID of a `Poller`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a RADIUS account."""
  deleteRadiusAccount(
    """The ID of a `RadiusAccount`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a RADIUS group."""
  deleteRadiusGroup(
    """The ID of a `RadiusGroup`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a RADIUS group reply attribute."""
  deleteRadiusGroupReplyAttribute(
    """fields.radius_group_reply_attribute_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a RADIUS server."""
  deleteRadiusServer(
    """The ID of a `RadiusServer`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a rate center."""
  deleteRateCenter(
    """The ID of a `RateCenter`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a refunded payment."""
  deleteRefundedPayment(
    """fields.refunded_payment_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a reversed payment."""
  deleteReversedPayment(
    """fields.reversed_payment_id"""
    id: Int64Bit!
    input: DeleteReversedPaymentMutationInput
  ): SuccessResponse
  """Delete a role."""
  deleteRole(id: Int64Bit!): SuccessResponse
  """Delete a saved message category."""
  deleteSavedMessageCategory(
    """ID of the Saved Message Category."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a schedule address."""
  deleteScheduleAddress(
    """fields.schedule_address_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a schedule availability."""
  deleteScheduleAvailability(
    """The ID of a `ScheduleAvailability`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a schedule availability day/time."""
  deleteScheduleAvailabilityDayTime(
    """fields.schedule_availability_day_time_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a schedule blocker."""
  deleteScheduleBlocker(
    """The ID of a `ScheduleBlocker`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a schedule blocker day/time."""
  deleteScheduleBlockerDayTime(
    """fields.schedule_blocker_day_time_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a schedule time off."""
  deleteScheduleTimeOff(
    """fields.schedule_time_off_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a scheduled event."""
  deleteScheduledEvent(
    """The ID of a `ScheduledEvent`"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a saved search filter for the current user."""
  deleteSearchFilter(id: Int64Bit!): SuccessResponse
  """Delete a service."""
  deleteService(
    """The ID of a Service."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete service metadata."""
  deleteServiceMetadata(
    """The ID of a ServiceMetadata field."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a serviceable address."""
  deleteServiceableAddress(id: Int64Bit!): SuccessResponse
  """Delete a serviceable address account assignment future"""
  deleteServiceableAddressAccountAssignmentFuture(
    """The ID of the serviceable address account assignment future."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a Signature."""
  deleteSignature(
    """The ID of the entity."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an SNMP OID."""
  deleteSnmpOid(
    """The ID of an `SnmpOid`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an SNMP OID threshold."""
  deleteSnmpOidThreshold(
    """The ID of an `SnmpOidThreshold`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an SNMP override."""
  deleteSnmpOverride(
    """fields.snmp_override_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a stored view."""
  deleteStoredView(
    """The ID of a `StoredView` entity."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a subnet."""
  deleteSubnet(
    """The ID of a `Subnet`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a subscription."""
  deleteSubscription(
    """The ID of the entity."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a supernet."""
  deleteSupernet(
    """The ID of a `Supernet`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a system backup destination."""
  deleteSystemBackupDestination(
    """The ID of a destination that a system backup can be exported to."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a task."""
  deleteTask(
    """The ID of the entity."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a task template."""
  deleteTaskTemplate(
    """The ID of a `TaskTemplate`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a task template item."""
  deleteTaskTemplateItem(
    """The ID of a `TaskTemplateItem`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a tax."""
  deleteTax(id: Int64Bit!): SuccessResponse
  """Delete a tax exemption."""
  deleteTaxExemption(
    """fields.tax_exemption_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a tax override."""
  deleteTaxOverride(
    """fields.tax_override_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a tax provider."""
  deleteTaxProvider(
    """The ID of an `TaxProvider`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a ticket."""
  deleteTicket(
    """The ID of a `Ticket`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a ticket category."""
  deleteTicketCategory(
    """fields.ticket_category_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a ticket comment."""
  deleteTicketComment(
    """fields.ticket_comment_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a ticket group."""
  deleteTicketGroup(
    """The ID of a `TicketGroup`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a ticket recipient."""
  deleteTicketRecipient(
    """fields.ticket_recipient_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete multiple tickets."""
  deleteTickets(
    """The IDs of multiple `Ticket`s."""
    ids: [Int64Bit!]!
  ): SuccessResponse
  """
  DEPRECATED: Delete a triggered email. See deleteTriggeredMessageMutation.
  """
  deleteTriggeredEmail(id: Int64Bit!): SuccessResponse
  """Delete a triggered message."""
  deleteTriggeredMessage(
    """The ID of a `TriggeredMessage`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete an uninventoried MAC address."""
  deleteUninventoriedMacAddress(
    """fields.uninventoried_mac_address_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a usage based billing policy."""
  deleteUsageBasedBillingPolicy(
    """The ID of a `UsageBasedBillingPolicy`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a usage based billing policy free period."""
  deleteUsageBasedBillingPolicyFreePeriod(
    """fields.usage_based_billing_policy_free_period_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a vehicle."""
  deleteVehicle(
    """The ID of a `Vehicle`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a vendor item."""
  deleteVendorItem(
    """The ID of a vendor item."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a voice provider."""
  deleteVoiceProvider(
    """The ID of a `VoiceProvider`."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a voice provider rate."""
  deleteVoiceProviderRate(
    """The ID of a `VoiceProviderRate`"""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a single voice service configuration parameter."""
  deleteVoiceServiceGenericParameter(
    """The ID of a voice service configuration parameter."""
    id: Int64Bit!
    input: DeleteVoiceServiceGenericParameterMutationInput
  ): SuccessResponse
  """Delete a webhook endpoint."""
  deleteWebhookEndpoint(
    """The ID of a webhook endpoint."""
    id: Int64Bit!
  ): SuccessResponse
  """Delete a webhook endpoint event."""
  deleteWebhookEndpointEvent(
    """The model and event attached to the webhook endpoint"""
    id: Int64Bit!
  ): SuccessResponse
  """Disconnect an account."""
  disconnectAccount(
    input: DisconnectAccountMutationInput
    """The ID of an Account."""
    id: Int64Bit!
  ): Account
  """Disconnect a RADIUS session."""
  disconnectRadiusSession(
    """The ID of a `RadiusSessionHistory`."""
    id: Int64Bit!
  ): RadiusSessionHistory
  """Resend emailed invoices."""
  emailInvoiceBatch(input: EmailInvoiceBatchMutationInput): SuccessResponse
  """Email an invoice to a contact manually."""
  emailInvoiceToContact(input: EmailInvoiceToContactMutationInput): SuccessResponse
  """Email an approved purchase order to its vendor."""
  emailPurchaseOrderToVendor(
    """The ID of a purchase order."""
    id: Int64Bit!
  ): SuccessResponse
  """Generate import credentials for use with Flatfile."""
  generateImportCredentialsFlatfile(input: GenerateImportCredentialsFlatfileMutationInput): ImportCredentialsFlatfile
  """Generate Splice Report from Vetro FiberMap."""
  generateSpliceReport(
    """The ID of the address."""
    id: Int64Bit!
  ): SuccessResponse
  """mutations.generateTestWebhookMutation"""
  generateTestWebhook(
    """The ID of a webhook endpoint."""
    id: Int64Bit!
  ): WebhookTestResponse
  """Link a parent and child account."""
  linkAccounts(
    input: LinkAccountsMutationInput
    """The ID of the `Account` that is this `Account`s master."""
    id: Int64Bit!
  ): Account
  """Link Calix Cloud subscriber to Sonar account."""
  linkCalixCloudSubscriberToAccount(input: LinkCalixCloudSubscriberToAccountMutationInput): SuccessResponse
  """Link an entity to a ticket."""
  linkEntityToTicket(
    input: LinkEntityToTicketMutationInput
    """The ID of a `Ticket`."""
    id: Int64Bit!
  ): Ticket
  """Link Fibermap Plan To Network Site"""
  linkFibermapPlanToNetworkSite(input: LinkFibermapPlanToNetworkSiteMutationInput): NetworkSite
  """Link Fibermap Service Location To Address"""
  linkFibermapServiceLocationToAddress(input: LinkFibermapServiceLocationToAddressMutationInput): Address
  """Link a file to an entity."""
  linkFileToEntity(input: LinkFileToEntityMutationInput): FileableInterface
  """Link an inventory item to an account service."""
  linkInventoryItemToAccountService(input: LinkInventoryItemToAccountServiceMutationInput): SuccessResponse
  """Link inventory model to account services."""
  linkInventoryModelToAccountServices(input: LinkInventoryModelToAccountServicesMutationInput): SuccessResponse
  """Link a parent and child invoice."""
  linkInvoices(
    input: LinkInvoicesMutationInput
    """The ID of the `Invoice` that is this `Invoice`s master."""
    id: Int64Bit!
  ): Invoice
  """
  Link a TowerCoverage submission to a new or existing serviceable address.
  """
  linkTowercoverageSubmissionToServiceableAddressMutation(
    input: LinkTowercoverageSubmissionToServiceableAddressMutationInput
    """The ID of a `TowercoverageSubmission`."""
    id: Int64Bit!
  ): TowercoverageSubmission
  """Merge two subnets together."""
  mergeSubnets(input: MergeSubnetsMutationInput): Subnet
  """Merge multiple tickets into one."""
  mergeTickets(
    input: MergeTicketsMutationInput
    """The ID of a `Ticket`."""
    id: Int64Bit!
  ): Ticket
  """Publish a report."""
  publishReport(dashboard_id: String!): AvailableReport
  """Forced reboot of an inventory item"""
  rebootInventoryItem(
    """The ID of an `InventoryItem`."""
    inventory_item_id: Int64Bit!
  ): InventoryItem
  """Recalculate the next recurring charge amount of an account."""
  recalculateNextRecurringChargeAmount(input: RecalculateNextRecurringChargeAmountMutationInput): SuccessResponse
  """Receive a list of purchase order items into an inventory location."""
  receivePurchaseOrderItems(input: ReceivePurchaseOrderItemsMutationInput): [InventoryItem]
  """
  Re-enroll an authentication factor, resending the one-time password verification message if applicable.
  """
  reenrollAuthenticationFactor(
    """The ID of an `AuthenticationFactor`."""
    id: Int64Bit!
  ): SuccessResponse
  """Refund a payment."""
  refundPayment(
    input: RefundPaymentMutationInput
    """The ID of a `Payment`."""
    id: Int64Bit!
  ): RefundedPayment
  """Reindex a model in elastic."""
  reindexModel(input: ReindexModelMutationInput): SuccessResponse
  """Reschedule a schedule blocker."""
  rescheduleScheduleBlocker(input: RescheduleScheduleBlockerMutationInput): ScheduleBlockerOverride
  """Resend a ticket autoreply email."""
  resendAutoreply(input: ResendAutoreplyMutationInput): SuccessResponse
  """Resend a copy of a contract."""
  resendContract(
    """fields.contract_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Resend a failed print to mail batch."""
  resendPrintToMailBatch(
    """The ID of the print to mail batch."""
    id: Int64Bit!
  ): SuccessResponse
  """Resend the initial setup email to a newly created user."""
  resendUserCreationEmail(
    """The ID of a User."""
    user_id: Int64Bit!
  ): SuccessResponse
  """Software reset connection of an inventory item"""
  resetInventoryItem(
    """The ID of an `InventoryItem`."""
    inventory_item_id: Int64Bit!
  ): InventoryItem
  """Respond to an instance management request."""
  respondToInstanceManagementRequest(
    input: RespondToInstanceManagementRequestMutationInput
    """fields.instance_management_request_id"""
    id: Int64Bit!
  ): InstanceManagementRequest
  """
  Retries the creation of an address from a specific unmapped Vetro Fibermap Service location.
  """
  resyncFibermapServiceLocationToAddress(input: ResyncFibermapServiceLocationToAddressMutationInput): FibermapServiceLocation
  """Reverse a debit."""
  reverseDebit(
    input: ReverseTransactionMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): Debit
  """Reverse a discount."""
  reverseDiscount(
    input: ReverseTransactionMutationInput
    """The ID of a `Discount`."""
    id: Int64Bit!
  ): Discount
  """Reverse a payment."""
  reversePayment(
    input: ReversePaymentMutationInput
    """The ID of a `Payment`."""
    id: Int64Bit!
  ): ReversedPayment
  """Schedule many jobs and schedule blocker overrides at the same time."""
  scheduleManyJobsAndScheduleBlockerOverrides(input: ScheduleManyJobsAndScheduleBlockerOverridesMutationInput): SuccessResponse
  """
  Schedule jobs and schedule blocker overrides and skip scheduling validations
  """
  scheduleManyJobsAndScheduleBlockerOverridesSkipsValidation(input: ScheduleManyJobsAndScheduleBlockerOverridesMutationInput): SuccessResponse
  """Send an email to verify an email domain."""
  sendEmailDomainVerificationEmail(
    input: SendEmailDomainVerificationEmailMutationInput
    """The ID of an `EmailDomain`."""
    id: Int64Bit!
  ): SuccessResponse
  """mutations.sendTestEmailMutation"""
  sendTestEmail(
    input: SendTestEmailMutationInput
    """The ID of an `EmailDomain`."""
    id: Int64Bit!
  ): SuccessResponse
  """mutations.sendTestTriggeredEmailMutation"""
  sendTestTriggeredEmail(
    input: SendTestTriggeredEmailMutationInput
    """fields.triggered_email_id"""
    id: Int64Bit!
  ): SuccessResponse
  """Set the active stored view."""
  setActiveStoredView(input: SetActiveStoredViewMutationInput): SuccessResponse
  """Split a subnet in half."""
  splitSubnet(
    """The ID of the entity."""
    id: Int64Bit!
  ): [Subnet]
  """Synchronize a cable modem provisioner."""
  synchronizeCableModemProvisioner(input: SynchronizeCableModemProvisionerMutationInput): CableModemProvisioner
  """Synchronize Calix Cloud setting."""
  synchronizeCalixCloud(input: SynchronizeCalixCloudMutationInput): CalixCloudSetting
  """Full synchronization of a Calix integration"""
  synchronizeCalixIntegration(
    """Calix Inegartion ID."""
    calix_integration_id: Int64Bit!
  ): CalixIntegration
  """
  Removes all existing leases and writes new ones based on existing IP assignments.
  """
  synchronizeDhcpServer(input: SynchronizeDhcpServerMutationInput): DhcpServer
  """Synchronize a Fibermap Integration"""
  synchronizeFibermapIntegration(
    """FiberMap integration ID"""
    fibermap_integration_id: Int64Bit!
  ): FibermapIntegration
  """Synchronize an inline device."""
  synchronizeInlineDevice(input: SynchronizeInlineDeviceMutationInput): InlineDevice
  """Synchronize an LTE provider."""
  synchronizeLteProvider(input: SynchronizeLteProviderMutationInput): LteProvider
  """Synchronize a RADIUS server."""
  synchronizeRadiusServer(input: SynchronizeRadiusServerMutationInput): RadiusServer
  """Perform Sonar takeover of Adtran Mosaic Cloud."""
  takeoverAdtranMosaic(input: TakeoverAdtranMosaicMutationInput): AdtranMosaicSetting
  """Toggle all notifications as read or unread."""
  toggleAllNotifications(input: ToggleAllNotificationsMutationInput): SuccessResponse
  """Toggle notifications as read or unread."""
  toggleNotifications(input: ToggleNotificationsMutationInput): SuccessResponse
  """Unarchive an account."""
  unarchiveAccount(
    """The ID of the entity."""
    id: Int64Bit!
  ): Account
  """Unclaim one or many inventory items."""
  unclaimInventoryItems(input: UnclaimInventoryItemsMutationInput): SuccessResponse
  """Unlink a parent and child account."""
  unlinkAccounts(
    """The ID of a child `Account`."""
    id: Int64Bit!
  ): Account
  """Unlink an entity from a ticket."""
  unlinkEntityFromTicket(
    input: UnlinkEntityFromTicketMutationInput
    """The ID of a `Ticket`."""
    id: Int64Bit!
  ): Ticket
  """Unlink a parent and child invoice."""
  unlinkInvoices(
    """The ID of a child `Invoice`."""
    id: Int64Bit!
  ): Invoice
  """Update an account."""
  updateAccount(
    input: UpdateAccountMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): Account
  """Update a previously activated accounts activation date."""
  updateAccountActivationDate(
    input: UpdateAccountActivationDateMutationInput
    """The ID of an Account."""
    id: Int64Bit!
  ): Account
  """Update account Adtran Mosaic service details."""
  updateAccountAdtranMosaicServiceDetail(
    input: UpdateAccountAdtranMosaicServiceDetailMutationInput
    """fields.account_adtran_mosaic_service_detail_id"""
    id: Int64Bit!
  ): AccountAdtranMosaicServiceDetail
  """Update a variety of account billing parameters."""
  updateAccountBillingParameter(
    input: UpdateAccountBillingParameterMutationInput
    """The ID of an Account."""
    account_id: Int64Bit!
  ): AccountBillingParameter
  """Update an account calix service detail."""
  updateAccountCalixServiceDetail(
    input: UpdateAccountCalixServiceDetailMutationInput
    """fields.account_calix_service_detail_id"""
    id: Int64Bit!
  ): AccountCalixServiceDetail
  """Update an account group."""
  updateAccountGroup(
    input: UpdateAccountGroupMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): AccountGroup
  """Update an account service."""
  updateAccountService(
    input: UpdateAccountServiceMutationInput
    """The ID of an AccountService."""
    id: Int64Bit!
  ): AccountService
  """Update an account status."""
  updateAccountStatus(
    input: UpdateAccountStatusMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): AccountStatus
  """Update an account type."""
  updateAccountType(
    input: UpdateAccountTypeMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): AccountType
  """Update an account voice service detail."""
  updateAccountVoiceServiceDetail(
    input: UpdateAccountVoiceServiceDetailMutationInput
    """The ID of an account voice service detail."""
    id: Int64Bit!
  ): AccountVoiceServiceDetail
  """Update an address list."""
  updateAddressList(
    input: UpdateAddressListMutationInput
    """fields.address_list_id"""
    id: Int64Bit!
  ): AddressList
  """Update an address status."""
  updateAddressStatus(
    input: UpdateAddressStatusMutationInput
    """Address status ID."""
    id: Int64Bit!
  ): AddressStatus
  """Update an adjustment service."""
  updateAdjustmentService(
    input: UpdateAdjustmentServiceMutationInput
    """The ID of a Service."""
    id: Int64Bit!
  ): Service
  """Update Adtran Mosaic audit."""
  updateAdtranMosaicAudit(
    input: UpdateAdtranMosaicAuditMutationInput
    """The ID of an Adtran Mosaic audit record."""
    id: Int64Bit!
  ): AdtranMosaicAudit
  """Update Adtran Mosaic settings."""
  updateAdtranMosaicSetting(
    input: UpdateAdtranMosaicSettingMutationInput
    """The ID of an Adtran Mosaic setting."""
    id: Int64Bit!
  ): AdtranMosaicSetting
  """Update an alerting rotation."""
  updateAlertingRotation(
    input: UpdateAlertingRotationMutationInput
    """The alerting rotation ID."""
    id: Int64Bit!
  ): AlertingRotation
  """Update an alerting rotation day."""
  updateAlertingRotationDay(
    input: UpdateAlertingRotationDayMutationInput
    """The alerting rotation day and time ID."""
    id: Int64Bit!
  ): AlertingRotationDay
  """Update an application firewall rule."""
  updateApplicationFirewallRule(
    input: UpdateApplicationFirewallRuleMutationInput
    """fields.application_firewall_rule_id"""
    id: Int64Bit!
  ): ApplicationFirewallRule
  """Update an auth provider."""
  updateAuthProvider(
    input: UpdateAuthProviderMutationInput
    """The ID of an `AuthProvider`."""
    id: Int64Bit!
  ): AuthProvider
  """Update an authentication factor."""
  updateAuthenticationFactor(
    input: UpdateAuthenticationFactorMutationInput
    """The ID of an `AuthenticationFactor`."""
    id: Int64Bit!
  ): AuthenticationFactor
  """Update an Avalara bundled tax definition."""
  updateAvalaraTaxDefinition(
    input: UpdateAvalaraTaxDefinitionMutationInput
    """fields.avalara_tax_definition_id"""
    id: Int64Bit!
  ): AvalaraTaxDefinition
  """Update a bank account."""
  updateBankAccount(
    input: UpdateBankAccountMutationInput
    """The ID of a BankAccount."""
    id: Int64Bit!
  ): BankAccount
  """Update a bank account processor."""
  updateBankAccountProcessor(
    input: UpdateBankAccountProcessorMutationInput
    """The ID of a BankProcessor."""
    id: Int64Bit!
  ): BankAccountProcessor
  """Update a billing default."""
  updateBillingDefault(
    input: UpdateBillingDefaultMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): BillingDefault
  """Update the system billing settings."""
  updateBillingSettings(input: UpdateBillingSettingsMutationInput): BillingSetting
  """Update a cable modem provisioner."""
  updateCableModemProvisioner(
    input: UpdateCableModemProvisionerMutationInput
    """The ID of a `CableModemProvisioner`."""
    id: Int64Bit!
  ): CableModemProvisioner
  """Update a calendar - iCalendar."""
  updateCalendarIcal(
    input: UpdateCalendarIcalMutationInput
    """fields.calendar_ical_id"""
    id: Int64Bit!
  ): CalendarIcal
  """Update a iCalendar calendar token"""
  updateCalendarIcalToken(
    """fields.calendar_ical_id"""
    id: Int64Bit!
  ): CalendarIcal
  """Update system settings related to calendars."""
  updateCalendarSystemSettings(input: UpdateCalendarSystemSettingsMutationInput): SystemSetting
  """Update a Calix Cloud setting."""
  updateCalixCloudSetting(
    input: UpdateCalixCloudSettingMutationInput
    """The ID of a `CalixCloudSetting`."""
    id: Int64Bit!
  ): CalixCloudSetting
  """Update a Calix integration"""
  updateCalixIntegration(
    input: UpdateCalixIntegrationMutationInput
    """Calix Inegartion ID."""
    id: Int64Bit!
  ): CalixIntegration
  """Update a call detail record (CDR)."""
  updateCallDetailRecord(
    input: UpdateCallDetailRecordMutationInput
    """fields.call_detail_record_id"""
    id: Int64Bit!
  ): CallDetailRecord
  """Update a call log."""
  updateCallLog(
    input: UpdateCallLogMutationInput
    """The ID of a `CallLog`."""
    id: Int64Bit!
  ): CallLog
  """Update a canned reply."""
  updateCannedReply(
    input: UpdateCannedReplyMutationInput
    """fields.canned_reply_id"""
    id: Int64Bit!
  ): CannedReply
  """Update a canned reply category."""
  updateCannedReplyCategory(
    input: UpdateCannedReplyCategoryMutationInput
    """The ID of a `CannedReplyCategory`."""
    id: Int64Bit!
  ): CannedReplyCategory
  """Update a company."""
  updateCompany(
    input: UpdateCompanyMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): Company
  """Update a contact."""
  updateContact(
    input: UpdateContactMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): Contact
  """Update a contract."""
  updateContract(
    input: UpdateContractMutationInput
    """fields.contract_id"""
    id: Int64Bit!
  ): Contract
  """Update a contract template."""
  updateContractTemplate(
    input: UpdateContractTemplateMutationInput
    """The ID of a `ContractTemplate`."""
    id: Int64Bit!
  ): ContractTemplate
  """Update a credit card."""
  updateCreditCard(
    input: UpdateCreditCardMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): CreditCard
  """Update a credit card processor."""
  updateCreditCardProcessor(
    input: UpdateCreditCardProcessorMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): CreditCardProcessor
  """Update a custom field."""
  updateCustomField(
    input: UpdateCustomFieldMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): CustomField
  """Update a custom link."""
  updateCustomLink(
    input: UpdateCustomLinkMutationInput
    """fields.custom_link_id"""
    id: Int64Bit!
  ): CustomLink
  """Update a data service."""
  updateDataService(
    input: UpdateDataServiceMutationInput
    """The ID of a Service."""
    id: Int64Bit!
  ): Service
  """Update a data usage history record."""
  updateDataUsageHistory(
    input: UpdateDataUsageHistoryMutationInput
    """The ID of a `DataUsageHistory`."""
    id: Int64Bit!
  ): DataUsageHistory
  """Update a debit."""
  updateDebit(
    input: UpdateDebitMutationInput
    """The ID of a `Debit`."""
    id: Int64Bit!
  ): Debit
  """Update a delinquency exclusion."""
  updateDelinquencyExclusion(
    input: UpdateDelinquencyExclusionMutationInput
    """fields.delinquency_exclusion_id"""
    id: Int64Bit!
  ): DelinquencyExclusion
  """Update a department."""
  updateDepartment(
    input: UpdateDepartmentMutationInput
    """The ID of a department."""
    id: Int64Bit!
  ): Department
  """Update a deployment type."""
  updateDeploymentType(
    input: UpdateDeploymentTypeMutationInput
    """The ID of a `DeploymentType`."""
    id: Int64Bit!
  ): DeploymentType
  """Update a deposit slip."""
  updateDepositSlip(
    input: UpdateDepositSlipMutationInput
    """The deposit slip ID."""
    id: Int64Bit!
  ): DepositSlip
  """Update a DHCP server."""
  updateDhcpServer(
    input: UpdateDhcpServerMutationInput
    """The ID of a `DhcpServer`."""
    id: Int64Bit!
  ): DhcpServer
  """Update a DHCP server identifier."""
  updateDhcpServerIdentifier(
    input: UpdateDhcpServerIdentifierMutationInput
    """The ID of a `DhcpServerIdentifier`."""
    id: Int64Bit!
  ): DhcpServerIdentifier
  """Update a DID."""
  updateDid(
    input: UpdateDidMutationInput
    """The ID of a `Did`."""
    id: Int64Bit!
  ): Did
  """Update a DID assignment."""
  updateDidAssignment(
    input: UpdateDidAssignmentMutationInput
    """The ID of a `DidAssignment`."""
    id: Int64Bit!
  ): DidAssignment
  """Update a discount."""
  updateDiscount(
    input: UpdateDiscountMutationInput
    """The ID of a `Discount`."""
    id: Int64Bit!
  ): Discount
  """Update the assigned drivers on a vehicle."""
  updateDrivers(
    input: UpdateDriversMutationInput
    """The ID of a `Vehicle`."""
    id: Int64Bit!
  ): Vehicle
  """Update a messaging category."""
  updateEmailCategory(
    input: UpdateEmailCategoryMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): EmailCategory
  """Update a saved message."""
  updateEmailMessage(
    input: UpdateEmailMessageMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): EmailMessage
  """Update saved message contents."""
  updateEmailMessageContent(
    input: UpdateEmailMessageContentMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): EmailMessageContent
  """Update the custom fields on an entity."""
  updateEntityCustomFields(
    input: UpdateEntityCustomFieldsMutationInput
    """The type of entity that owns this custom field data."""
    customfielddataable_type: CustomfielddataableType!
    """The ID of the entity that owns this custom field data."""
    customfielddataable_id: Int64Bit!
  ): [CustomFieldData]
  """Update an LTE EPC."""
  updateEpc(
    input: UpdateEpcMutationInput
    """fields.epc_id"""
    id: Int64Bit!
  ): Epc
  """Update an expiring service."""
  updateExpiringService(
    input: UpdateExpiringServiceMutationInput
    """The ID of a Service."""
    id: Int64Bit!
  ): Service
  """Update an external marketing integration."""
  updateExternalMarketingProvider(
    input: UpdateExternalMarketingProviderMutationInput
    """The ID of an `ExternalMarketingProvider`."""
    id: Int64Bit!
  ): ExternalMarketingProvider
  """Update a FiberMap Integration."""
  updateFibermapIntegration(
    input: UpdateFibermapIntegrationMutationInput
    """FiberMap integration ID"""
    id: Int64Bit!
  ): FibermapIntegration
  """Update a Fibermap Plan."""
  updateFibermapPlan(
    input: UpdateFibermapPlanMutationInput
    """FiberMap plan ID"""
    id: Int64Bit!
  ): FibermapPlan
  """Update a Fibermap Service Location."""
  updateFibermapServiceLocation(
    input: UpdateFibermapServiceLocationMutationInput
    """Fibermap service location ID."""
    id: Int64Bit!
  ): FibermapServiceLocation
  """Update a file."""
  updateFile(
    input: UpdateFileMutationInput
    """The ID of a `File`."""
    id: Int64Bit!
  ): File
  """Update a general ledger code."""
  updateGeneralLedgerCode(
    input: UpdateGeneralLedgerCodeMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): GeneralLedgerCode
  """Update a generic inventory assignee."""
  updateGenericInventoryAssignee(
    input: UpdateGenericInventoryAssigneeMutationInput
    """fields.generic_inventory_assignee_id"""
    id: Int64Bit!
  ): GenericInventoryAssignee
  """Update a geo tax zone."""
  updateGeoTaxZone(
    input: UpdateGeoTaxZoneMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): GeoTaxZone
  """Update a geofence."""
  updateGeofence(
    input: UpdateGeofenceMutationInput
    """The ID of a `Geofence`."""
    id: Int64Bit!
  ): Geofence
  """Update a Global Inventory Model Min/Max."""
  updateGlobalInventoryModelMinMax(
    input: UpdateGlobalInventoryModelMinMaxMutationInput
    """fields.global_inventory_model_min_max_id"""
    id: Int64Bit!
  ): GlobalInventoryModelMinMax
  """Update a GPS tracking provider."""
  updateGpsTrackingProvider(
    input: UpdateGpsTrackingProviderMutationInput
    """A `GpsTrackingProvider` ID."""
    id: Int64Bit!
  ): GpsTrackingProvider
  """Update an ActiveDirectory identity provider."""
  updateIdentityProviderActiveDirectory(
    input: UpdateIdentityProviderActiveDirectoryMutationInput
    """The ID of an `IdentityProvider`."""
    id: Int64Bit!
  ): IdentityProvider
  """Update a Google identity provider."""
  updateIdentityProviderGoogle(
    input: UpdateIdentityProviderGoogleMutationInput
    """The ID of an `IdentityProvider`."""
    id: Int64Bit!
  ): IdentityProvider
  """Update a Microsoft identity provider."""
  updateIdentityProviderMicrosoft(
    input: UpdateIdentityProviderMicrosoftMutationInput
    """The ID of an `IdentityProvider`."""
    id: Int64Bit!
  ): IdentityProvider
  """Update a SAML identity provider."""
  updateIdentityProviderSaml(
    input: UpdateIdentityProviderSamlMutationInput
    """The ID of an `IdentityProvider`."""
    id: Int64Bit!
  ): IdentityProvider
  """Update an inbound mailbox."""
  updateInboundMailbox(
    input: UpdateInboundMailboxMutationInput
    """The ID of an `InboundMailbox`."""
    id: Int64Bit!
  ): InboundMailbox
  """Update an inline device."""
  updateInlineDevice(
    input: UpdateInlineDeviceMutationInput
    """The ID of an `InlineDevice`."""
    id: Int64Bit!
  ): InlineDevice
  """Update the autopay setting for an instance service fund."""
  updateInstanceServiceFundAutoPay(input: UpdateInstanceServiceFundAutoPayMutationInput): InstanceServiceFundAutoPay!
  """Update an internal location."""
  updateInternalLocation(
    input: UpdateInternalLocationMutationInput
    """fields.internal_location_id"""
    id: Int64Bit!
  ): InternalLocation
  """Update an inventory item."""
  updateInventoryItem(
    input: UpdateInventoryItemsMutationInput
    """The ID of an `InventoryItem`."""
    id: Int64Bit!
  ): InventoryItem
  """Update the contents of inventory item model fields."""
  updateInventoryItemFields(
    input: UpdateInventoryItemFieldsMutationInput
    """The ID of an `InventoryItem`."""
    id: Int64Bit!
  ): InventoryItem
  """Update an inventory item segment."""
  updateInventoryItemSegment(
    input: UpdateInventoryItemSegmentMutationInput
    """The ID of an `InventoryItem`."""
    id: Int64Bit!
  ): [InventoryItem]
  """Update an Inventory Item status."""
  updateInventoryItemStatus(
    input: UpdateInventoryItemStatusMutationInput
    """The ID of an `InventoryItem`."""
    id: Int64Bit!
  ): InventoryItem
  """Update one or more inventory items."""
  updateInventoryItems(
    input: UpdateInventoryItemsMutationInput
    """IDs of `InventoryItem`s."""
    ids: [Int64Bit!]!
  ): [InventoryItem]
  """Update an inventory location."""
  updateInventoryLocation(
    input: UpdateInventoryLocationMutationInput
    """The ID of an `InventoryLocation`."""
    id: Int64Bit!
  ): InventoryLocation
  """Update an inventory model."""
  updateInventoryModel(
    input: UpdateInventoryModelMutationInput
    """The ID of an `InventoryModel`."""
    id: Int64Bit!
  ): InventoryModel
  """Update an inventory model category."""
  updateInventoryModelCategory(
    input: UpdateInventoryModelCategoryMutationInput
    """The ID of an InventoryModelCategory."""
    id: Int64Bit!
  ): InventoryModelCategory
  """Update an inventory model field."""
  updateInventoryModelField(
    input: UpdateInventoryModelFieldMutationInput
    """The ID of an `InventoryModelField`."""
    id: Int64Bit!
  ): InventoryModelField
  """Update an Inventory Model Min/Max."""
  updateInventoryModelMinMax(
    input: UpdateInventoryModelMinMaxMutationInput
    """fields.inventory_model_min_max_id"""
    id: Int64Bit!
  ): InventoryModelMinMax
  """Update an invoice."""
  updateInvoice(
    input: UpdateInvoiceMutationInput
    """The ID of an `Invoice`."""
    id: Int64Bit!
  ): Invoice
  """Update an invoice attachment."""
  updateInvoiceAttachment(
    input: UpdateInvoiceAttachmentMutationInput
    """fields.invoice_attachment_id"""
    id: Int64Bit!
  ): InvoiceAttachment
  """Update an invoice message."""
  updateInvoiceMessage(
    input: UpdateInvoiceMessageMutationInput
    """The ID of an `InvoiceMessage`."""
    id: Int64Bit!
  ): InvoiceMessage
  """Update an invoice template."""
  updateInvoiceTemplate(
    input: UpdateInvoiceTemplateMutationInput
    """The ID of an Invoice Template."""
    id: Int64Bit!
  ): InvoiceTemplate
  """Update an IP assignment."""
  updateIpAssignment(
    input: UpdateIpAssignmentMutationInput
    """The ID of an `IpAssignment`."""
    id: Int64Bit!
  ): IpAssignment
  """Update an IP pool."""
  updateIpPool(
    input: UpdateIpPoolMutationInput
    """The ID of an `IpPool`."""
    id: Int64Bit!
  ): IpPool
  """Update a job."""
  updateJob(
    input: UpdateJobMutationInput
    """The ID of a `Job`."""
    id: Int64Bit!
  ): Job
  """Update the quantity of a service associated with a job."""
  updateJobService(
    input: UpdateJobServiceMutationInput
    """fields.job_service_id"""
    id: Int64Bit!
  ): JobService
  """Update a job skipping validation."""
  updateJobSkipsValidation(
    input: UpdateJobMutationInput
    """The ID of a `Job`."""
    id: Int64Bit!
  ): Job
  """Update a job type."""
  updateJobType(
    input: UpdateJobTypeMutationInput
    """The ID of a `JobType`."""
    id: Int64Bit!
  ): JobType
  """Update a local prefix."""
  updateLocalPrefix(
    input: UpdateLocalPrefixMutationInput
    """The ID of a local prefix."""
    id: Int64Bit!
  ): LocalPrefix
  """Update a report builder license."""
  updateLookerExploreLicense(
    input: UpdateLookerExploreLicenseMutationInput
    """fields.looker_explore_license_id"""
    id: Int64Bit!
  ): LookerExploreLicense
  """Update a report viewer license."""
  updateLookerViewLicense(
    input: UpdateLookerViewLicenseMutationInput
    """fields.looker_view_license_id"""
    id: Int64Bit!
  ): LookerViewLicense
  """Update an LTE provider."""
  updateLteProvider(
    input: UpdateLteProviderMutationInput
    """The ID of an `LteProvider`."""
    id: Int64Bit!
  ): LteProvider
  """Update an account mailing address."""
  updateMailingAddress(
    input: UpdateMailingAddressMutationInput
    """The ID of the address."""
    id: Int64Bit!
  ): Address
  """Update a manufacturer."""
  updateManufacturer(
    input: UpdateManufacturerMutationInput
    """The ID of a Manufacturer."""
    id: Int64Bit!
  ): Manufacturer
  """Update a map overlay."""
  updateMapOverlay(
    input: UpdateMapOverlayMutationInput
    """The ID of a map overlay."""
    id: Int64Bit!
  ): MapOverlay
  """Update your user profile."""
  updateMe(input: UpdateMeMutationInput): Me
  """Update a messaging category."""
  updateMessageCategory(
    input: UpdateMessageCategoryMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): MessageCategory
  """Update the multi-factor authentication admin settings."""
  updateMfaAdminSettings(input: UpdateMfaAdminSettingsMutationInput): MfaAdminSetting
  """Update a Netflow allowed subnet."""
  updateNetflowAllowedSubnet(
    input: UpdateNetflowAllowedSubnetMutationInput
    """fields.netflow_allowed_subnet_id"""
    id: Int64Bit!
  ): NetflowAllowedSubnet
  """Update a Netflow endpoint."""
  updateNetflowEndpoint(
    input: UpdateNetflowEndpointMutationInput
    """The ID of a `NetflowEndpoint`."""
    id: Int64Bit!
  ): NetflowEndpoint
  """Update a Netflow on premise record."""
  updateNetflowOnPremise(
    input: UpdateNetflowOnPremiseMutationInput
    """The ID of a `NetflowOnPremise` record."""
    id: Int64Bit!
  ): NetflowOnPremise
  """Update a Netflow whitelist."""
  updateNetflowWhitelist(
    input: UpdateNetflowWhitelistMutationInput
    """fields.netflow_whitelist_id"""
    id: Int64Bit!
  ): NetflowWhitelist
  """Update a Network Monitoring Graph."""
  updateNetworkMonitoringGraph(
    input: UpdateNetworkMonitoringGraphMutationInput
    """The ID of a `NetworkMonitoringGraph`."""
    id: Int64Bit!
  ): NetworkMonitoringGraph
  """Update a Network Monitoring Template."""
  updateNetworkMonitoringTemplate(
    input: UpdateNetworkMonitoringTemplateMutationInput
    """The ID of a `NetworkMonitoringTemplate`."""
    id: Int64Bit!
  ): NetworkMonitoringTemplate
  """Update a network site."""
  updateNetworkSite(
    input: UpdateNetworkSiteMutationInput
    """Network site id."""
    id: Int64Bit!
  ): NetworkSite
  """Update a non-inventory item."""
  updateNonInventoryItem(
    input: UpdateNonInventoryItemMutationInput
    """fields.non_inventory_item_id"""
    id: Int64Bit!
  ): NonInventoryItem
  """Update a note."""
  updateNote(
    input: UpdateNoteMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): Note
  """Update a one time service."""
  updateOneTimeService(
    input: UpdateOneTimeServiceMutationInput
    """The ID of a Service."""
    id: Int64Bit!
  ): Service
  """Update an order group."""
  updateOrderGroup(
    input: UpdateOrderGroupMutationInput
    """The ID of an order group."""
    id: Int64Bit!
  ): OrderGroup
  """Update an overage service."""
  updateOverageService(
    input: UpdateOverageServiceMutationInput
    """The ID of a Service."""
    id: Int64Bit!
  ): Service
  """Update a package."""
  updatePackage(
    input: UpdatePackageMutationInput
    """The ID of a `Package`."""
    id: Int64Bit!
  ): Package
  """Update the password policy that is applied to users."""
  updatePasswordPolicy(input: UpdatePasswordPolicyMutationInput): PasswordPolicy
  """Update a PayPal credential."""
  updatePayPalCredential(
    input: UpdatePayPalCredentialInput
    """The ID of the entity."""
    id: Int64Bit!
  ): PayPalCredential
  """Update a payment that was created without a payment method."""
  updatePayment(
    input: UpdatePaymentMutationInput
    """The ID of a `Payment`."""
    id: Int64Bit!
  ): Payment
  """Update a phone number."""
  updatePhoneNumber(
    input: UpdatePhoneNumberMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): PhoneNumber
  """Update a phone number type."""
  updatePhoneNumberType(
    input: UpdatePhoneNumberTypeMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): PhoneNumberType
  """Update a poller."""
  updatePoller(
    input: UpdatePollerMutationInput
    """The ID of a `Poller`."""
    id: Int64Bit!
  ): Poller
  """Update the system poller settings."""
  updatePollerSettings(input: UpdatePollerSettingsMutationInput): PollerSetting
  """Update the Preseem integration."""
  updatePreseem(input: UpdatePreseemMutationInput): Preseem
  """Update a print to mail order error."""
  updatePrintToMailOrderError(
    input: UpdatePrintToMailOrderErrorMutationInput
    """The ID of the print to mail order error."""
    id: Int64Bit!
  ): PrintToMailOrderError
  """Update the print to mail settings."""
  updatePrintToMailSettings(input: UpdatePrintToMailSettingsMutationInput): PrintToMailSetting
  """Update a purchase order."""
  updatePurchaseOrder(
    input: UpdatePurchaseOrderMutationInput
    """The ID of a purchase order."""
    id: Int64Bit!
  ): PurchaseOrder
  """Update system settings related to purchase orders."""
  updatePurchaseOrderSystemSettings(input: UpdatePurchaseOrderSystemSettingsInput): SuccessResponse
  """Update a RADIUS account."""
  updateRadiusAccount(
    input: UpdateRadiusAccountMutationInput
    """The ID of a `RadiusAccount`."""
    id: Int64Bit!
  ): RadiusAccount
  """Update a RADIUS group."""
  updateRadiusGroup(
    input: UpdateRadiusGroupMutationInput
    """The ID of a `RadiusGroup`."""
    id: Int64Bit!
  ): RadiusGroup
  """Update a RADIUS group reply attribute."""
  updateRadiusGroupReplyAttribute(
    input: UpdateRadiusGroupReplyAttributeMutationInput
    """fields.radius_group_reply_attribute_id"""
    id: Int64Bit!
  ): RadiusGroupReplyAttribute
  """Update a RADIUS server."""
  updateRadiusServer(
    input: UpdateRadiusServerMutationInput
    """The ID of a `RadiusServer`."""
    id: Int64Bit!
  ): RadiusServer
  """Update a rate center."""
  updateRateCenter(
    input: UpdateRateCenterMutationInput
    """The ID of a `RateCenter`."""
    id: Int64Bit!
  ): RateCenter
  """Update a recurring service."""
  updateRecurringService(
    input: UpdateRecurringServiceMutationInput
    """The ID of a Service."""
    id: Int64Bit!
  ): Service
  """Update a role."""
  updateRole(
    input: UpdateRoleMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): Role
  """Update a saved message category."""
  updateSavedMessageCategory(
    input: UpdateSavedMessageCategoryMutationInput
    """ID of the Saved Message Category."""
    id: Int64Bit!
  ): SavedMessageCategory
  """Update a schedule address."""
  updateScheduleAddress(
    input: UpdateScheduleAddressMutationInput
    """fields.schedule_address_id"""
    id: Int64Bit!
  ): ScheduleAddress
  """Update a schedule availability."""
  updateScheduleAvailability(
    input: UpdateScheduleAvailabilityMutationInput
    """The ID of a `ScheduleAvailability`."""
    id: Int64Bit!
  ): ScheduleAvailability
  """Update a schedule availability day/time."""
  updateScheduleAvailabilityDayTime(
    input: UpdateScheduleAvailabilityDayTimeMutationInput
    """fields.schedule_availability_day_time_id"""
    id: Int64Bit!
  ): ScheduleAvailabilityDayTime
  """Update a schedule blocker."""
  updateScheduleBlocker(
    input: UpdateScheduleBlockerMutationInput
    """The ID of a `ScheduleBlocker`."""
    id: Int64Bit!
  ): ScheduleBlocker
  """Update a schedule blocker day/time."""
  updateScheduleBlockerDayTime(
    input: UpdateScheduleBlockerDayTimeMutationInput
    """fields.schedule_blocker_day_time_id"""
    id: Int64Bit!
  ): ScheduleBlockerDayTime
  """Update a schedule time off."""
  updateScheduleTimeOff(
    input: UpdateScheduleTimeOffMutationInput
    """fields.schedule_time_off_id"""
    id: Int64Bit!
  ): ScheduleTimeOff
  """Update a scheduled event."""
  updateScheduledEvent(
    input: UpdateScheduledEventMutationInput
    """The ID of a `ScheduledEvent`"""
    id: Int64Bit!
  ): ScheduledEvent
  """
  Update a saved search filter for the current user, or enable it for all users (superadmin only).
  """
  updateSearchFilter(
    input: UpdateSearchFilterMutationInput
    """The ID of a SearchFilter entity."""
    id: Int64Bit!
  ): SearchFilter
  """Update service metadata."""
  updateServiceMetadata(
    input: UpdateServiceMetadataMutationInput
    """The ID of a ServiceMetadata field."""
    id: Int64Bit!
  ): ServiceMetadata
  """Update a serviceable address."""
  updateServiceableAddress(
    input: UpdateServiceableAddressMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): Address
  """Update a serviceable address account assignment future"""
  updateServiceableAddressAccountAssignmentFuture(
    input: UpdateServiceableAddressAccountAssignmentFutureMutationInput
    """The ID of the serviceable address account assignment future."""
    id: Int64Bit!
  ): ServiceableAddressAccountAssignmentFuture
  """Update a Signature."""
  updateSignature(
    input: UpdateSignatureMutationInput
    """The ID of a signature."""
    id: Int64Bit!
  ): Signature
  """Update the SMS settings."""
  updateSmsSettings(input: UpdateSmsSettingsMutationInput): SmsSetting
  """Update an SNMP OID."""
  updateSnmpOid(
    input: UpdateSnmpOidMutationInput
    """The ID of an `SnmpOid`."""
    id: Int64Bit!
  ): SnmpOid
  """Update an SNMP OID threshold."""
  updateSnmpOidThreshold(
    input: UpdateSnmpOidThresholdMutationInput
    """The ID of an `SnmpOidThreshold`."""
    id: Int64Bit!
  ): SnmpOidThreshold
  """Update an SNMP override."""
  updateSnmpOverride(
    input: UpdateSnmpOverrideMutationInput
    """fields.snmp_override_id"""
    id: Int64Bit!
  ): SnmpOverride
  """Update a stored view."""
  updateStoredView(
    input: UpdateStoredViewMutationInput
    """The ID of a `StoredView` entity."""
    id: Int64Bit!
  ): StoredView
  """Update a subnet."""
  updateSubnet(
    input: UpdateSubnetMutationInput
    """The ID of a `Subnet`."""
    id: Int64Bit!
  ): Subnet
  """Update supernet mutation."""
  updateSupernet(
    input: UpdateSupernetMutationInput
    """The ID of a `Supernet`."""
    id: Int64Bit!
  ): Supernet
  """Update a system backup destination."""
  updateSystemBackupDestination(
    input: UpdateSystemBackupDestinationMutationInput
    """The ID of a destination that a system backup can be exported to."""
    id: Int64Bit!
  ): SystemBackupDestination
  """Update settings for system backups."""
  updateSystemBackupSettings(input: UpdateSystemBackupSettingsMutationInput): SystemBackupSetting
  """Update system configuration."""
  updateSystemSettings(input: UpdateSystemSettingsMutationInput): SystemSetting
  """Update a task."""
  updateTask(
    input: UpdateTaskMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): Task
  """Update a task template."""
  updateTaskTemplate(
    input: UpdateTaskTemplateMutationInput
    """The ID of a `TaskTemplate`."""
    id: Int64Bit!
  ): TaskTemplate
  """Update a task template item."""
  updateTaskTemplateItem(
    input: UpdateTaskTemplateItemMutationInput
    """The ID of a `TaskTemplateItem`."""
    id: Int64Bit!
  ): TaskTemplateItem
  """Update a tax."""
  updateTax(
    input: UpdateTaxMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): Tax
  """Update a tax exemption."""
  updateTaxExemption(
    input: UpdateTaxExemptionMutationInput
    """fields.tax_exemption_id"""
    id: Int64Bit!
  ): TaxExemption
  """Update a tax override."""
  updateTaxOverride(
    input: UpdateTaxOverrideMutationInput
    """fields.tax_override_id"""
    id: Int64Bit!
  ): TaxOverride
  """Update a tax provider."""
  updateTaxProvider(
    input: UpdateTaxProviderMutationInput
    """The ID of an `TaxProvider`."""
    id: Int64Bit!
  ): TaxProvider
  """Update a ticket."""
  updateTicket(
    input: UpdateTicketMutationInput
    """The ID of a `Ticket`."""
    id: Int64Bit!
  ): Ticket
  """Update a ticket category."""
  updateTicketCategory(
    input: UpdateTicketCategoryMutationInput
    """fields.ticket_category_id"""
    id: Int64Bit!
  ): TicketCategory
  """Update a ticket comment."""
  updateTicketComment(
    input: UpdateTicketCommentMutationInput
    """fields.ticket_comment_id"""
    id: Int64Bit!
  ): TicketComment
  """Update a ticket group."""
  updateTicketGroup(
    input: UpdateTicketGroupMutationInput
    """The ID of a `TicketGroup`."""
    id: Int64Bit!
  ): TicketGroup
  """Update a ticket recipient."""
  updateTicketRecipient(
    input: UpdateTicketRecipientMutationInput
    """fields.ticket_recipient_id"""
    id: Int64Bit!
  ): TicketRecipient
  """Update the ticketing settings."""
  updateTicketingSettings(input: UpdateTicketingSettingsMutationInput): TicketingSetting
  """Update the TowerCoverage integration."""
  updateTowercoverageConfiguration(input: UpdateTowercoverageConfigurationInput): TowercoverageConfiguration
  """Update a Towercoverage submission."""
  updateTowercoverageSubmission(
    input: UpdateTowercoverageSubmissionMutationInput
    """The ID of a `TowercoverageSubmission`."""
    id: Int64Bit!
  ): TowercoverageSubmission
  """
  DEPRECATED: Update a triggered email. See updateTriggeredMessageMutation.
  """
  updateTriggeredEmail(
    input: UpdateTriggeredEmailMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): TriggeredEmail
  """Update a triggered message."""
  updateTriggeredMessage(
    input: UpdateTriggeredMessageMutationInput
    """The ID of a `TriggeredMessage`."""
    id: Int64Bit!
  ): TriggeredMessage
  """Update an uninventoried MAC address."""
  updateUninventoriedMacAddress(
    input: UpdateUninventoriedMacAddressMutationInput
    """fields.uninventoried_mac_address_id"""
    id: Int64Bit!
  ): UninventoriedMacAddress
  """Update a usage based billing policy."""
  updateUsageBasedBillingPolicy(
    input: UpdateUsageBasedBillingPolicyMutationInput
    """The ID of a `UsageBasedBillingPolicy`."""
    id: Int64Bit!
  ): UsageBasedBillingPolicy
  """Update a usage based billing policy free period."""
  updateUsageBasedBillingPolicyFreePeriod(
    input: UpdateUsageBasedBillingPolicyFreePeriodMutationInput
    """fields.usage_based_billing_policy_free_period_id"""
    id: Int64Bit!
  ): UsageBasedBillingPolicyFreePeriod
  """Update a user."""
  updateUser(
    input: UpdateUserMutationInput
    """The ID of the entity."""
    id: Int64Bit!
  ): User
  """Update a vehicle."""
  updateVehicle(
    input: UpdateVehicleMutationInput
    """The ID of a `Vehicle`."""
    id: Int64Bit!
  ): Vehicle
  """Update a vendor."""
  updateVendor(
    input: UpdateVendorMutationInput
    """The ID of a vendor."""
    id: Int64Bit!
  ): Vendor
  """Update a vendor item."""
  updateVendorItem(
    input: UpdateVendorItemMutationInput
    """The ID of a vendor item."""
    id: Int64Bit!
  ): VendorItem
  """Update a voice provider."""
  updateVoiceProvider(
    input: UpdateVoiceProviderMutationInput
    """The ID of a `VoiceProvider`."""
    id: Int64Bit!
  ): VoiceProvider
  """Update a voice provider rate."""
  updateVoiceProviderRate(
    input: UpdateVoiceProviderRateMutationInput
    """The ID of a `VoiceProviderRate`"""
    id: Int64Bit!
  ): VoiceProviderRate
  """Update the charge percent for all rates of a voice provider."""
  updateVoiceProviderRateChargePercentMutation(input: UpdateVoiceProviderRateChargePercentMutationInput): SuccessResponse
  """Update a voice service."""
  updateVoiceService(
    input: UpdateVoiceServiceMutationInput
    """The ID of a Service."""
    id: Int64Bit!
  ): Service
  """Create a single voice service configuration parameter."""
  updateVoiceServiceGenericParameter(
    input: UpdateVoiceServiceGenericParameterMutationInput
    """The ID of a voice service configuration parameter."""
    id: Int64Bit!
  ): VoiceServiceGenericParameter
  """Update a webhook endpoint."""
  updateWebhookEndpoint(
    input: UpdateWebhookEndpointMutationInput
    """The ID of a webhook endpoint."""
    id: Int64Bit!
  ): WebhookEndpoint
  """
  Validate the credentials for a cable modem provisioner. This will update the `status` of the cable modem provisioner.
  """
  validateCableModemProvisionerCredentials(
    """The ID of a `CableModemProvisioner`."""
    id: Int64Bit!
  ): CredentialValidationResponse
  """Validate credentials of a Calix integration"""
  validateCalixCredentials(
    """Calix Inegartion ID."""
    calix_integration_id: Int64Bit!
  ): CredentialValidationResponse
  """
  Validate the entered DHCP server credentials. This will update the `status` of the DHCP server.
  """
  validateDhcpServerCredentials(
    """The ID of a `DhcpServer`."""
    id: Int64Bit!
  ): CredentialValidationResponse
  """Validate an email domain's DNS records and email verification status."""
  validateEmailDomain(
    """The ID of an `EmailDomain`."""
    id: Int64Bit!
    """Perform the check for the purposes of email provider migration."""
    check_for_migration: Boolean = false
  ): EmailDomain
  """
  Validate GPS tracking provider credentials validate against external provider.
  """
  validateGpsTrackingProviderCredentials(
    """A `GpsTrackingProvider` ID."""
    id: Int64Bit!
  ): CredentialValidationResponse
  """
  Validate the credentials for an inline device. This will update the `status` of the inline device.
  """
  validateInlineDeviceCredentials(
    """The ID of an `InlineDevice`."""
    id: Int64Bit!
  ): CredentialValidationResponse
  """
  Validate the entered LTE provider credentials. This will update the `status` of the LTE provider.
  """
  validateLteProviderCredentials(
    """The ID of an `LteProvider`."""
    id: Int64Bit!
  ): CredentialValidationResponse
  """
  Validate the entered RADIUS server credentials. This will update the `status` of the RADIUS server.
  """
  validateRadiusServerCredentials(
    """The ID of a `RadiusServer`."""
    id: Int64Bit!
  ): CredentialValidationResponse
  """Validate the entered tax provider credentials."""
  validateTaxProviderCredentials(
    """The ID of an `TaxProvider`."""
    id: Int64Bit!
  ): CredentialValidationResponse
  """Verify a one-time password for an authentication factor."""
  verifyOneTimePasswordForAuthenticationFactor(input: VerifyOneTimePasswordForAuthenticationFactorMutationInput): SuccessResponse
  """Verify the credentials for a system backup destination."""
  verifySystemBackupDestinationConnection(
    """The ID of a destination that a system backup can be exported to."""
    id: Int64Bit!
  ): SuccessResponse
  """Void a credit on an invoice."""
  voidCredit(
    """fields.credit_id"""
    id: Int64Bit!
  ): Credit
  """Void an invoice."""
  voidInvoice(
    """The ID of an `Invoice`."""
    id: Int64Bit!
  ): Invoice
  """Void a payment."""
  voidPayment(
    input: VoidPaymentMutationInput
    """The ID of a `Payment`."""
    id: Int64Bit!
  ): VoidedPayment
}
```
