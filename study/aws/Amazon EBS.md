EBS is the **Elastic Block Store**. EBS volumes are network-attached storage that can be attached to EC2 instances. EBS volume data persists independently of the life of the instance, and it does not need to be attached to an instance. You can attach multiple EBS volumes to an instance; however, you cannot attach an EBS volume to multiple instances (use Elastic File Store instead).

EBS is designed for an annual failure rate of 0.1%-0.2% & an SLA (Service Level Agreement) of 99.95%.

Volume sizes and types can be upgraded without downtime (except for magnetic standard). Elastic Volumes allow you to increase volume size, adjust performance, or change the volume type while the volume is in use. However, you cannot decrease an EBS volume size. When changing volumes, the new volume must be at least the current volume’s snapshot size.

**Limits**

You can have up to 5,000 EBS volumes and up to 10,000 snapshots by default.

### EBS Volume Types
**SSD, General Purpose - gp2**
	- Baseline of 3 IOPS per GiB with a minimum of 100 IOPS
	-   Burst up to 3000 IOPS (for volumes >= 334GB)
	-   Up to 16,000 IOPS per volume
	-   AWS designs gp2 volumes to deliver 90% of the provisioned performance 99% of the time. A gp2 volume can range in size from 1 GiB to 16 TiB.

**SSD, Provisioned IOPS - iO1**
	-   More than 16,000 IOPS
	-   Up to 64,000 IOPS per volume
	-   Up to 50 IOPS per GiB
	-   Amazon EBS delivers the provisioned IOPS performance 99.9 percent of the time.

HDD, Throughput Optimized - st1
	-   Frequently accessed throughput intensive workloads with large datasets and large I/O sizes, such as MapReduce, Kafka, log processing, data warehouse, and ETL workloads
	-   Throughput measured in MB/s and includes the ability to burst up to 250 MB/s per TB, with a baseline throughput of 40 MB/s per TB and a maximum throughput of 500 MB/s per volume
	-   Cannot be a boot volume

HDD, Cold - sc1
	-    Less frequently accessed workloads with large, cold datasets
	-   These volumes can burst up to 80 MB/s per TB, with a baseline throughput of 12 MB/s per TB and a maximum throughput of 250 MB/s per volume.

**Magnetic (Standard)**
	-   Cheap, infrequently accessed storage that can be a boot volume
	-   Delivers around 100 IOPS on average

**EBS optimized instances**
	-   Dedicated capacity for Amazon EBS I/O
	-   EBS-optimized instances are designed for use with all EBS volume types.
	-   Max bandwidth: 400 Mbps – 12000 Mbps
	-   IOPS: 3000 – 65000
	-   GP-SSD within 10% of baseline and burst performance 99.9% of the time
	-   PIOPS within 10% of baseline and burst performance 99.9% of the time
	-   Additional hourly fee
	-   Available for select instance types
	-   Some instance types have EBS-optimized enabled by default.

### Encryption with EBS
When you create an encrypted EBS volume and attach it to a supported instance type, the following types of data are encrypted:

-   Data at rest inside the volume
-   All data moving between the volume and the instance
-   All snapshots created from the volume
-   All volumes created from those snapshots

EBS encrypts your volume with a data key using the industry-standard AES-256 algorithm. Your data key is stored on-disk with your encrypted data, but not before EBS encrypts it with your CMK.

### Snapshots

**The following information applies to snapshots:**

-   Snapshots are created asynchronously and are incremental.
-   You can copy unencrypted snapshots (optionally encrypt).
-   You can copy an encrypted snapshot (optionally re-encrypt with a different key).
-   Snapshot copies receive a new unique ID.
-   You can copy within or between regions.
-   You cannot move snapshots, only copy them.
-   You cannot take a copy of a snapshot when it is in a “pending” state; it must be “complete”.
-   S3 Server Side Encryption (SSE) protects data in transit while copying.
-   User-defined tags are not copied.
-   You can have up to 5 snapshot copy requests running in a single destination per account.
-   You can copy Import/Export service, AWS Marketplace, and AWS Storage Gateway snapshots.
-   If you try to copy an encrypted snapshot without having access to the encryption keys, it will fail silently (cross-account permissions are required).

**Copying snapshots may be required for:**

-   Creating services in other regions
-   DR — the ability to restore from a snapshot in another region
-   Migration to another region
-   Applying encryption
-   Data retention

**To take application-consistent snapshots of RAID arrays:**

-   Stop the application from writing to disk.
-   Flush all caches to the disk.
-   Freeze the filesystem.
-   Unmount the RAID array.
-   Shut down the associated EC2 instance.
