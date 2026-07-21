---
title: "Worklog Week 8"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

Week 8 Objectives:
- Optimize application performance in preparation for heavy traffic. By deploying an In-memory Caching mechanism with Amazon ElastiCache (Redis), the objective is to significantly reduce the load on the RDS database and decrease latency for APIs returning static or infrequently changing content.

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 05/06 | Researched documentation on caching strategies and the Amazon ElastiCache service. Analyzed current API endpoints of the Pet Resort system and identified that the API fetching the 'Spa Services List' is a highly read-heavy endpoint but its data rarely changes. Decided to implement Redis as a cache layer positioned between the Backend and the RDS Database. | 05/06 | 06/06 | |
| 07/06 | Accessed the AWS Console and provisioned a Redis Cluster via the ElastiCache service. Placed this Redis Cluster inside the Private Subnets to maximize security. Established a distinct Security Group for the Redis Cluster, configuring Inbound Rules to only allow EC2 servers hosting the Backend permission to connect via the default port 6379, completely blocking all other unauthorized access sources. | 07/06 | 08/06 | |
| 09/06 | Returned to the Spring Boot codebase, added the `spring-boot-starter-data-redis` dependency and configured the connection to the ElastiCache host via environment variables. Enabled Spring's caching features using the `@EnableCaching` annotation. Applied annotations like `@Cacheable`, `@CachePut`, and `@CacheEvict` on logic handling functions fetching the services list. Meticulously configured the Time-To-Live (TTL) for data in the cache to ensure data doesn't become stale. | 09/06 | 10/06 | |
| 11/06 | Re-packaged (built) the `.jar` file, uploaded it, and restarted the systemd service on EC2. Utilized tools like Apache JMeter or Postman Runner to perform trickle Load Testing. Closely observed the Response Time. Recorded the results: initial requests took several hundred milliseconds to fetch from RDS, subsequent requests fetching directly from Redis on RAM took under a few tens of milliseconds, reducing latency by over 80%. | 11/06 | 11/06 | |

Week 8 Achievements:

- Successfully and efficiently integrated Redis Cache technology (via ElastiCache) into the overall system architecture.
- Thoroughly eliminated database speed bottlenecks, mitigating the risk of overloading RDS.
- Drastically improved user experience with near-instantaneous API response speeds for loading service catalogs.
