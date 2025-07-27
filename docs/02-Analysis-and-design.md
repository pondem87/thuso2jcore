# Analysis and design

## Domain modelling

domains
- customer engagement
- products and services
- bookings
- promotions
- crm
- administration
- system

### Customer engagement

#### Entities:
- customer
- conversation - lasts 24 hours and new one created
- message
- sentiment record
- customer preferences
- daily activity - summary of all entity records for the day

#### Value objects:
- phone number
- label
- label type
- message direction

#### Domain services:
sentiment service
- recordSentimentChange - method called when current sentiment of conversation changes. We have to create a new sentiment record as we are tracking sentiment dynamically. Snapshot sentiment is still stored on the conversation object.

![diagram](uml/domain_modelling/images/customer_engagement_domain.png)
- [link to puml file](uml/domain_modelling/customer_engagement.puml)

### Products and services