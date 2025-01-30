# Java Interview Question
<details>
<summary>
You need to handle 1 million requests per second. How would you scale your backend architecture?
</summary>

1. **Horizontal Scaling**: Instead of relying on one super-powerful server, you add more servers to handle the load. Think of it as expanding a factory: instead of having just one assembly line, you set up several. This way, each server handles a smaller piece of the traffic, making the whole system more efficient.

2. **Caching**: Not every request needs to go all the way to the database. If the data doesn't change often, you can store frequently requested information in a cache (like a fast-access memory area). This reduces the load on your database, improving response times.

3. **Database Sharding**: If you're using a database, you'll need to split your data into smaller, more manageable chunks (called sharding). Each chunk can be stored on a different server. This allows you to distribute the load and ensures no single database is overloaded.

4. **Microservices Architecture**: Instead of having one giant system that does everything, you split your application into smaller, independent services that handle specific tasks. Each service can scale independently, so if one part of your app gets a lot of traffic, you can scale that part without affecting the rest of the system.

5. **Auto-scaling**: With cloud providers like AWS, Google Cloud, or Azure, you can set up your system to automatically add or remove servers based on the current load. This ensures you're only using resources when you need them, helping you manage costs while meeting demand.

6. **Asynchronous Processing**: Not all tasks need to be done in real-time. For things that can wait (like sending an email or generating a report), you can use queues. Requests are placed in a queue and processed later, which allows your system to focus on handling real-time requests first.
</details>

<details>
<summary>
If you are building an order management system, how would you design the services? (Database choices, API interactions, scalability)
</summary>

1. **Relational Databases** (like PostgreSQL) for transactional data, with NoSQL where appropriate.
2. A **microservices architecture** with a REST or GraphQL API design for smooth communication between services.
3. **Horizontal scaling** using load balancing, auto-scaling, and service discovery to handle millions of requests.
4. Strategies for data consistency (**ACID transactions**) and fault tolerance (circuit breakers, retries).
5. **Logging and monitoring** to track system health and prevent downtime.

With these choices, the OMS will be able to handle high traffic, remain resilient during failures, and grow over time.
