### Overview
- Proxy supplemented by additional functionality
  - Authentication / Authorization
  - Save in Progress
  - Prefill
  - Notifications
  - Monitoring
  - Downtime Notifications
- Diagram with major components
- Anatomy of an API request

### Development
- Style Guides
- Development Process
- Automated Testing
- Load Testing
- Security

### Routing (Guide)
- Authentication (Overview)
- Authorization [Guide](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Engineering/Design%20Docs/authorization%20design%20doc.md)

### Request Processing (Guide)
- Minimal controller logic
- External service client instantiation
- Caching
- Instrumentation

### Forms
- Form Schema Validation (Guide)
- PDF Generation (Guide) [Future?]

### External Service Client (Guide)
- Configuration
- Service Object
- Models
- Instrumentation
- Maintenance Windows

### Response Serialization (Guide)

### Handling Errors (Guide)
- Definition / Internal || External
- Responses
- Tracking

### Documentation (Guide)

### Overall Instrumentation (Guide)
### Asynchronous Processing (Additional Information)
### Support / Incident Response (Additional Information)

### Notes from Alastair to be considered for BE guide:
- Config/settings.yml entry for base urls and other options that change per environment
- Configuration class (REST or SOAP) to load the above settings and initialize a Faraday connection
- Service class to call endpoints on the sub-system's API
- Response class that validates and parses the response (sometimes doubles as a model)
- Model class (if the response isn't doing double duty)
- Serializer to filter and serialize model attributes to the json-api spec
- Route definition map paths to controller actions
