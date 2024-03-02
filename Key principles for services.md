Airbnb decided on some key principles to design these services with a disciplined approach:

- Services should own both the reads and writes to their data. It’s quite similar to the **database-per-service** pattern where a particular database should be owned by one and only one service, making it easier to maintain data consistency.

- **Each service should address a specific concern**. Airbnb wanted to make sure that the monolith does not decompose into another giant service that turned into another monolith over time. Also, they wanted to avoid the path of traditional granular microservices that are only good at one thing. Instead, Airbnb shifted towards building services focused on a specific business functionality. Think of it as a high-cohesion design.
- 
- - **Services should avoid duplicating functionality**. Sharing parts of infrastructure or code was done by means of shared libraries and shared services, making them easier to maintain.
- - **Data mutation should take place via standard events**. For example, if the reservation service creates a new row, the availability service should learn about this reservation by means of an event so that it can mark the home’s availability as busy.
- - **Each service must be built as if it was mission-critical**. This meant the service should have appropriate alerting mechanisms, built-in observability and best practices for infrastructure.