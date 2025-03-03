# Cloud Based Integration & Messaging. Data Processing & Streaming (aka Data Pipeline). Open Data Hub
- [Message Queue in Kubernetes. Event-driven Messaging. Real-Time Data Streaming](#message-queue-in-kubernetes-event-driven-messaging-real-time-data-streaming)
- [RPC vs Messaging](#rpc-vs-messaging)
- [Message Brokers](#message-brokers)
	- [ActiveMQ message broker](#activemq-message-broker)
	- [RabbitMQ message broker](#rabbitmq-message-broker)
	- [Redis message broker](#redis-message-broker)
	- [Apache Camel message broker](#apache-camel-message-broker)
		- [Apache Camel K](#apache-camel-k)
	- [KubeMQ message broker](#kubemq-message-broker)
	- [Google Cloud Platform Pub/Sub](#google-cloud-platform-pubsub)
- [Cloud Based Integration. Integration Platform-as-a-Service (iPaaS) solutions](#cloud-based-integration-integration-platform-as-a-service-ipaas-solutions)
	- [Red Hat Fuse and Red Hat Fuse Online](#red-hat-fuse-and-red-hat-fuse-online)
	- [Syndesis open source integration platform](#syndesis-open-source-integration-platform)
- [Debezium open source distributed platform for Change Data Capture (CDC) software design pattern](#debezium-open-source-distributed-platform-for-change-data-capture-cdc-software-design-pattern)
- [Red Hat Integration service registry and Apicurio](#red-hat-integration-service-registry-and-apicurio)
- [Data Mesh](#data-mesh)
- [Data Processing (aka Streaming Data, Data Pipeline or Big Data Pipeline)](#data-processing-aka-streaming-data-data-pipeline-or-big-data-pipeline)
	- [Apache Kafka](#apache-kafka)
		- [Strimzi kubernetes operator for apache kafka](#strimzi-kubernetes-operator-for-apache-kafka)
		- [Apache Kafka Desktop Clients](#apache-kafka-desktop-clients)
	- [AWS Kinesis](#aws-kinesis)
	- [MQTT](#mqtt)
	- [Banzai Cloud Supertubes (Cloud Native Kafka implementation)](#banzai-cloud-supertubes-cloud-native-kafka-implementation)
	- [Confluent Cloud (Apache Kafka Re-engineered for the Cloud)](#confluent-cloud-apache-kafka-re-engineered-for-the-cloud)
	- [Redpanda (kafka alternative). A modern streaming platform for mission critical workloads](#redpanda-kafka-alternative-a-modern-streaming-platform-for-mission-critical-workloads)
		- [KsqlDB](#ksqldb)
	- [Apache Pulsar](#apache-pulsar)
	- [Apache Flink](#apache-flink)
	- [Hazelcast JET](#hazelcast-jet)
- [Workflow Engines](#workflow-engines)
- [Zeebe](#zeebe)
	- [Apache Airflow](#apache-airflow)
	- [Couler](#couler)
- [Red Hat AMQ (ActiveMQ Artemis broker and Apache Kafka)](#red-hat-amq-activemq-artemis-broker-and-apache-kafka)
	- [Red Hat AMQ Broker (ActiveMQ Artemis)](#red-hat-amq-broker-activemq-artemis)
	- [Red Hat AMQ Streams](#red-hat-amq-streams)
- [Open Data Hub AI-as-a-Service (AIaaS) platform](#open-data-hub-ai-as-a-service-aiaas-platform)
- [KEDA. Kubernetes Event Driven Autoscaling](#keda-kubernetes-event-driven-autoscaling)
- [Integration Platform as a Solution (iPaaS). Platforms for collecting, storing and routing customer event data](#integration-platform-as-a-solution-ipaas-platforms-for-collecting-storing-and-routing-customer-event-data)
	- [IpaaS Vendors](#ipaas-vendors)
- [eBooks](#ebooks)
- [Related](#related)
- [Questions and Answers](#questions-and-answers)
- [Videos](#videos)
- [Tweets](#tweets)

## Message Queue in Kubernetes. Event-driven Messaging. Real-Time Data Streaming
- [Wikipedia: Message Broker](https://en.wikipedia.org/wiki/Message_broker)
- [Wikipedia: Event-driven messaging](https://en.wikipedia.org/wiki/Event-driven_messaging)
- [Wikipedia: Streaming Data](https://en.wikipedia.org/wiki/Streaming_data)
- [nginx.com: Event-Driven Data Management for Microservices 🌟](https://www.nginx.com/blog/event-driven-data-management-microservices/)
- [dzone: Event-Driven Architecture as a Strategy](https://dzone.com/articles/event-driven-architecture-as-a-strategy) Event-driven architecture provides five key benefits to modern application architecture: scalability, resilience, agility, data sharing, and cloud enabling.
- [infoq.com: From Monolith to Event-Driven: Finding Seams in Your Future Architecture](https://www.infoq.com/articles/event-driven-finding-seams/)
- [wikipedia: Enterprise service bus](https://en.wikipedia.org/wiki/Enterprise_service_bus)
- [thenewstack.io: The Rise of the Event Streaming Database 🌟](https://thenewstack.io/the-rise-of-the-event-streaming-database/)
- [cncf.io: The need for Kubernetes Native Messaging Platform in Hybrid Cloud Environment](https://www.cncf.io/blog/2020/11/03/the-need-for-kubernetes-native-messaging-platform-in-hybrid-cloud-environment/)
- [wiprodigital.com: A Guide to Enterprise Event-Driven Architecture](https://wiprodigital.com/2020/11/10/a-guide-to-enterprise-event-driven-architecture/)
- [medium: Introduction to Event-Driven Architecture 🌟](https://medium.com/microservicegeeks/introduction-to-event-driven-architecture-e94ef442d824) The essential concepts that every developer should know
- [ibm.com: Event-driven cloud-native applications (microservices)](https://www.ibm.com/cloud/architecture/architecture/practices/event-driven-cloud-native-apps-architecture) The event backbone is being part of the microservices mesh, providing the publish-and-subscribe communication between microservices and enabling the support of loosely coupled event-driven microservices.
- [stackoverflow.blog: How event-driven architecture solves modern web app problems 🌟](https://stackoverflow.blog/2020/03/16/how-event-driven-architecture-solves-modern-web-app-problems/) In this article, we’ll discuss some of the problems driving innovation in modern web development. Then we’ll dive into the basics of event-driven architecture (EDA), which tries to address these problems by thinking about back-end architecture in a novel way.
- [sebalopezz.medium.com: Monolith to Microservices + Event-Driven Architecture 🌟](https://sebalopezz.medium.com/monolith-to-microservices-event-driven-architecture-ff4284bf4ecf)
- [confluent.io: Event-Driven Microservices Architecture (white paper) 🌟](https://www.confluent.io/resources/event-driven-microservices/) Microservices are an architectural pattern that structures an application as a collection of small, loosely coupled services that operate together to achieve a common goal. Because they work independently, they can be added, removed, or upgraded without interfering with other applications. While there are numerous benefits to microservices architecture, like easier deployment and testing, improved productivity, flexibility, and scalability, they also pose a few disadvantages, as independently run microservices require a seamless method of communication to operate as one larger application. Event-driven microservices allow for real-time microservices communication, enabling data to be consumed in the form of events before they’re even requested. In this white paper, we’ll cover how event-driven microservices work, presenting a sample currency exchange platform to illustrate the design and architecture of an application composed of event-driven microservices using Apache Kafka® and Confluent Platform. We also discuss other aspects of microservices architectures, such as team structure, continuous delivery, deployment, and testing. Lastly, we discuss how Apache Kafka and Confluent Platform enable and extend core principles of microservices, including decoupling, separation of concerns, agility, and real-time streaming of event data.
- [redhat.com: Event-driven architecture: Understanding the essential benefits 🌟](https://www.redhat.com/architect/event-driven-architecture-essentials) Event-driven architectures bring significant benefits when managing many endpoints, but it also has its complexities to be aware of.
- [medium: Introduction to Message Queues 🌟](https://medium.com/hookdeck/introduction-to-message-queues-20d00373cc1f)
- [headspring.com: Is Kafka or RabbitMQ the right messaging tool for you?](https://headspring.com/2019/07/09/kafka-or-rabbitmq-messaging/)
- [dzone: Why Pub/Sub Isn’t Enough for Modern Apps](https://dzone.com/articles/why-pubsub-isnt-enough-for-modern-apps) Pub/Sub is the most appropriate way of architecting the delivery side of an event-driven architecture (especially for the web).
- [baeldung.com: Pub-Sub vs. Message Queues 🌟](https://www.baeldung.com/pub-sub-vs-message-queues)
- [engineering.atspotify.com: Spotify’s Event Delivery – The Road to the Cloud (Part I)](https://engineering.atspotify.com/2016/02/25/spotifys-event-delivery-the-road-to-the-cloud-part-i/)
- [medium: Monolithic to Microservices Architecture with Patterns & Best Practices 🌟](https://medium.com/design-microservices-architecture-with-patterns/monolithic-to-microservices-architecture-with-patterns-best-practices-a768272797b2)
- [infoq.com: Turning Microservices Inside-Out](https://www.infoq.com/articles/microservices-inside-out/)
- [towardsdatascience.com: Architecture for High-Throughput Low-Latency Big Data Pipeline on Cloud 🌟](https://towardsdatascience.com/scalable-efficient-big-data-analytics-machine-learning-pipeline-architecture-on-cloud-4d59efc092b5) Scalable and efficient data pipelines are as important for the success of analytics, data science, and machine learning as reliable supply lines are for winning a war.
- [dzone: RESTful Applications in An Event-Driven Architecture](https://dzone.com/articles/restful-applications-in-an-event-driven-architecture) Hybrid architecture with both RESTful and event-driven services.
- [developers.redhat.com: Distributed transaction patterns for microservices compared](https://developers.redhat.com/articles/2021/09/21/distributed-transaction-patterns-microservices-compared)
- [thenewstack.io: The Rise of Event-Driven Architecture ](https://thenewstack.io/the-rise-of-event-driven-architecture/)
- [jinwookim928.medium.com: Why Not Event Driven Architecture?](https://jinwookim928.medium.com/intro-to-event-driven-architecture-79914e5969d7)
- [thenewstack.io: Streaming Data and the Modern Real-Time Data Stack](https://thenewstack.io/streaming-data-and-the-modern-real-time-data-stack/)

	|  | **Modern Data Stack** | **Modern Real-Time Data Stack** | 
	| :--- | :--- | :--- | 
	| Language | SQL | SQL |
	| Deployment | Cloud-native | Cloud-native |
	| Data Ops | Complex batch transformations every 15 minutes, hourly or daily | Simple incremental transformations every second |
	| Insights | Monthly, Weekly or Daily | Instantly |
	| Cost | Affordable at massive scale | Affordable at massive scale and speed |

- [blog.direktiv.io: Event driven orchestration with Knative (part 1)](https://blog.direktiv.io/event-driven-orchestration-with-knative-part-1-fbdcc0e2ea03)
- [blog.direktiv.io: Redefining event-driven orchestration for automation & applications](https://blog.direktiv.io/redefining-event-driven-orchestration-for-automation-applications-ec07d79f21c0)
- [pub.towardsai.net: Deep Dive into Event-Driven architecture | Gul Ershad](https://pub.towardsai.net/software-engineering-baa4e7a8015c)
## RPC vs Messaging
- [particular.net: RPC vs. Messaging – which is faster?](https://particular.net/blog/rpc-vs-messaging-which-is-faster)

## Message Brokers
- [Apache ActiveMQ](https://activemq.apache.org/)
- [Dzone: Introduction to Message Brokers. Part 1: Apache Kafka vs. RabbitMQ](https://dzone.com/articles/introduction-to-message-brokers-part-1-apache-kafk)
- [Dzone: Introduction to Message Brokers. Part 2: ActiveMQ vs. Redis Pub/Sub](https://dzone.com/articles/introduction-to-message-brokers-part-2-activemq-vs)
- [developers.redhat.com: Choosing the right asynchronous-messaging infrastructure for the job](https://developers.redhat.com/blog/2020/07/31/choosing-the-right-asynchronous-messaging-infrastructure-for-the-job/)

### ActiveMQ message broker
- [ActiveMQ 5.x "classic"](https://activemq.apache.org/components/classic/)
- [ActiveMQ Artemis](https://activemq.apache.org/components/artemis/) Apache ActiveMQ is a subproject of Apache ActiveMQ. It has been donated to the Apache Software Foundation in 2015. There were lots of changes in project names in the past. The Artemis project first started as JBoss Messaging and got renamed to HornetQ in August 2009.
- [Apache Artemis JMeter](https://github.com/apache/activemq-artemis/tree/master/examples/perf/jmeter) Running the ActiveMQ Artemis JMeter Performance Testing Examples.
- [developers.redhat.com: Implementing Apache ActiveMQ-style broker meshes with Apache Artemis](https://developers.redhat.com/articles/2021/06/30/implementing-apache-activemq-style-broker-meshes-apache-artemis)

### RabbitMQ message broker
- [K8s prevent queue worker Pod from being killed during deployment](https://itnext.io/k8s-prevent-queue-worker-pod-from-being-killed-during-deployment-4252ea7c13f6) How to prevent a Kubernetes (like RabbitMQ) queue worker Pod from being killed during deployment while handling a message?
- [medium.com: **RabbitMQ vs. Kafka**](https://medium.com/better-programming/rabbitmq-vs-kafka-1ef22a041793) An architect’s dilemma
- [blog.rabbitmq.com: First Application With RabbitMQ Streams](https://blog.rabbitmq.com/posts/2021/07/rabbitmq-streams-first-application/)
- [geshan.com.np: How to use RabbitMQ and Node.js with Docker and Docker-compose](https://geshan.com.np/blog/2021/07/rabbitmq-docker-nodejs/)

### Redis message broker
- [Redis](https://redis.io/)
- [Redis Pub/sub](https://redis.io/topics/pubsub)

### Apache Camel message broker
- [Apache Camel](https://camel.apache.org/) Camel is an Open Source integration framework that empowers you to quickly and easily integrate various systems consuming or producing data. In version 3 we use <5MB memory, including the JVM. Also reflection free, low GC, super modular, native compilation friendly.
- [Quora.com: What's the difference between Apache Camel and Kafka?](https://www.quora.com/Whats-the-difference-between-Apache-Camel-and-Kafka)
- [dzone: Hybrid multi-cloud event mesh architectural design](https://dzone.com/articles/building-a-hybrid-multi-cloud-event-mesh-demo-with) Building the event mesh with Camel
- [developers.redhat.com: Integrating systems with Apache Camel and Quarkus on Red Hat OpenShift](https://developers.redhat.com/articles/2021/05/17/integrating-systems-apache-camel-and-quarkus-red-hat-openshift)

#### Apache Camel K
- [Apache Camel K](https://camel.apache.org/camel-k/latest/) is a lightweight cloud-integration platform that runs natively on Kubernetes. Based on the famous Apache Camel, Camel K is designed and optimized for serverless and microservices architectures.
- [developers.redhat.com: Six reasons to love Camel K](https://developers.redhat.com/blog/2020/05/12/six-reasons-to-love-camel-k/)
- [developers.redhat.com: Extending Kafka connectivity with Apache Camel Kafka connectors](https://developers.redhat.com/blog/2020/05/19/extending-kafka-connectivity-with-apache-camel-kafka-connectors/)
- [developers.redhat.com: Design event-driven integrations with Kamelets and Camel K](https://developers.redhat.com/blog/2021/04/02/design-event-driven-integrations-with-kamelets-and-camel-k)
- [thenewstack.io: Camel K Brings Apache Camel to Kubernetes for Event-Driven Architectures](https://thenewstack.io/camel-k-brings-apache-camel-to-kubernetes-for-event-driven-architectures/)

### KubeMQ message broker
- [KubeMQ.io: Kubernetes Native Message Queue Broker](https://kubemq.io/)
- [devops.com: Best of 2019: Implementing Message Queue in Kubernetes](https://devops.com/implementing-message-queue-in-kubernetes/)
- [kubemq.io: Kafka VS KubeMQ 🌟](https://kubemq.io/kafka-vs-kubemq/)
- [github.com/kubemq-io/kubemq-community 🌟](https://github.com/kubemq-io/kubemq-community) KubeMQ community version is now available as an open-source project!
- [dzone: KubeMQ: A Modern Alternative to Kafka](https://dzone.com/articles/seamless-migration-from-kafka-to-kubemq) This article introduces a modern, Kubernetes-native message queue called KubeMQ, to show how organizations trying to implement Kafka on Kubernetes can benefit from it.

### Google Cloud Platform Pub/Sub
- [Google Cloud Platform Pub/Sub](https://cloud.google.com/pubsub/docs/overview)
- [A generic framework of concurrent consumers for Google Cloud Platform Pub/Sub 🌟](https://towardsdatascience.com/a-python-implementation-of-concurrent-consumers-for-google-cloud-platform-pub-sub-991ae8b9841d) An example shows how to publish messages to Pub/Sub and build a service to consume the messages concurrently using the Python multiprocessing module

## Cloud Based Integration. Integration Platform-as-a-Service (iPaaS) solutions 
- [Wikipedia: Cloud Based Integration (iPaaS)](https://en.wikipedia.org/wiki/Cloud-based_integration)
- Integration Platform as a Service (iPaaS) is a suite of cloud services enabling development, execution and governance of integration flows connecting any combination of on premises and cloud-based processes, services, applications and data within individual or across multiple organizations.
- Integration platform as a service (iPaaS) is a set of automated tools for connecting software applications that are deployed in different environments. iPaaS is often used by large business-to-business (B2B) enterprises that need to integrate on-premises applications and data with cloud applications and data.
- [blog.axway.com: What is iPaaS?](https://blog.axway.com/hybrid-integration/whats-ipaas)
- [ibm.com: iPaaS (Integration-Platform-as-a-Service)](https://www.ibm.com/cloud/learn/ipaas): iPaaS is a cloud-based solution that simplifies application integration across on-premises and cloud environments, to help you accelerate innovation and lower your integration and operations costs.

### Red Hat Fuse and Red Hat Fuse Online
- [**Red Hat Fuse**](https://www.redhat.com/en/technologies/jboss-middleware/fuse)
- [**Red Hat Fuse Online**](https://www.redhat.com/en/technologies/jboss-middleware/fuse-online)
    
### Syndesis open source integration platform 
- [**Syndesis** open source integration platform](https://syndesis.io/) (OpenSource Project for **Red Hat Fuse Online**)
- [developers.redhat.com: Low-code microservices orchestration with Syndesis](https://developers.redhat.com/blog/2020/03/25/low-code-microservices-orchestration-with-syndesis/)

## Debezium open source distributed platform for Change Data Capture (CDC) software design pattern
- **Change Data Capture**, or **CDC**, is a well-established **software design pattern** for a system that monitors and captures the changes in data so that other software can respond to those changes. CDC captures row-level changes to database tables and passes corresponding change events to a data streaming bus. Applications can read these change event streams and access these change events in the order in which they occurred.
- [**Debezium**:](https://debezium.io/) Stream changes from your database
- [developers.redhat.com: Decoupling microservices with Apache Camel and Debezium](https://developers.redhat.com/blog/2019/11/19/decoupling-microservices-with-apache-camel-and-debezium/)
- [A good explanation of how to avoid distributed transactions using outbox pattern: Transaction Log Tailing With Debezium](https://medium.com/trendyol-tech/transaction-log-tailing-with-debezium-part-1-aeb968d72220)
- [developers.redhat.com: Capture database changes with Debezium Apache Kafka connectors](https://developers.redhat.com/blog/2020/04/14/capture-database-changes-with-debezium-apache-kafka-connectors/)
- [developers.redhat.com: Change data capture for microservices without writing any code](https://developers.redhat.com/blog/2020/05/15/change-data-capture-for-microservices-without-writing-any-code/)
- [debezium.io: Lessons Learned from Running Debezium with PostgreSQL on Amazon RDS](https://debezium.io/blog/2020/02/25/lessons-learned-running-debezium-with-postgresql-on-rds/)
- [info.crunchydata.com: PostgreSQL Change Data Capture With Debezium](https://info.crunchydata.com/blog/postgresql-change-data-capture-with-debezium)
- [medium.com: Stream Your Database into Kafka with Debezium](https://medium.com/comsystoreply/stream-your-database-into-kafka-with-debezium-a94b2f649664) An Introduction and Experience Report. Insightful post by David Hettler of 
comsysto about their usage of Debezium, touching on many details like outbox pattern, Avro schemas, Postgres on RDS etc.
- [noti.st: Change Data Capture with Flink SQL and Debezium 🌟](https://noti.st/morsapaes/liQzgs/change-data-capture-with-flink-sql-and-debezium)
- [vladmihalcea.com: A beginner’s guide to CDC (Change Data Capture)](https://vladmihalcea.com/a-beginners-guide-to-cdc-change-data-capture/)
- [shopify.engineering: Capturing Every Change From Shopify’s Sharded Monolith](https://shopify.engineering/capturing-every-change-shopify-sharded-monolith)
- [developers.redhat.com: Db2 and Oracle connectors coming to Debezium 1.4 GA](https://developers.redhat.com/blog/2021/03/25/db2-and-oracle-connectors-coming-to-debezium-1-4-ga)
- [medium: Change Data Capture — Using Debezium](https://medium.com/geekculture/change-data-capture-using-debezium-ec48631d643a)
- [daily.dev: Building a fault-tolerant event-driven architecture with Google Cloud, Pulumi and Debezium](https://daily.dev/blog/building-a-fault-tolerant-event-driven-architecture-with-google-cloud-pulumi-and-debezium)
- [pradeepdaniel.medium.com: Creating an ETL data pipeline to sync data to Snowflake using Kafka and Debezium](https://pradeepdaniel.medium.com/real-time-change-data-replication-to-snowflake-using-kafka-and-debezium-d6ebb0d4eb29) Setting up a real-time data pipeline from scratch to sync data from transactional databases to Snowflake cloud warehouse.
- [medium: A Visual Introduction to Debezium 🌟](https://medium.com/event-driven-utopia/a-visual-introduction-to-debezium-32563e23c6b8) A story-based introduction to understanding what Debezium is, how it is made of, and how it works in a real-world scenario
- [debezium.io: Using Debezium to Create a Data Lake with Apache Iceberg](https://debezium.io/blog/2021/10/20/using-debezium-create-data-lake-with-apache-iceberg/)

## Red Hat Integration service registry and Apicurio
- [Red Hat Integration service registry](https://developers.redhat.com/blog/2019/12/16/getting-started-with-red-hat-integration-service-registry/)
- [**Apicurio** Registry](https://github.com/apicurio/apicurio-registry) An API/Schema registry - stores APIs and Schemas.
- [Event streaming and data federation: A citizen integrator’s story](https://developers.redhat.com/blog/2020/06/12/event-streaming-and-data-federation-a-citizen-integrators-story/)
- [redhat.com: Using a schema registry to ensure data consistency between microservices](https://www.redhat.com/architect/schema-registry) Make interservice communication easier by using a schema registry.

## Data Mesh
- [martinfowler.com: Data Mesh Principles and Logical Architecture](https://martinfowler.com/articles/data-mesh-principles.html)
- [infoq.com: Data Mesh Principles and Logical Architecture Defined](https://www.infoq.com/news/2020/12/data-mesh-architecture/)
- [martinfowler.com: How to Move Beyond a Monolithic Data Lake to a Distributed Data Mesh](https://martinfowler.com/articles/data-monolith-to-mesh.html)
- [towardsdatascience.com: Data Domains and Data Products](https://towardsdatascience.com/data-domains-and-data-products-64cc9d28283e) Practical guidance from the field

## Data Processing (aka Streaming Data, Data Pipeline or Big Data Pipeline)
- [Awesome Streaming](https://github.com/manuzhang/awesome-streaming) A curated list of awesome [streaming (stream processing)](https://www.oreilly.com/radar/the-world-beyond-batch-streaming-101/) frameworks, applications, readings and other resources.
- [cloudblog.withgoogle.com: Turn any Dataflow pipeline into a reusable template](https://cloudblog.withgoogle.com/products/data-analytics/create-templates-from-any-dataflow-pipeline/amp/)
- [thenewstack.io: Part 1: The Evolution of Data Pipeline Architecture](https://thenewstack.io/part-1-the-evolution-of-data-pipeline-architecture/)
- [eng.uber.com: Uber’s Journey Toward Better Data Culture From First Principles](https://eng.uber.com/ubers-journey-toward-better-data-culture-from-first-principles/)
- [satishchandragupta.com: Scalable Efficient Big Data Pipeline Architecture](https://www.satishchandragupta.com/tech/scalable-efficient-big-data-analytics-machine-learning-pipeline-architecture-on-cloud.html)
- [openshift.com: How to Orchestrate Data Pipelines with Applications Deployed on OpenShift](https://www.openshift.com/blog/how-to-orchestrate-data-pipelines-with-applications-deployed-on-openshift)

### Apache Kafka
- [Apache Kafka](https://kafka.apache.org/)
- [developers.redhat.com: Using secrets in Kafka Connect configuration](https://developers.redhat.com/blog/2020/02/14/using-secrets-in-apache-kafka-connect-configuration/)
- [developers.redhat.com: Capture database changes with Debezium Apache Kafka connectors](https://developers.redhat.com/blog/2020/04/14/capture-database-changes-with-debezium-apache-kafka-connectors/)
- [Awesome Kafka](https://github.com/monksy/awesome-kafka/blob/master/tools.md)
- [Single Message Transformations - The Swiss Army Knife of Kafka Connect](https://www.morling.dev/blog/single-message-transforms-swiss-army-knife-of-kafka-connect/)
- [medium: Logs & Offsets: (Near) Real Time ELT with Apache Kafka + Snowflake](https://medium.com/convoy-tech/logs-offsets-near-real-time-elt-with-apache-kafka-snowflake-473da1e4d776) Replacing Apache Airflow with Debezium. 
- [medium: Apache Kafka Startup Guide: System Design Architectures: Notification System, Web Activity Tracker, ELT Pipeline, Storage System 🌟](https://medium.com/swlh/apache-kafka-startup-guide-system-design-architectures-notification-system-web-activity-tracker-6dcaf0cf8a7)
- [medium: Getting Started With Kafka on OpenShift](https://medium.com/swlh/getting-started-with-kafka-on-openshift-c44c0fdec384)
- [containerjournal.com: Red Hat Platform Brings Kafka Closer to Kubernetes](https://containerjournal.com/topics/container-management/red-hat-platform-brings-kafka-closer-to-kubernetes/)
- [lightbend.com: Monitor Kafka Consumer Group Latency with Kafka Lag Exporter](https://www.lightbend.com/blog/monitor-kafka-consumer-group-latency-with-kafka-lag-exporter)
- [AKHQ (previously known as KafkaHQ) 🌟](https://github.com/tchiotludo/akhq) Kafka GUI for Apache Kafka to manage topics, topics data, consumers group, schema registry, connect and more...
- [banzaicloud.com: Kafka Schema Registry on Kubernetes the declarative way](https://banzaicloud.com/blog/kafka-schemareg/)
- [Build a simple cloud-native change data capture pipeline](https://developers.redhat.com/blog/2020/07/02/build-a-simple-cloud-native-change-data-capture-pipeline/)
- [banzaicloud.com: Bulletproof Kafka, and the tale of an Amazon outage](https://banzaicloud.com/blog/supertubes-focal/)=
- [confluent.fr: Infrastructure Modernization with Google Anthos and Apache Kafka](https://www.confluent.fr/blog/modernize-apps-and-infrastructure-with-anthos-confluent-kafka/)
- [confluent.io: Apache Kafka DevOps with Kubernetes and GitOps](https://www.confluent.io/blog/kafka-devops-with-confluent-kubernetes-and-gitops/)
- [Build a data streaming pipeline using Kafka Streams and Quarkus](https://developers.redhat.com/blog/2020/09/28/build-a-data-streaming-pipeline-using-kafka-streams-and-quarkus/)
- [levelup.gitconnected.com: Kafka for Engineers 🌟](https://levelup.gitconnected.com/kafka-for-engineers-975feaea6067) Here are things about Kafka that you need to understand as a software engineer.
- [confluent.io: How to Build and Deploy Scalable Machine Learning in Production with Apache Kafka](https://www.confluent.io/blog/build-deploy-scalable-machine-learning-production-apache-kafka/)
- [banzaicloud.com: Kafka on Kubernetes - using etcd 🌟](https://banzaicloud.com/blog/kafka-on-etcd/)
- [softwareengineeringdaily.com: Kafka Applications with Tim Berglund (podcast) 🌟](https://softwareengineeringdaily.com/2020/12/16/kafka-applications-with-tim-berglund-repeat/)
- [medium: Logs & Offsets: (Near) Real Time ELT with Apache Kafka + Snowflake](https://medium.com/convoy-tech/logs-offsets-near-real-time-elt-with-apache-kafka-snowflake-473da1e4d776)
- [infoq.com: Building a SQL Database Audit System using Kafka, MongoDB and Maxwell's Daemon](https://www.infoq.com/articles/database-audit-system-kafka/)
- [tecmint: How to Install Apache Kafka in CentOS/RHEL 7](https://www.tecmint.com/install-apache-kafka-in-centos-rhel/)
- [medium: Processing guarantees in Kafka](https://medium.com/@andy.bryant/processing-guarantees-in-kafka-12dd2e30be0e) "Duplicates and lost messages are due not only to features of the messaging systems, but in the design of producer and consumer applications as well." One of the best posts on processing guarantees in kafka.
- [davidxiang.com: Kafka As A Database? Yes Or No](https://davidxiang.com/2021/01/10/kafka-as-a-database/)
- [medium: How Pinterest runs Kafka at scale](https://medium.com/pinterest-engineering/how-pinterest-runs-kafka-at-scale-ff9c6f735be)
- [medium: Google Pub/Sub Lite for Kafka Users](https://medium.com/google-cloud/google-pub-sub-lite-for-kafka-users-dec8a7cfc5e5)
- [medium: 4 Microservices Caching Patterns at Wix](https://medium.com/wix-engineering/4-microservices-caching-patterns-at-wix-b4dfee1ae22f)
- [Confluent.io: Intro to Apache Kafka: How Kafka Works 🌟](https://www.confluent.io/blog/apache-kafka-intro-how-kafka-works/)
- [levelup.gitconnected.com: Kafka for Engineers](https://levelup.gitconnected.com/kafka-for-engineers-975feaea6067)
- [medium: Microservices in Rust with Kafka](https://medium.com/digitalfrontiers/microservices-in-rust-with-kafka-2b671295b24e)
- [medium: Apache Kafka in a Nutshell 🌟](https://medium.com/swlh/apache-kafka-in-a-nutshell-5782b01d9ffb) Architecture, Use Cases, and a Getting Started guide — rolled into one
- [confluent.io: Simplifying Apache Kafka Multi-Cluster Management Using Control Center and Cluster Registry](https://www.confluent.io/blog/simplify-multiple-kafka-cluster-management-monitoring-using-confluent)
- [kai-waehner.de: App Modernization and Hybrid Cloud Architectures with Apache Kafka](https://www.kai-waehner.de/blog/2021/03/10/apache-kafka-app-modernization-legacy-hybrid-cloud-native-architecture)
- [kai-waehner.de: Apache Kafka and MQTT (Part 1 of 5) – Overview and Comparison](https://www.kai-waehner.de/blog/2021/03/15/apache-kafka-mqtt-sparkplug-iot-blog-series-part-1-of-5-overview-comparison/)
- [medium: Solutions to Communication Problems in Microservices using Apache Kafka and Kafka Lens](https://medium.com/@harmonh/solutions-to-communication-problems-in-microservices-using-apache-kafka-and-kafka-lens-9b6d453de352)
- [kafka-tutorials.confluent.io 🌟](https://kafka-tutorials.confluent.io/)
	- [kafka-tutorials.confluent.io: How to join a stream and a lookup table 🌟](https://kafka-tutorials.confluent.io/join-a-stream-to-a-table/kstreams.html) If I have events in a Kafka topic and a table of reference data (aka a lookup table), how can I join each event in the stream to a piece of data in the table based on a common key?
- [confluent.io: DevOps for Apache Kafka with Kubernetes and GitOps 🌟](https://www.confluent.io/blog/devops-for-apache-kafka-with-kubernetes-and-gitops)
- [dzone.com: Microservices, Event-Driven Architecture and Kafka 🌟](https://dzone.com/articles/microservices-event-driven-architecture-and-kafka) 
- [medium: Understanding Kafka Topic Partitions](https://medium.com/event-driven-utopia/understanding-kafka-topic-partitions-ae40f80552e8) Everything in Kafka is modeled around partitions. They rule Kafka’s storage, scalability, replication, and message movement.
- [kafka-tutorials.confluent.io: How to count messages in a Kafka topic](https://kafka-tutorials.confluent.io/how-to-count-messages-on-a-kafka-topic/ksql.html)
- [confluent.io: Apache Kafka Made Simple: A First Glimpse of a Kafka Without ZooKeeper 🌟](https://www.confluent.io/blog/kafka-without-zookeeper-a-sneak-peek/)
- [piotrminkowski.com: Knative Eventing with Kafka and Quarkus](https://piotrminkowski.com/2021/03/31/knative-eventing-with-kafka-and-quarkus/)
- [blog.cloudera.com: Scalability of Kafka Messaging using Consumer Groups](https://blog.cloudera.com/scalability-of-kafka-messaging-using-consumer-groups/)
- [thenewstack.io: Beyond the Quickstart: Running Apache Kafka as a Service on Kubernetes](https://thenewstack.io/beyond-the-quickstart-running-apache-kafka-as-a-service-on-kubernetes/)
- [towardsdatascience.com: You Can Replace Kafka with a Database](https://towardsdatascience.com/you-can-replace-kafka-with-a-database-39e13b610b63)
- [Handling Retries in Kafka: If You’re Using Kafka With Your Microservices, You’re Probably Handling Retries Wrong](https://dt-23597.medium.com/if-youre-using-kafka-with-your-microservices-you-re-probably-handling-retries-wrong-8492890899fa)
- [Kafdrop – Kafka Web UI 🌟](https://github.com/obsidiandynamics/kafdrop)
- [confluent.io: What’s New in Apache Kafka 2.8](https://www.confluent.io/blog/kafka-2-8-0-features-and-improvements-with-early-access-to-kip-500/)
- [devclass.com: Apache Kafka 2.8.0 previews life without ZooKeeper](https://devclass.com/2021/04/20/apache-kafka-2-8-0-previews-life-without-zookeeper/)
- [KLoadGen - Kafka + (Avro/Json Schema) Load Generator 🌟](https://github.com/corunet/kloadgen) KLoadGen is kafka load generator plugin for jmeter designed to work with AVRO and JSON schema. It allows sending kafka messages with a structure defined as an AVRO Schema or a Json Schema. It connects to the Scheme Registry Server, retrieve the subject to send and generate a random message every time.
- [instaclustr.com: Apache Kafka Architecture: A Complete Guide 🌟](https://www.instaclustr.com/apache-kafka-architecture/)
- [youtube playlist: Kafka Connect Tutorials | Kafka Connect 101: REST API 🌟](https://www.youtube.com/watch?v=9wu-j9gIlBY&list=PLa7VYi0yPIH1MB2n2w8pMZguffCDu2L4Y&index=8&ab_channel=Confluent) KafkaConnect uses a REST API to expose its management capabilities. tlberglund demonstrates many of the key functions available using the REST API, including creating connectors, viewing their status, and accessing troubleshooting information.
- [developers.redhat.com: Event-driven APIs and schema governance for Apache Kafka: Get ready for Kafka Summit Europe 2021](https://developers.redhat.com/blog/2021/05/04/event-driven-apis-and-schema-governance-for-apache-kafka-get-ready-for-kafka-summit-europe-2021/)
- [developers.redhat.com: Building resilient event-driven architectures with Apache Kafka](https://developers.redhat.com/blog/2021/05/05/building-resilient-event-driven-architectures-with-apache-kafka/)
- [tech.ebayinc.com: Resiliency and Disaster Recovery with Kafka](https://tech.ebayinc.com/engineering/resiliency-and-disaster-recovery-with-kafka/)
- [dev.to: Learn how to use Kafkacat – the most versatile Kafka CLI client 🌟](https://dev.to/de_maric/learn-how-to-use-kafkacat-the-most-versatile-kafka-cli-client-1kb4)
- [newrelic.com: Effective Strategies for Kafka Topic Partitioning 🌟](https://newrelic.com/blog/best-practices/effective-strategies-kafka-topic-partitioning)
- [gentlydownthe.stream](https://www.gentlydownthe.stream/) A children’s book about Apache Kafka.
- [confluent.io: Apache Kafka Made Simple: A First Glimpse of a Kafka Without ZooKeeper](https://www.confluent.io/blog/kafka-without-zookeeper-a-sneak-peek/)
- [dzone: Event-Driven APIs and Schema Governance for Apache Kafka](https://dzone.com/articles/event-driven-apis-and-schema-governance-for-apache) As a developer, I'm always excited to attend so many great sessions addressing critical challenges in the Apache Kafka ecosystem like how changes to event-driven APIs are leading developers to focus on contract-first development for Kafka.
- [phoenixnap.com: How to Set Up and Run Kafka on Kubernetes 🌟](https://phoenixnap.com/kb/kafka-on-kubernetes)
- [piotrminkowski.com: Knative Eventing with Quarkus, Kafka and Camel](https://piotrminkowski.com/2021/06/14/knative-eventing-with-quarkus-kafka-and-camel/)
- [itnext.io: Configuring Kafka Sources and Sinks declaratively in Kubernetes using Knative](https://itnext.io/configuring-kafka-sources-and-sinks-in-kubernetes-271e3757b208) This solves the complexity in work flow of compiling JARs and uploading them to a Kafka connect cluster. Using Knative it can be possible to leverage the Kubernetes cluster and define Kafka sources and sinks with Kubernetes objects.
- [strimzi.io: Kafka upgrade improvements](https://strimzi.io/blog/2021/07/05/upgrade-improvements/)
- [developers.redhat.com: Getting started with Red Hat OpenShift Streams for Apache Kafka](https://developers.redhat.com/articles/2021/07/07/getting-started-red-hat-openshift-streams-apache-kafka)
- [developers.redhat.com: Managing the API life cycle in an event-driven architecture: A practical approach 🌟](https://developers.redhat.com/articles/2021/07/07/managing-api-life-cycle-event-driven-architecture-practical-approach)
- [baeldung.com: List Active Brokers in a Kafka Cluster Using Shell Commands 🌟](https://www.baeldung.com/ops/kafka-list-active-brokers-in-cluster)
- [developers.redhat.com: How to secure Apache Kafka schemas with Red Hat Integration Service Registry 2.0](https://developers.redhat.com/articles/2021/07/16/how-secure-apache-kafka-schemas-red-hat-integration-service-registry-20)
- [mercurytfs.blogspot.com: Colas Kafka](https://mercurytfs.blogspot.com/2021/07/colas-kafka.html)
- [grafana.com: Get comprehensive monitoring for your Apache Kafka ecosystem instances quickly with Grafana Cloud](https://grafana.com/blog/2021/07/26/get-comprehensive-monitoring-for-your-apache-kafka-ecosystem-instances-quickly-with-grafana-cloud/)
- [dzone: Next-Gen Data Pipes With Spark, Kafka and k8s 🌟](https://dzone.com/articles/next-gen-data-pipes-with-spark-kafka-and-k8s) This article examines the architecture patterns and provides some sample code for the readers to implement in their own environment.
- [github.com/lensesio/fast-data-dev (Lenses Box)](https://github.com/lensesio/fast-data-dev) Kafka Docker for development. Kafka, Zookeeper, Schema Registry, Kafka-Connect, Landoop Tools, 20+ connectors. A apachekafka docker image that actually works without zookeeper. If you don't want do deal with docker-compose this one is for you.
- [confluent.io: Making Apache Kafka Serverless: Lessons From Confluent Cloud](https://www.confluent.io/blog/designing-an-elastic-apache-kafka-for-the-cloud/)
- [developer.confluent.io 🌟🌟](https://developer.confluent.io/) over ten hours of FREE video courses with hands-on exercises, 50+ event streaming patterns, deep-dive articles on Kafka's internals, and a ton more.
- [itnext.io: Sending Messages to Kafka in Kubernetes](https://itnext.io/sending-messages-to-kafka-cfb5a246f5eb)
- [cloudhut.dev: Running Apache Kafka on Kubernetes successfully](https://cloudhut.dev/blog/2021-06-24-running-kafka-on-kubernetes/) A comparison for different installation methods for running Kafka in Kubernetes
- [developers.redhat.com: The outbox pattern with Apache Kafka and Debezium 🌟](https://developers.redhat.com/articles/2021/09/01/outbox-pattern-apache-kafka-and-debezium)
- [towardsdatascience.com: Overview of UI Tools for Monitoring and Management of Apache Kafka Clusters](https://towardsdatascience.com/overview-of-ui-tools-for-monitoring-and-management-of-apache-kafka-clusters-8c383f897e80)
- [analyticsindiamag.com: How Uber is Leveraging Apache Kafka For More Than 300 Micro Services](https://analyticsindiamag.com/how-uber-is-leveraging-apache-kafka-for-more-than-300-micro-services/)
- [itnext.io: Securely Decoupling Kubernetes-based Applications on Amazon EKS using Kafka with SASL/SCRAM](https://itnext.io/securely-decoupling-applications-on-amazon-eks-using-kafka-with-sasl-scram-48c340e1ffe9) Securely decoupling Go-based microservices on Amazon EKS using Amazon MSK with IRSA, SASL/SCRAM, and data encryption
- [medium: Running Kafka in Kubernetes, Part 1: Why we migrated our Kafka clusters to Kubernetes](https://medium.com/transferwise-engineering/running-kafka-in-kubernetes-part-1-why-we-migrated-our-kafka-clusters-to-kubernetes-722101a2e751) At Wise, we chose to migrate our Apache Kafka clusters, previously running on Amazon Web Services (AWS) EC2 instances, into a multi-cluster Kubernetes setup. This article is the first part of a two-part series aiming to outline the motivations behind this choice and the challenges we faced.
- [betterprogramming.pub: How to Handle Duplicate Messages and Message Ordering in Kafka](https://betterprogramming.pub/how-to-handle-duplicate-messages-and-message-ordering-in-kafka-82e2fef82025) Dealing with the challenges faced when using Apache Kafka
- [medium: Optimizing Kafka Streams Apps on Kubernetes by Splitting Topologies](https://medium.com/bakdata/optimizing-kafka-streams-apps-on-kubernetes-by-splitting-topologies-ac6b4c90516e)

#### Strimzi kubernetes operator for apache kafka
- [strimzi.io](https://strimzi.io/)
- [developers.redhat.com: how easy to deploy and configure a Kafka Connect on Kubernetes through strimziio operator and use secrets](https://developers.redhat.com/blog/2020/02/14/using-secrets-in-apache-kafka-connect-configuration/)
- [developers.redhat.com: Introduction to Strimzi: Apache Kafka on Kubernetes (KubeCon Europe 2020) 🌟](https://developers.redhat.com/blog/2020/08/14/introduction-to-strimzi-apache-kafka-on-kubernetes-kubecon-europe-2020/)
- [strimzi.io: Optimizing Kafka producers](https://strimzi.io/blog/2020/10/15/producer-tuning/)
- [strimzi.io: Optimizing Kafka consumers 🌟](https://strimzi.io/blog/2021/01/07/consumer-tuning/)
- [strimzi.io: Optimizing Kafka producers 🌟](https://strimzi.io/blog/2020/10/15/producer-tuning/)
- [pepy.tech/project/strimzi-kafka-cli 🌟](https://pepy.tech/project/strimzi-kafka-cli) - [pypi.org/project/strimzi-kafka-cli](https://pypi.org/project/strimzi-kafka-cli/)
- [strimzi/kafka-kubernetes-config-provider: Kubernetes Configuration Provider for Apache Kafka](https://github.com/strimzi/kafka-kubernetes-config-provider) Apache Kafka supports pluggable configuration providers which can load configuration data from external sources. The configuration providers in this repo can be used to load data from Kubernetes Secrets and Config Maps. It can be used in all Kafka components and does not depend on the other Strimzi components. So you could, for example, use it with your producer or consumer applications even if you don't use the Strimzi operators to provide your Kafka cluster. One of the example use-cases is to load certificates or JAAS configuration from Kubernetes Secrets.
- [strimzi.io: Using Kubernetes Configuration Provider to load data from Secrets and Config Maps](https://strimzi.io/blog/2021/07/22/using-kubernetes-config-provider-to-load-data-from-secrets-and-config-maps/)
- [strimzi.io: Using HTTP Bridge as a Kubernetes sidecar](https://strimzi.io/blog/2021/08/18/using-http-bridge-as-a-kubernetes-sidecar/)
- [strimzi.io: Using Open Policy Agent with Strimzi and Apache Kafka](https://strimzi.io/blog/2020/08/05/using-open-policy-agent-with-strimzi-and-apache-kafka/)
- [strimzi/strimzi-canary](https://github.com/strimzi/strimzi-canary) This repository contains the Strimzi canary tool implementation. It acts as an indicator of whether Kafka clusters are operating correctly. This is achieved by creating a canary topic and periodically producing and consuming events on the topic and getting metrics out of these exchanges.

<center>
[![airflow vs kafka debezium](images/airflow_vs_debezium.jpg)](https://medium.com/convoy-tech/logs-offsets-near-real-time-elt-with-apache-kafka-snowflake-473da1e4d776)
</center>

#### Apache Kafka Desktop Clients
- [conduktor.io 🌟](https://www.conduktor.io/) Apache Kafka Desktop Client. We created Conduktor, the all-in-one friendly interface to work with the Kafka ecosystem. Develop and manage Apache Kafka with confidence.

### AWS Kinesis
- [AWS Kinesis](https://docs.aws.amazon.com/kinesis/index.html)
- [softkraft.co: WS Kinesis vs Kafka comparison: Which is right for you? 🌟](https://www.softkraft.co/aws-kinesis-vs-kafka-comparison/)

### MQTT
- [mqtt.org](https://mqtt.org/) MQTT: The Standard for IoT Messaging
- [developers.redhat.com: Deploying the Mosquitto MQTT message broker on Red Hat OpenShift, Part 1](https://developers.redhat.com/blog/2021/04/16/deploying-the-mosquitto-mqtt-message-broker-on-red-hat-openshift-part-1/)
	- [developers.redhat.com: Deploying the Mosquitto MQTT message broker on Red Hat OpenShift, Part 2](https://developers.redhat.com/blog/2021/04/26/deploying-the-mosquitto-mqtt-message-broker-on-red-hat-openshift-part-2)

### Banzai Cloud Supertubes (Cloud Native Kafka implementation)
- [Banzai Cloud](https://banzaicloud.com/)
- [Banzai Kafka Operator](https://github.com/banzaicloud/kafka-operator)
- [The benefits of integrating Apache Kafka with Istio](https://banzaicloud.com/blog/kafka-on-istio-benefits/)

### Confluent Cloud (Apache Kafka Re-engineered for the Cloud)
- [confluent.io](https://www.confluent.io/) The Complete Event Streaming Platform for Apache Kafka. 
- Focus on building apps and not managing clusters with a scalable, resilient and secure event streaming platform. Event streaming with Kafka made simple on AWS, Azure and GCP clouds.
- [mongodb.com: DaaS with MongoDB and Confluent](https://www.mongodb.com/blog/post/daa-s-with-mongo-db-and-confluent)
- [confluent.io: Confluent and Microsoft Announce Strategic Alliance](https://www.confluent.io/blog/confluent-microsoft-announce-strategic-alliance/)
- [confluent.io: Monitoring Your Event Streams: Integrating Confluent with Prometheus and Grafana](https://www.confluent.io/blog/monitor-kafka-clusters-with-prometheus-grafana-and-confluent)

### Redpanda (kafka alternative). A modern streaming platform for mission critical workloads
- [Redpanda 🌟](https://vectorized.io/) is a Kafka® compatible event streaming platform. No Zookeeper, no JVM, and no code changes required. Use all your favorite open source tooling - 10x faster.
- [hub.docker.com/r/vectorized/redpanda](https://hub.docker.com/r/vectorized/redpanda) Easy Docker experience to use VectorizedIO Redpanda in a container. Streaming platform for mission critical workloads, Kafka compatible, no Zookeeper, no JVM, no code changes required - 10x faster.
- [Redpanda is now Free & Source Available](https://vectorized.io/blog/open-source/) 
- [softwareengineeringdaily.com: Redpanda: Kafka Alternative with Alexander Gallego 🌟](https://softwareengineeringdaily.com/2021/01/22/redpanda-kafka-alternative-with-alexander-gallego/)


#### KsqlDB
- [ksqlDB](https://ksqldb.io/) The event streaming database purpose-built for stream processing applications.
- [Kafka Streams and ksqlDB Compared – How to Choose](https://www.confluent.io/blog/kafka-streams-vs-ksqldb-compared/)

### Apache Pulsar
- [Apache Pulsar](https://pulsar.apache.org/) is an open-source distributed pub-sub messaging system originally created at Yahoo and now part of the Apache Software Foundation
- [Pulsar vs Kafka – Comparison and Myths Explored](https://www.kai-waehner.de/blog/2020/06/09/apache-kafka-versus-apache-pulsar-event-streaming-comparison-features-myths-explored/)

### Apache Flink
- [Apache Flink](https://flink.apache.org/) Apache Flink is a framework and distributed processing engine for stateful computations over unbounded and bounded data streams. Flink has been designed to run in all common cluster environments, perform computations at in-memory speed and at any scale.
- [How to set up Apache Flink on Kubernetes for real time data processing](https://ci.apache.org/projects/flink/flink-docs-stable/ops/deployment/kubernetes.html)
- [flink.apache.org: How to natively deploy Flink on Kubernetes with High-Availability (HA)](https://flink.apache.org/2021/02/10/native-k8s-with-ha.html)

### Hazelcast JET
- [Hazelcast JET](https://jet-start.sh/) Open-Source Distributed Stream Processing
- [devops.com: Hazelcast Simplifies Streaming for Extremely Fast Event Processing in IoT, Edge and Cloud Environments](https://devops.com/hazelcast-simplifies-streaming-for-extremely-fast-event-processing-in-iot-edge-and-cloud-environments/)

## Workflow Engines
- [wikipedia: Workflow Engine](https://en.wikipedia.org/wiki/Workflow_engine)

## Zeebe
- [infoq.com: Event Streams and Workflow Engines – Kafka and Zeebe 🌟](https://www.infoq.com/news/2019/05/kafka-zeebe-streams-workflows)
- [Zeebe workflow engine](https://zeebe.io/)
- [Orchestration Made Easy with Zeebe and Kafka](https://www.softobiz.com/orchestration-made-easy-with-zeebe-and-kafka/)

### Apache Airflow
- [towardsdatascience.com: A journey to Airflow on Kubernetes](https://towardsdatascience.com/a-journey-to-airflow-on-kubernetes-472df467f556)
- [dzone: Apache Airflow Architecture on OpenShift](https://dzone.com/articles/apache-airflow-architecture-on-openshift)
- [redhat.com: Monitoring Apache Airflow using Prometheus](https://www.redhat.com/en/blog/monitoring-apache-airflow-using-prometheus)
- [towardsdatascience.com: Apache Airflow for containerized data-pipelines](https://towardsdatascience.com/apache-airflow-for-containerized-data-pipelines-4d7a3c385bd) Are you having problems running tasks with a different version of Python on Airflow? In this article, I explain how to solve this issue.
- [Apache Airflow official helm chart 🌟](https://airflow.apache.org/docs/helm-chart/)
- [youtube: Airflow Helm Chart : Quick Start For Beginners in 10mins](https://www.youtube.com/watch?v=GDOw8ByzMyY&ab_channel=MarcLamberti)
- [snowflake.com: Migrating Airflow from Amazon EC2 to Kubernetes](https://www.snowflake.com/blog/migrating-airflow-from-amazon-ec2-to-kubernetes/)
- [dev.to: Get started with Apache Airflow](https://dev.to/arunkc/get-started-with-apache-airflow-1218)

### Couler
- [Couler](https://github.com/couler-proj/couler) Couler aims to provide a unified interface for constructing and managing workflows on different workflow engines, such as Argo Workflows, Tekton Pipelines, and Apache Airflow.

## Red Hat AMQ (ActiveMQ Artemis broker and Apache Kafka)
- [**Red Hat AMQ overview**](https://developers.redhat.com/products/amq/overview)
- [Red Hat AMQ](https://www.redhat.com/en/technologies/jboss-middleware/amq) = AMQ Broker (Apache ActiveMQ Artemis) + AMQ Streams (Apache Kafka)

### Red Hat AMQ Broker (ActiveMQ Artemis)
- [Apache ActiveMQ Artemis broker](https://activemq.apache.org/components/artemis/)
- [developers.redhat.com: JDBC Master-Slave Persistence setup with Activemq using Postgresql database](https://developers.redhat.com/blog/2017/10/05/jdbc-master-slave-persistence-setup-activemq-using-postgresql-database)
- [developers.redhat.com: Connecting external clients to Red Hat AMQ Broker on Red Hat OpenShift](https://developers.redhat.com/blog/2020/08/26/connecting-external-clients-to-red-hat-amq-broker-on-red-hat-openshift)

### Red Hat AMQ Streams
- [Understanding Red Hat AMQ Streams components for OpenShift and Kubernetes 🌟](https://developers.redhat.com/blog/2019/12/04/understanding-red-hat-amq-streams-components-for-openshift-and-kubernetes-part-1/)
- [Red Hat **AMQ streams** (kafka): Simplify Apache Kafka on Red Hat OpenShift](https://www.redhat.com/en/resources/amq-streams-datasheet)
- [Set up **Red Hat AMQ Streams** custom certificates on OpenShift](https://developers.redhat.com/blog/2020/04/01/set-up-red-hat-amq-streams-custom-certificates-on-openshift-update/)
- [speakerdeck.com: Apache Kafka with Red Hat AMQ Streams 🌟](https://speakerdeck.com/mabulgu/apache-kafka-with-red-hat-amq-streams)
- [HTTP-based Kafka messaging with Red Hat AMQ Streams](https://developers.redhat.com/blog/2020/08/04/http-based-kafka-messaging-with-red-hat-amq-streams/#more-720187)
- [blog.jromanmartin.io: How to upgrade Strimzi Operator using the CLI](https://blog.jromanmartin.io/2020/09/25/how-upgrade-strimzi-operator.html)

<center>
[![AMQ in a nutshell](images/AMQ.png)](https://developers.redhat.com/products/amq/overview)
</center>

<center>

Product|Also Known As|Components|URL
:------|:----|:--------|:----
Red Hat AMQ 6|JBoss AMQ 6|Apache ActiveMQ|[Ref](https://access.redhat.com/documentation/en-us/red_hat_amq/6.3/)
Red Hat AMQ 7|JBoss AMQ 7 (Broker) or Red Hat AMQ 7 Suite|AMQ Broker + AMQ Streams|[Ref](https://access.redhat.com/documentation/en-us/red_hat_amq/6.3/)
Red Hat AMQ 7|JBoss AMQ 7 (Broker) or Red Hat AMQ 7 Suite|JBoss AMQ 7 (Broker) + Apache Kafka|[Ref](https://access.redhat.com/documentation/en-us/red_hat_amq/6.3/)
Red Hat AMQ 7|JBoss AMQ 7 (Broker) or Red Hat AMQ 7 Suite|Apache ActiveMQ Artemis + Apache Kafka|[Ref](https://access.redhat.com/documentation/en-us/red_hat_amq/6.3/)

</center>

<center>
<script async class="speakerdeck-embed" data-id="54c1ce6ee6e44d68a0c311c31ddc8225" data-ratio="1.77777777777778" src="//speakerdeck.com/assets/embed.js"></script>
</center>

## Open Data Hub AI-as-a-Service (AIaaS) platform
- [Open Data Hub](https://opendatahub.io/)
- [Open Data Hub 0.6 brings component updates and Kubeflow architecture](https://developers.redhat.com/blog/2020/05/07/open-data-hub-0-6-brings-component-updates-and-kubeflow-architecture/)
- [A development roadmap for Open Data Hub](https://developers.redhat.com/blog/2020/06/22/a-development-roadmap-for-open-data-hub/)

## KEDA. Kubernetes Event Driven Autoscaling
- [KEDA](https://keda.sh/) Kubernetes Event-driven Autoscaling. Application autoscaling made simple. https://github.com/kedacore/keda 
- [Dzone: Autoscaling Your Kubernetes Microservice with KEDA](https://dzone.com/articles/autoscaling-your-kubernetes-microservice-with-keda) Introduction to KEDA—event-driven autoscaler for Kubernetes, Apache Camel, and ActiveMQ Artemis—and how to use it to scale a Java microservice on Kubernetes.
- [tomd.xyz: Event-driven integration on Kubernetes with Camel & KEDA 🌟](https://tomd.xyz/kubernetes-event-driven-keda/) Can we develop apps in Kubernetes that autoscale based on events? Perhaps, with this example using KEDA, ActiveMQ and Apache Camel.
- [faun.pub: Scaling an app in Kubernetes with KEDA (no Prometheus is needed)](https://faun.pub/keda-ec9fc7c8dd81)

## Integration Platform as a Solution (iPaaS). Platforms for collecting, storing and routing customer event data
- [quandarycg.com: Everything You Need To Know About System Integration (And IPaaS) 🌟](https://quandarycg.com/everything-you-need-to-know-about-integrations/)
- [blog.hubspot.com: The 22 Best iPaaS Vendors for Any Budget](https://blog.hubspot.com/marketing/ipaas-vendors)

### IpaaS Vendors
- [rudderstack.com iPaaS](https://rudderstack.com/) - [opensource.com: Stream event data with rudderstack](https://opensource.com/article/21/4/event-streaming-rudderstack)
- [Mulesoft](https://www.mulesoft.com/)
- etc

## eBooks
- [O'Really: Streaming data](http://streamingsystems.net/)

## Related
- [Service meshes to the rescue: Load balancing and scaling long-lived connections in Kubernetes 🌟](https://learnk8s.io/kubernetes-long-lived-connections) Kubernetes doesn't load balance long-lived connections, some Pods might receive more requests than others, In case you are using HTTP/2, gRPC, RSockets, AMQP. Any work around?

## Questions and Answers
- [adambien.blog - 75th **airhacks.tv** Questions and Answers: Kafka, JAX-RS, MicroProfile, JSON-B, GSON, JWT, VSC, NetBeans, Java Fullstack](https://adambien.blog/roller/abien/entry/kafka_jax_rs_microprofile_json) "Kafka vs. JAX-RS / RPC, thoughts about APIs, JSON-B vs. GSON, Path.of over Paths.get, Java Records, MicroProfile JWT, beginners vs. expert content, best Java fullstack, code coverage, NetBeans in 2020, Visual Studio Setup for Java, screencast configuration, ReactJS / Angular over JSF?, JSON-P vs. JSON-B, security code scanning"

## Videos
<details>
  <summary>Click to expand!</summary>

<center>
<iframe width="560" height="315" src="https://www.youtube.com/embed/LieT75Zb_OY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>
</details>

## Tweets
<details>
  <summary>Click to expand!</summary>

<center>
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Pub-Sub ≠ Partitioning ≠ Multiplexing <a href="https://t.co/0ZVaH9Mxvr">pic.twitter.com/0ZVaH9Mxvr</a></p>&mdash; Clemens Vasters 🇪🇺☁📨 (@clemensv) <a href="https://twitter.com/clemensv/status/1288152399211909120?ref_src=twsrc%5Etfw">July 28, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">We are excited to announce that KubeMQ community version is now available as an open-source project!<br><br>The community version supports all messaging patterns, connectors, bridges, and run in production. Give us a star on Github if you like our project!<a href="https://t.co/0ufRQ5bhCE">https://t.co/0ufRQ5bhCE</a></p>&mdash; KubeMQ (@KubeMq) <a href="https://twitter.com/KubeMq/status/1436284885132529707?ref_src=twsrc%5Etfw">September 10, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
</center>
</details>