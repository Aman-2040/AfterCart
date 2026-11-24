# Database Schema (initial planning)

Suggested entities:
- User
- PaymentMethod (issuer, card type, network and variant only; no card credentials)
- Product
- ProductAttribute
- Retailer
- ProductListing
- Offer
- OfferCondition
- DealCalculation
- Order
- OrderItem
- OrderEvent
- AgentTask
- TaskStep
- Approval
- Resolution
- Document

Normalize product variants before comparison. Store offer source and observation timestamp. Track return lifecycle states separately, such as FORM_FILLED, AWAITING_APPROVAL, RETURN_REQUEST_SUBMITTED, RETURN_ACCEPTED and REFUND_ISSUED.
