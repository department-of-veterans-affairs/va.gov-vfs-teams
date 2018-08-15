---
title: Request Processing
label: Request Processing
---
Request processing occurs after [Routing](./routing.md), [Authentication](./authentication), and [Authorization](./authorization). It consists of validating any user input or parameters, processing that input, and generating a response.

## Example

## Caching

## Error Handling

## Instrumentation

## External Service Client Instantiation

## Implementation Considerations

### Security

### Performance

Take into consideration the time and resources that are required to process a request. In order to improve the user experience and prevent resource exhaustion at the infrastructure level, try to minimize the request process time, and ensure that implementations are as performant as is realistic given the requirements. Generally, Vets-API recommends request processing not exceed 100ms. If this is unavoidable, consider running the process [asynchronously](./AsynchronousProcessing.md), and ensure that the user experience takes this processing time into account.

<!-- Next Button -->
<a href='./response-serialization'><div class="next-button"><h5 class="next-text">Next: Response Serialization</h5></div></a>
