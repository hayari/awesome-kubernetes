# Java and Memory Management
- [Java Performance Optimization](#java-performance-optimization)
	- [Java on Kubernetes. Java Memory Arguments for Containers](#java-on-kubernetes-java-memory-arguments-for-containers)
	- [Benchmarking modern Java Virtual Machines and the next-generation garbage collectors](#benchmarking-modern-java-virtual-machines-and-the-next-generation-garbage-collectors)
	- [Relevant JVM Metrics](#relevant-jvm-metrics)
	- [Common JVM Errors](#common-jvm-errors)
	- [Tuning Jenkins GC](#tuning-jenkins-gc)
	- [Tuning Java Containers](#tuning-java-containers)
	- [Debugging java applications on OpenShift and Kubernetes](#debugging-java-applications-on-openshift-and-kubernetes)
- [List of Performance Analysis Tools](#list-of-performance-analysis-tools)
	- [Threadumps, Heapdumps and GC Analysis Tools](#threadumps-heapdumps-and-gc-analysis-tools)
- [Garbage Collection and Heap Offloading](#garbage-collection-and-heap-offloading)
- [Java Tracing Tools. JDK Flight Recorder](#java-tracing-tools-jdk-flight-recorder)
- [Cambios importantes en la gestión de memoria de Java 8 de Oracle (2014)](#cambios-importantes-en-la-gestión-de-memoria-de-java-8-de-oracle-2014)
- [Slides](#slides)
- [Tweets](#tweets)

## Java Performance Optimization
* [DZone refcard: java performance optimization 🌟](https://dzone.com/refcardz/java-performance-optimization) Tools and Techniques for Turbocharged Apps
- [DZone: String Concatenation's Effect on Performance](https://dzone.com/articles/string-concatentions-effect-on-performance) Don’t use the string concatenation operator to combine more than a few strings unless performance is irrelevant. Use StringBuilder’s append method instead. 
- [DZone: Performance Improvement in Java Applications: ORM/JPA 🌟](https://dzone.com/articles/performance-improvement-in-java-applications-orm-j)
- [DZone: The JVM Architecture Explained 🌟](https://dzone.com/articles/jvm-architecture-explained) An overview of the different components of the JVM, along with a very useful diagram
- [DZone: How to Troubleshoot Sudden CPU Spikes](https://dzone.com/articles/troubleshoot-sudden-cpu-spikes) Your Java application has been running fine, but all of a sudden CPU consumption starts to go higher and higher... sound familiar?
- [DZone refcard: Java Caching](https://dzone.com/refcardz/java-caching)
- [Dzone: 7 JVM Arguments of Highly Effective Applications 🌟🌟🌟](https://dzone.com/articles/7-jvm-arguments-of-highly-effective-applications-1) How to use 7 JVM arguments to help increase your application's performance and avoid common memory pitfalls.
- [developers.redhat.com: Get started with JDK Flight Recorder in OpenJDK 8u 🌟](https://developers.redhat.com/blog/2020/08/25/get-started-with-jdk-flight-recorder-in-openjdk-8u/) Deploy JDK Flight Recorder with JDK Mission Control, a new monitoring and profiling tool that exposes a high level of information without adding a tax on the runtime system
- [blog.heaphero.io: HeapHero - Java & Android Heap Dump Analyzer](https://blog.heaphero.io/)
- [blog.heaphero.io: What is GC Log, thread dump and Heapdump? 🌟](https://blog.heaphero.io/2020/10/16/what-is-gc-log-thread-dump-and-heapdump/) Java Virtual Machine (JVM) generates 3 critical #artifacts that are useful for optimizing the performance and troubleshooting production problems. Those artifacts & their differences are explained in this PDF.
- [developers.redhat.com: Shenandoah garbage collection in OpenJDK 16: Concurrent reference processing](https://developers.redhat.com/articles/2021/05/20/shenandoah-garbage-collection-openjdk-16-concurrent-reference-processing)
- [java-success.com: 01: 9 Java low latency interview questions & answers](https://www.java-success.com/writing-low-latency-applications-in-java/)
- [java-success.com: 9 Java Garbage Collection interview questions & answers](https://www.java-success.com/java-garbage-collection-interview-questions-and-answers/)
- [developers.redhat.com: JDK Flight Recorder support for GraalVM Native Image: The journey so far 🌟](https://developers.redhat.com/articles/2021/07/23/jdk-flight-recorder-support-graalvm-native-image-journey-so-far)
- [OpenHFT/Java-Thread-Affinity](https://github.com/OpenHFT/Java-Thread-Affinity) Bind a java thread to a given core. A library that lets you pin the threads of your Java application to specific CPU cores. Looks like an interesting part of the performance engineering toolbox, e.g. helping to reduce the number of cache misses.
- [dzone.com: Flight Recorder: Examining Java and Kotlin Apps](https://dzone.com/articles/flight-recorder-examining-java-and-kotlin-apps) Learn how to use Java's Flight Recorder to profile Java and Kotlin apps and get a close look at JVM internals.
- [==kstefanj.github.io: GC progress from JDK 8 to JDK 17==](https://kstefanj.github.io/2021/11/24/gc-progress-8-17.html) JVM with <5ms GC pauses (ZGC). JDK17 is a huge leap forward in benchmark after benchmark. Upgrade as fast as you can. Amazon’s Corretto builds are available for a huge number of platforms and distribution channels. The JRE disappeared with jdk9: use jlink to assemble exactly the JRE you need.

### Java on Kubernetes. Java Memory Arguments for Containers
- [medium: How to reduce your JVM app memory footprint in Docker and Kubernetes 🌟](https://medium.com/wix-engineering/how-to-reduce-your-jvm-app-memory-footprint-in-docker-and-kubernetes-d6e030d21298)
- [tech.olx.com: Improving JVM Warm-up on Kubernetes 🌟](https://tech.olx.com/improving-jvm-warm-up-on-kubernetes-1b27dd8ecd58) Vikas Kumar explains why you should not run your Java applications with a fixed quota of a single CPU core. Instead, use Burstable QoS to allow for increased CPU usage during start-up.
- [dzone: Best Practices: Java Memory Arguments for Containers 🌟](https://dzone.com/articles/best-practices-java-memory-arguments-for-container) In this article, we will discuss the possible JVM arguments that can be used to specify the Java heap size and the best option to choose.

### Benchmarking modern Java Virtual Machines and the next-generation garbage collectors
* [jet-start.sh: Performance of Modern Java on Data-Heavy Workloads, Part 1 🌟](https://jet-start.sh/blog/2020/06/09/jdk-gc-benchmarks-part1) The Java runtime has been evolving more rapidly in recent years and, after 15 years, we finally got a **new default garbage collector: the G1**. Two more GCs are on their way to production and are available as experimental features: **Oracle's ZGC** and **OpenJDK's Shenandoah**. We at Hazelcast thought it was time to put all these new options to the test and find which choices work well with workloads typical for our distributed stream processing engine, [Hazelcast Jet](https://jet-start.sh/).

### Relevant JVM Metrics
Metric|Details / Reference
:---|:---
GC Throughput|**Repeated Full GC happens way before OutOfMemoryError**<br/> [ref1](https://dzone.com/articles/7-jvm-arguments-of-highly-effective-applications-1)<br/>[ref2](https://blog.gceasy.io/2019/03/13/micrometrics-to-forecast-application-performance)
etc|

### Common JVM Errors
JVM Error|Details / Reference
:----|:----
OutOfMemoryError|**Repeated Full GC happens way before OutOfMemoryError** <br/> [ref1](https://dzone.com/articles/7-jvm-arguments-of-highly-effective-applications-1)<br/>[ref2](https://blog.gceasy.io/2019/03/13/micrometrics-to-forecast-application-performance)
StackOverflowError|[ref](https://blog.fastthread.io/2018/09/24/stackoverflowerror/)
etc|

### Tuning Jenkins GC
* [jenkins.io - Tuning Jenkins GC For Responsiveness and Stability with Large Instances 🌟](https://jenkins.io/blog/2016/11/21/gc-tuning/)
* [Running Jenkins on Java 11 🌟](https://www.jenkins.io/doc/administration/requirements/jenkins-on-java-11/#:~:text=The%20easiest%20way%20to%20run,images%2C%20use%20the%20jdk11%20tag.)

### Tuning Java Containers
* [blog.openshift.com: Scaling Java Containers 🌟](https://blog.openshift.com/scaling-java-containers/)
* [blog.openshift.com: Performance Metrics (APM) for Spring Boot Microservices on OpenShift](https://blog.openshift.com/performance-metrics-apm-spring-boot-microservices-openshift/)
* [dzone.com: Java RAM Usage in Containers: Top 5 Tips for Not Losing Your Memory](https://dzone.com/articles/java-ram-usage-in-containers-top-5-tips-not-to-los)
* [dzone.com: Running a JVM in a Container Without Getting Killed:](https://dzone.com/articles/running-a-jvm-in-a-container-without-getting-kille) Starting in JDK 9, and earlier if you use JDK 8u131, your JVM can detect how much memory is available when running inside a Docker container.
* [dzone.com: Java Inside Docker: What You Must Know to Not FAIL](https://dzone.com/articles/java-inside-docker-what-you-must-know-to-not-fail) If you've tried Java in containers, particularly Docker, you might have encountered some problems with the JVM and heap size. Here's how to fix it.
* [itnext.io: How to cold start fast a java service on k8s (EKS)](https://itnext.io/how-to-cold-start-fast-a-java-service-on-k8s-eks-3a7b4450845d)
* [blog.gceasy.io: Best practices: Java memory arguments for Containers 🌟](https://blog.gceasy.io/2020/11/05/best-practices-java-memory-arguments-for-containers/)

### Debugging java applications on OpenShift and Kubernetes
* [blog.openshift.com: Debugging Java Applications On OpenShift and Kubernetes](https://blog.openshift.com/debugging-java-applications-on-openshift-kubernetes/)

## List of Performance Analysis Tools
* [en.wikipedia.org/wiki/List_of_performance_analysis_tools](https://en.wikipedia.org/wiki/List_of_performance_analysis_tools)
* [InspectIT](https://en.wikipedia.org/wiki/InspectIT)
* [VisualVM](https://en.wikipedia.org/wiki/VisualVM)
* [OverOps](https://en.wikipedia.org/wiki/OverOps)
* [FusionReactor](https://en.wikipedia.org/wiki/FusionReactor)
* etc

### Threadumps, Heapdumps and GC Analysis Tools
* [geekflare.com: What is Thread Dump and How to Analyze them? 🌟](https://geekflare.com/generate-analyze-thread-dumps/)
* [baeldung.com: How to Analyze Java Thread Dumps 🌟](https://www.baeldung.com/java-analyze-thread-dumps)
* [baeldung.com: Capturing a Java Thread Dump](https://www.baeldung.com/java-thread-dump)
* [tier1app.com](https://tier1app.com/)
* [fastthread.io](https://fastthread.io/)
* [gceasy.io](https://gceasy.io/)
* [heaphero.io](https://heaphero.io/)

## Garbage Collection and Heap Offloading
- [Tecnologías de Heap-Offloading son EHcache, Memcached, Jillegal library, etc.](http://ehcache.org/)
- [Jillegal OffHeap Module](https://github.com/serkan-ozal/jillegal)
- [Free eGuide: JVM Troubleshooting Guide](http://freepromagazine.blogspot.de/2014/07/free-eguide-jvm-troubleshooting-guide.html)
- [Cambios importantes en la gestión de memoria de Java 8 de Oracle](http://karunsubramanian.com/websphere/one-important-change-in-memory-management-in-java-8/)
- [PermGen eliminado](http://www.infoq.com/articles/Java-PERMGEN-Removed)
- [On heap vs off heap memory usage](http://www.javacodegeeks.com/2014/12/on-heap-vs-off-heap-memory-usage.html)
- [How Garbage Collection differs in the three big JVMs](http://apmblog.dynatrace.com/2011/05/11/how-garbage-collection-differs-in-the-three-big-jvms/)
- [cubrid.org: How to Tune Java Garbage Collection](http://www.cubrid.org/blog/dev-platform/how-to-tune-java-garbage-collection)
- [DZone: Revisiting the Advanced Theories of ‘Java Garbage Collection’ 🌟](https://dzone.com/articles/revisiting-the-advanced-theories-of-java-garbage-c)
- [DZone: Understanding the Java Memory Model and Garbage Collection 🌟](https://dzone.com/articles/understanding-the-java-memory-model-and-the-garbag) In this article we will try to understand the Java memory model and how garbage collection works. In this article I have used JDK8 Oracle Hot Spot 64 bit JVM. First let me depict the different memory areas available for Java processes.
- [DZone: Memory Leaks and Java Code](https://dzone.com/articles/memory-leak-andjava-code) When you aren't using objects, but they aren't touched by GC, a memory leak happens. Here are six ways memory leaks happen to look for and avoid.

## Java Tracing Tools. JDK Flight Recorder
- [Byteman](https://byteman.jboss.org/)
- [developers.redhat.com: Collect JDK Flight Recorder events at runtime with JMC Agent 🌟](https://developers.redhat.com/blog/2020/10/29/collect-jdk-flight-recorder-events-at-runtime-with-jmc-agent/)
- [developers.redhat.com: Checkpointing Java from outside of Java](https://developers.redhat.com/blog/2020/10/15/checkpointing-java-from-outside-of-java/)
- [developers.redhat.com: A faster way to access JDK Flight Recorder data](https://developers.redhat.com/articles/2021/11/23/faster-way-access-jdk-flight-recorder-data)

## Cambios importantes en la gestión de memoria de Java 8 de Oracle (2014)

PermGen no pertenece al heap y los objetos no son promocionados a esta sección de memoria gestionada durante un GC. Como bien dices es un espacio contiguo al heap, pero también se limpia cada vez que la tenured/old generation procede a un GC. No es una generación separada del mismo modo que es la young generation, y no hay un mecanismo específico para un GC separado de PermGen. La tenured/old generation y la permanent generation proceden a un GC cuando una de las dos se llena.

De todos modos no me queda claro si incorporaron PermGen dentro del heap en Java 7, aunque poco importa ya con los cambios en Java 8.

Mejor empiezo por introducir qué implementación de JVM es Java 8 de Oracle. Existen numerosas implementaciones de JVM y cada una utiliza diferentes soluciones para la gestión de memoria.

Dos de las soluciones más conocidas y populares de JVM han sido HotSpot de Sun (habitual en Tomcat) y JRockit de BEA (Weblogic). Ambas compañias fueron compradas por Oracle y Java 8 viene a ser la integración definitiva de ambas soluciones.

Históricamente se consideraba que HotSpot es el JVM con mejor rendimiento de las dos, si bien JRockit es valorada como la más escalable.

Originalmente en HotSpot no había generación permanente. Objetos y clases de JVM se almacenaban juntas. Las clases de ésta JVM eran estáticas y prácticamente no se utilizaban 'Class Loaders' (Load y Unload/Collection de Clases). PermGen surgió como una mejora de rendimiento. Por defecto los datos en la generación permanente no se eliminan nunca (son datos de JVM y no de aplicación, pudiendo variar según la pólítica de garbage collection). Esto podía llenar la generación permanente generando un OutOfMemoryErrors si se producía un elevado número de classloading. En muchos casos un problema con una generación permanente implica reiniciar regularmente la JVM y la aplicación Java.

Actualmente las clases de JVM son dinámicas y el espacio requerido para metadatos puede cambiar fácilmente.

A diferencia de HotSpot VM, JRockit carece de generación permanente y en cambio almacena los metadatos 'off the heap' en memoria nativa. Estos buffers de código son liberados constantemente cuando sus ClassLoaders no se utilizan. El problema de OutOfMemory en JRockit no es diferente a HotSpot, excepto por el hecho de ser memoria nativa en lugar de memoria heap. Hay dos diferencias significativas. Primero, en JRockit la limpieza de metadatos está habilitada siempre por defecto y segundo, no hay tamaño límite fijo para el espacio de metadatos. Uno de los principales problemas con HotSpot es su dificultad para seleccionar un tamaño adecuado para la generación permanente. ¿128MB, 256MB? Es muy difícil acertar para cada aplicación. JRockit es dinámico en la gestión de memoria reservada para metadatos y sin límites de tamaño (a excepción de la memoria del sistema). JRockit es también el único JVM con soporte de heaps no contiguos (uso de memoria por encima y por debajo del alojamiento del kernel y otras librerías), importante en el caso de Windows donde su kernel a menudo se ubica en mitad del espacio de direcciones.

Java 8 (HotRockit?) incorpora todas las herramientas de monitorización de HotSpot (Java VisualVM, jstat, jmap) y JRockit (Java Mission Control, Java Flight Recorder). Muy interesante.

Un inconveniente de Java 8 es la fragmentación de la memoria nativa para metadatos, pero probablemente incluya compactación en un futuro próximo.

En el 2016 saldrá Java 9 con la funcionalidad de auto-tuning y soporte de tamaños Heap multi-gigas.

En cualquier caso hay una tendencia al Heap-Offloading. El consumo de memoria en Java tiene un coste y las pausas/latencias causadas por los Full GC son proporcionales al tamaño del heap. Estas pausas son notables en tamaños de heap > 1Gb, con un considerable impacto en aplicaciones de tiempo real donde un proceso que no responde rápido puede ser descartado del cluster. Aún así, los servidores actuales hacen uso de frameworks muy pesados y fácilmente requieren heaps > 4Gb. Una solución a este problema es alojar fuera del heap los objetos poco utilizados mediante técnicas de serialización/deserialización (caché). El heap de memoria se mantiene pequeño y el Full GC se completa en milisegundos. Ejemplos:

1. caché de sesión de usuarios, donde un fichero mapeado en memoria almacena gigabytes de sesiones de usuarios inactivos. Una vez que el usuario hace log-in, la aplicación dispone de todos sus datos sin ser necesaria una consulta a la BBDD. 
2. caché de resultados computacionales como queries, páginas html, etc (donde el coste computacional es mayor a la deserialización)

## Slides
<details>
  <summary>Click to expand!</summary>

<center>
<div class="container">
<iframe src="//www.slideshare.net/slideshow/embed_code/key/NpUYrnBQ59fyV6" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen class="video"> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/feuteston/jvm-internals-2015corkdevio" title="JVM Internals (2015)" target="_blank">JVM Internals (2015)</a> </strong> from <strong><a href="//www.slideshare.net/feuteston" target="_blank">Luiz Fernando Teston</a></strong> </div>
</div>
</center>
</details>

## Tweets
<details>
  <summary>Click to expand!</summary>

<center>
<blockquote class="twitter-tweet"><p lang="und" dir="ltr"><a href="https://twitter.com/hashtag/Java?src=hash&amp;ref_src=twsrc%5Etfw">#Java</a> on <a href="https://twitter.com/hashtag/Kubernetes?src=hash&amp;ref_src=twsrc%5Etfw">#Kubernetes</a> <a href="https://t.co/MRP0RwJWaG">pic.twitter.com/MRP0RwJWaG</a></p>&mdash; Bruno Borges (@brunoborges) <a href="https://twitter.com/brunoborges/status/1449655747764056073?ref_src=twsrc%5Etfw">October 17, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Once, I spent 6 months of my adult life as a full time JVM tuner. I was hired to work on data processing pipelines but the job became being a JVM tuning machine.</p>&mdash; Jaana Dogan ヤナ ドガン (@rakyll) <a href="https://twitter.com/rakyll/status/1461509707479195650?ref_src=twsrc%5Etfw">November 19, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
</center>
</details>