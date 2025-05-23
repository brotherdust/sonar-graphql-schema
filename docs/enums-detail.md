```graphql
"""The direction of a call detail record (CDR)."""
enum CallDetailRecordDirection {
  """INBOUND"""
  INBOUND
  """OUTBOUND"""
  OUTBOUND
}

"""The prefix type of a call detail record."""
enum CallDetailRecordPrefixType {
  """LOCAL"""
  LOCAL
  """LONG DISTANCE"""
  LONG_DISTANCE
  """TOLL FREE"""
  TOLL_FREE
  """PROVIDER RATED"""
  PROVIDER_RATED
}

"""The event which is associated with the disbursement detail."""
enum DisbursementDetailEvent {
  """Triggered daily"""
  DAYS
  """Triggered weekly"""
  WEEKS
  """Triggered monthly"""
  MONTHS
  """Triggered yearly"""
  YEARS
  """One-off"""
  SINGLE
  """Authorization"""
  AUTH
  """Capture"""
  CAPTURE
  """Refund"""
  REFUND
  """Merchant is boarded"""
  BOARD
  """Payout processed"""
  PAYOUT
  """Chargeback"""
  CHARGEBACK
  """Overdraft"""
  OVERDRAFT
  """Interchange fees"""
  INTERCHANGE
  """Payment processor"""
  PROCESSOR
  """ACH failure"""
  ACHFAIL
  """Bank account verified"""
  ACCOUNT
  """Fraud score"""
  SIFT
  """Adjustment"""
  ADJUSTMENT
  """Retrieval request chargeback"""
  RETRIEVAL
  """Arbitration chargeback"""
  ARBITRATION
  """eCheck Sale"""
  ECSALE
  """eCheck Refund"""
  ECREFUND
  """eCheck Return"""
  ECRETURN
  """Settlement"""
  SETTLEMENT
  """Misuse of authorization"""
  MISUSE
  """Profit sharing"""
  PROFIT_SHARE
  """Unauthorized entry"""
  UNAUTH
  """ACH notification of change"""
  ACHNOC
  """eCheck notification of change"""
  ECNOC
  """eCheck fail"""
  ECFAIL
  """eCheck non-sufficient funds"""
  ECNSF
  """Currency conversion"""
  CURRENCY_CONVERSION
  """Terminal transaction"""
  TERMINAL_TXN
  """Reversed payout"""
  REVERSE_PAYOUT
  """Partially reversed payout"""
  PARTIAL_REVERSE_PAYOUT
  """Reserved funds"""
  RESERVE_ENTRY
  """Released reserves"""
  RESERVE_ENTRY_RELEASE
  """Pending funds"""
  PENDING_ENTRY
  """Paid pending funds"""
  PENDING_PAID
  """Non-disbursed funds"""
  REMAINDER
  """Previously non-disbursed funds"""
  REMAINDER_USED
  """Cancelled pending refund"""
  PENDING_REFUND_CANCELLED
  """Event 43"""
  EVENT_43
  """Event 44"""
  EVENT_44
  """Event 45"""
  EVENT_45
  """Event 46"""
  EVENT_46
  """Event 47"""
  EVENT_47
  """Event 51"""
  EVENT_51
  """Event 52"""
  EVENT_52
  """Event 53"""
  EVENT_53
  """Event 54"""
  EVENT_54
  """Event 55"""
  EVENT_55
  """Event 56"""
  EVENT_56
  """Event 57"""
  EVENT_57
  """Event 58"""
  EVENT_58
  """Event 59"""
  EVENT_59
  """Event 60"""
  EVENT_60
  """Event 61"""
  EVENT_61
  """Event 62"""
  EVENT_62
  """Event 63"""
  EVENT_63
  """Event 64"""
  EVENT_64
  """Event 65"""
  EVENT_65
  """Event 66"""
  EVENT_66
  """Event 67"""
  EVENT_67
  """Event 68"""
  EVENT_68
  """Event 69"""
  EVENT_69
  """Event 70"""
  EVENT_70
  """Event 71"""
  EVENT_71
  """Event 72"""
  EVENT_72
  """Event 73"""
  EVENT_73
  """Event 74"""
  EVENT_74
  """Event 75"""
  EVENT_75
  """Event 76"""
  EVENT_76
  """Event 77"""
  EVENT_77
  """Event 78"""
  EVENT_78
  """Event 79"""
  EVENT_79
  """Event 80"""
  EVENT_80
  """Event 81"""
  EVENT_81
  """Event 82"""
  EVENT_82
  """Event 83"""
  EVENT_83
  """Event 84"""
  EVENT_84
  """Event 85"""
  EVENT_85
  """Event 86"""
  EVENT_86
  """Event 200"""
  EVENT_200
  """Event 201"""
  EVENT_201
}
```
