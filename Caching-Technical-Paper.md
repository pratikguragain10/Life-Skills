## Caching

---

## Introduction

- Cache in general terms is a storage location where such data are stored which are frequently accesed or retrieved. In basic words, it enables faster retrieval of data.

- Real-life Example:

    - Let's say there's a movie which is in high demand(popular) or is recently released and people are frequently trying to access or watch it. Now a user sends request to the browser server to access the data, the server then access the database search the requested data and fetch it it's a longer process instead of all that we or the system uses caching a specific memory is allocated in ram where that movie data is accessed so whenever any user request that data the server can directly access the cache and return the requested data which make's it faster instead of fetching from specific database.

---

## Caching's Purpose

- A cache's primary purpose is to increase data retrieval performance by reducing the need to access the underlying slower storage layer. Trading off capacity for speed, a cache typically stores a subset of data transiently, in contrast to databases whose data is usually complete and durable.

---

## Applications of caching

- Caching are preferably used for multiple purposes and in different technologies like:
    
    - Operating System(OS)
    - Content Delivery Network(CDN)
    - Domain Name System(DNS)
    - Web Application
    - Database

- They are mainly used in such field and technologies because they have to handle and tackle huge loads of data at once while facing huge traffics which can cause latency which decreases the quality of services for users. So inorder to avoid this issues caching is used to avoid latency and improve the work-rate of many read-heavy application workloads.

- Cached information can include the results of database queries, computationally intensive calculations, API requests/responses and web artifacts such as HTML, JavaScript, and image files

---

## Caching Approaches & Strategies

- Cache-Aside
- Read-Through
- Write-Through
- Write-Back
- Write-Around

### Cache-Aside

- In this approach, whenever any data is requested if that data is available in cache it is returned, if not available the data is fetched from database by the application and stored in cache for future usage it is also called lazy loading.

![Cache Aside](cache-aside.png)

### Read-Through

- In this approach, when the data request comes the application checks the cache first if available return it, if the data doesn't exist in cache then cache goes to database loads the data in it and return the data to application.

![Read Through](read-through.png)

### Write-Through

- In this mechanism, the application writes or loads the data in both cache and database simultaneously. However, it slows down write operations because of double the time write operation.

![Write Through](write-through.png)

### Write-Back

- In this mechanism, the application writes the data in cache first and after some delay the data is written into the database.

![Write Back](write-back.png)

### Write-Around

- Write-Around mechanism combines with a Read-Through caching approach or Cache-Aside strategy. The application always writes the data into the database and reads data from the cache. If there's a cache miss, the data is fetched from the database and then stored in the cache for future reads. This strategy works best when data is rarely updated and read in more often.

![Write Around](write-around.png)

---

## References

- https://aws.amazon.com/caching/
- https://www.geeksforgeeks.org/dbms/what-is-caching-strategies-in-dbms/
- https://docs.aws.amazon.com/whitepapers/latest/database-caching-strategies-using-redis/caching-patterns.html
- https://www.youtube.com/watch?v=6FyXURRVmR0

---