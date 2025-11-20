# S3

###[How AWS S3 serves 1 petabyte per second on top of slow HDDs](https://bigdata.2minutestreaming.com/p/how-aws-s3-scales-with-tens-of-millions-of-hard-drives) - by [Stanislav Kozlovski](https://substack.com/@stanislavkozlovski)

***

AWS S3 operates at an immense scale, storing over 400 trillion objects and handling 150 million requests per second. Its foundation is built on commodity Hard Disk Drives (HDDs), which are incredibly cost-effective for storage but are physically slow for the random I/O operations S3 requires. The core engineering challenge is delivering high-performance random access from inherently slow hardware.

S3's solution is **massive parallelism**, implemented at every level to overcome HDD limitations.

* **Erasure Coding:** Instead of simple replication, S3 shards each object into multiple data and parity pieces (e.g., a 5-of-9 scheme). This data is spread across many different disks, providing data durability and, crucially, allowing pieces of a file to be read in parallel from multiple sources.

* **End-to-End Parallelism:** The system is designed for parallel operations from the user to the disk. Clients are encouraged to upload and download files in parallel chunks (multipart uploads and byte-ranged GETs), and these requests are distributed across S3's vast network of front-end servers.

To prevent "hot spots" (overloaded disks), S3 uses clever load distribution. It employs randomization techniques like "Power of Two Random Choices" to place new data on the least-loaded disks and continuously rebalances data as it ages and becomes less frequently accessed.

Ultimately, as S3 has grown, its aggregated workload has become smoother and more predictable, a phenomenon known as "workload decorrelation," which makes managing the massive system more efficient at scale.
