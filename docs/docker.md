# Docker
- [Introduction and Tutorials](#introduction-and-tutorials)
- [Docker Swarm](#docker-swarm)
- [Awesome Lists](#awesome-lists)
- [Docker VS Kubernetes](#docker-vs-kubernetes)
- [Docker Patterns and Antipatterns](#docker-patterns-and-antipatterns)
- [Security](#security)
- [How To Build a Smaller Docker Image](#how-to-build-a-smaller-docker-image)
- [Reducing Build Time](#reducing-build-time)
- [Modify containers without rebuilding](#modify-containers-without-rebuilding)
- [Docker Tools](#docker-tools)
- [Docker and WSL2](#docker-and-wsl2)
- [Docker and Docker Swarm Cheat sheets](#docker-and-docker-swarm-cheat-sheets)
- [Docker Compose](#docker-compose)
- [Moving Linux Services Into Containers](#moving-linux-services-into-containers)
- [Windows Containers](#windows-containers)
- [Portainer](#portainer)
- [DockStation](#dockstation)
- [Linux Container Base Images](#linux-container-base-images)
- [Blogs](#blogs)
- [Cloud Native Buildpacks](#cloud-native-buildpacks)
- [Alternatives to Docker. Available alternatives to Docker for OCI compliant container image building](#alternatives-to-docker-available-alternatives-to-docker-for-oci-compliant-container-image-building)
- [Videos and Podcasts](#videos-and-podcasts)
- [Tweets](#tweets)

## Introduction and Tutorials
* [Wikipedia.org: Docker](https://en.wikipedia.org/wiki/Docker_(software))
* [Dzone refcard: Getting Started with Docker](https://dzone.com/refcardz/getting-started-with-docker-1)
* [Dzone refcard: Java Containerization 🌟](https://dzone.com/refcardz/java-containerization)
* [americanexpress.io: **Do Not Run Dockerized Applications as Root** 🌟](https://americanexpress.io/do-not-run-dockerized-applications-as-root/)
* [medium.com: Removing Docker Images, Containers, and Volumes with Ease](https://medium.com/@jon.froiland/removing-docker-images-containers-and-volumes-with-ease-fdf16bebccec)
* [medium.freecodecamp.com: A Beginner-Friendly Introduction to Containers, VMs and Docker](https://medium.freecodecamp.com/a-beginner-friendly-introduction-to-containers-vms-and-docker-79a9e3e119b)
* [Google Play: Learning Solution - Learn Docker 🌟](https://play.google.com/store/apps/details?id=com.LearningSolution.LearnDocker&hl=en)
* [Play with docker 🌟](https://labs.play-with-docker.com/) A simple, interactive and fun playground to learn Docker
* [blog.docker.com: Intro Guide to Dockerfile Best Practices 🌟](https://blog.docker.com/2019/07/intro-guide-to-dockerfile-best-practices/)
* [medium: Strategies of docker images optimization](https://medium.com/sciforce/strategies-of-docker-images-optimization-2ca9cc5719b6)
* [Dzone: Docker explained, an introductory guide to docker](https://dzone.com/articles/docker-explained-an-introductory-guide-to-docker)
* [Dzone: everything you need to know about docker](https://dzone.com/articles/everything-you-need-to-know-about-docker)
* [Dzone: a start to finish guide to docker with java](https://dzone.com/articles/a-start-to-finish-guide-to-docker-with-java)
* [docker.com: Intro Guide to Dockerfile Best Practices](https://www.docker.com/blog/intro-guide-to-dockerfile-best-practices/)
* [**GitHub build-push-action**](https://github.com/docker/build-push-action) Build+push official Docker GitHub action
* [docker.com: Speed Up Your Development Flow With These Dockerfile Best Practices](https://www.docker.com/blog/speed-up-your-development-flow-with-these-dockerfile-best-practices/)
* [itnext.io: Getting Started with Docker: Facts You Should Know 🌟](https://itnext.io/getting-started-with-docker-facts-you-should-know-d000e5815598)
* [jfrog.com: A Beginner’s Guide to Understanding and Building Docker Images 🌟](https://jfrog.com/knowledge-base/a-beginners-guide-to-understanding-and-building-docker-images/)
* [Broken by default: why you should avoid most Dockerfile example 🌟](https://pythonspeed.com/articles/dockerizing-python-is-hard/)
* [geekflare.com: docker tutorials](https://geekflare.com/docker-tutorials/)
* [medium: What is Docker, Why should you use it in simple words](https://medium.com/@shahinghasemy/what-is-docker-why-should-you-use-it-in-simple-words-cc5e6160f9db)
* [docker.com: Top Questions for Getting Started with Docker 🌟](https://www.docker.com/blog/top-questions-for-getting-started-with-docker/)
* [medium: How to Start Working With Docker Containers](https://medium.com/swlh/how-to-start-working-with-docker-containers-72b73ca60e0c)
* [dzone: Mitigating DevOps Repository Risks](https://dzone.com/articles/mitigating-devops-repository-risks) Docker is in the news for two reasons: Image retention limits and download throttling. Let's discuss both and see the better alternatives.
* [Top 18 Docker commands for Automation Tester/Devops/SDET/Test Lead? 🌟](https://automationreinvented.blogspot.com/2020/02/top-18-docker-commands-for-aytomation.html)
* [A Gentle Introduction to Using a Docker Container as a Dev Environment 🌟](https://css-tricks.com/a-gentle-introduction-to-using-a-docker-container-as-a-dev-environment/)
* [docs.docker.com: Deploying Docker containers on ECS](https://docs.docker.com/engine/context/ecs-integration/)
    * [AWS and Docker collaborate to simplify the developer experience](https://aws.amazon.com/blogs/containers/aws-docker-collaborate-simplify-developer-experience/)
    * [From Docker Straight to AWS](https://www.docker.com/blog/from-docker-straight-to-aws/)
* [medium: Understanding Docker Volumes, Mounts and Layers and How to Manage Data in Containers](https://medium.com/nycdev/understanding-docker-volumes-mounts-and-layers-9fa17befa493)
* [A Gentle Introduction to Using a Docker Container as a Dev Environment](https://css-tricks.com/a-gentle-introduction-to-using-a-docker-container-as-a-dev-environment/)
* [martinheinz.dev: It's Time to Forget About Docker 🌟](https://martinheinz.dev/blog/35)
* [docker.com: Docker Hub Experimental CLI tool](https://www.docker.com/blog/docker-hub-experimental-cli-tool/)
* [docker.com: Year in Review: The Most Viewed Docker Blog Posts of 2020 Part 1 🌟](https://www.docker.com/blog/year-in-review-the-most-viewed-docker-blog-posts-of-2020-part-1/)
* [docker.com: Year in Review: The Most Viewed Docker Blog Posts of 2020 Part 2 🌟](https://www.docker.com/blog/year-in-review-the-most-viewed-docker-blog-posts-of-2020-part-2/)
* [adictosaltrabajo.com: Cómo crear y desplegar microservicios con Spring Boot, Spring Cloud Netflix y Docker](https://www.adictosaltrabajo.com/2020/12/22/como-crear-y-desplegar-microservicios-con-spring-boot-spring-cloud-netflix-y-docker/)
* [cloudsavvyit.com: How to Use Cron With Your Docker Containers](https://www.cloudsavvyit.com/9033/how-to-use-cron-with-your-docker-containers/)
* [infoq.com: Docker Hub and JFrog Partnership Removes Image Pull Limits for Artifactory Users](https://www.infoq.com/news/2021/01/docker-jfrog-partnership/) 
* [technology.doximity.com: Buildpacks vs Dockerfiles 🌟](https://technology.doximity.com/articles/buildpacks-vs-dockerfiles) Exploring the tradeoffs of building container images at scale
* [docker.com: Containerized Python Development – Part 1](https://www.docker.com/blog/containerized-python-development-part-1/)
    * [docker.com: Containerized Python Development – Part 2](https://www.docker.com/blog/containerized-python-development-part-2/)
    * [docker.com: Containerized Python Development – Part 3](https://www.docker.com/blog/containerized-python-development-part-3/)
* [sysdig.com: Top 20 Dockerfile best practices 🌟](https://sysdig.com/blog/dockerfile-best-practices/)
* [pythonspeed.com: The worst so-called “best practice” for Docker](https://pythonspeed.com/articles/security-updates-in-docker/)
* [developers.redhat.com: Making environment variables accessible in front-end containers](https://developers.redhat.com/blog/2021/03/04/making-environment-variables-accessible-in-front-end-containers/)
* [towardsdatascience.com: Have you heard about our lord and savior Docker?](https://towardsdatascience.com/docker-101-ee3d2b8ace11) Introduction to working with Docker and creating your own development environment
* [medium: Dockerizing a REST API in Python Less Than 9 MB and Based on scratch Image](https://medium.com/analytics-vidhya/dockerizing-a-rest-api-in-python-less-than-9-mb-and-based-on-scratch-image-ef0ee3ad3f0a)
* [datamechanics.co: Optimized Apache Spark Docker Images](https://www.datamechanics.co/blog-post/optimized-spark-docker-images-now-available)
* [theskillpedia.com: Managing docker images - openshift tutorial](https://www.theskillpedia.com/managing-docker-images-openshift-tutorial/)
* [iximiuz.com: Container Networking Is Simple!](https://iximiuz.com/en/posts/container-networking-is-simple/)
* [r-bloggers.com: Dockerizing Shiny Applications](https://www.r-bloggers.com/2021/05/dockerizing-shiny-applications/)
* [pythonspeed.com: Docker can slow down your code and distort your benchmarks](https://pythonspeed.com/articles/docker-performance-overhead/)
* [turbofuture.com: A Beginners Guide to Containers and Docker](https://turbofuture.com/computers/introductiontodocker)
* [releasehub.com: Cutting Build Time In Half with Docker’s Buildx Kubernetes Driver](https://releasehub.com/blog/cutting-build-time-in-half-docker-buildx-kubernetes)
* [linuxadictos.com: Docker presenta nuevas capacidades para desarrolladores](https://www.linuxadictos.com/docker-presenta-nuevas-capacidades-para-desarrolladores.html)
* [grafana.com: Docker Integration for Grafana Cloud](https://grafana.com/docs/grafana-cloud/reference/integrations/integration-docker/) Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly.
* [dev.to: Docker CMD vs ENTRYPOINT: explaining the difference](https://dev.to/hood/docker-cmd-vs-entrypoint-explaining-the-difference-55g7)
* [blog.gougousis.net: File Permissions: the painful side of Docker 🌟](https://blog.gougousis.net/file-permissions-the-painful-side-of-docker/)
    * ["Excellent description of user ids and access rights in Docker; it’s a non trivial issue and there’s no silver bullet other than to avoid running your containers with a privileged user. As a bonus, I personally like openshift approach (random UIDs belonging to the super user GID)"](https://twitter.com/agarcia)
* [katacoda.com: Learn Docker & Containers using Interactive Browser-Based Scenarios 🌟](https://www.katacoda.com/courses/docker)
* [medium: Push Docker Image To Docker Hub](https://medium.com/codex/push-docker-image-to-docker-hub-acc978c76ad) Create Docker hub account and push Docker image.
* [blog.thundra.io: Why Should You Run All Your Tests in Docker? 🌟](https://blog.thundra.io/why-should-you-run-all-your-tests-in-docker)
* [returngis.net: Crea hosts de Docker con Docker Machine en Microsoft Azure](https://www.returngis.net/2021/08/crea-hosts-de-docker-con-docker-machine-en-microsoft-azure/) 
* [dev.to: Docker 101!](https://dev.to/kubona_my/docker-101-124e)
* [pawelurbanek.com: asdf and Docker for Managing Local Development Dependencies](https://pawelurbanek.com/asdf-docker-development)
* [tecmint.com: How to Install Docker on Rocky Linux and AlmaLinux](https://www.tecmint.com/install-docker-in-rocky-linux-and-almalinux/)
* [blog.adoptium.net: Using Jlink in Dockerfiles instead of a JRE](https://blog.adoptium.net/2021/08/using-jlink-in-dockerfiles/)
* [cloudsavvyit.com: How to SSH into a Docker container](https://www.cloudsavvyit.com/13937/how-to-ssh-into-a-docker-container/)
* [cloudsavvyit.com: How to use docker cp to copy files between host and containers](https://www.cloudsavvyit.com/13987/how-to-use-docker-cp-to-copy-files-between-host-and-containers/)
* [baeldung.com: Deploying a Java War in a Docker Container](https://www.baeldung.com/docker-deploy-java-war)
* [returngis.net: Explorar gráficamente el contenido de un volumen de Docker](https://www.returngis.net/2021/08/explorar-graficamente-el-contenido-de-un-volumen-de-docker/)
* [opensource.com: What is a container image?](https://opensource.com/article/21/8/container-image) A container image contains a packaged application, along with its dependencies, and information on what processes it runs when launched. 
* [zdnet.com: Docker changes its subscription plans, usage rules, and product line](https://www.zdnet.com/article/docker-changes-its-subscription-plans-usage-rules-and-product-line/)
* [servethehome.com: Docker Abruptly Starts Charging Many Users for Docker Desktop](https://www.servethehome.com/docker-abruptly-starts-charging-many-users-for-docker-desktop/)
* [matt-rickard.com: An Overview of Docker Desktop Alternatives](https://matt-rickard.com/docker-desktop-alternatives/)
* [blog.aquasec.com: How Do Containers Contain? Container Isolation Techniques](https://blog.aquasec.com/container-isolation-techniques)
* [infoworld.com: How Docker broke in half](https://www.infoworld.com/article/3632142/how-docker-broke-in-half.html) The game changing container company is a shell of its former self. What happened to one of the hottest enterprise technology businesses of the cloud era?
* [cloudsavvyit.com: How to Pass Environment Variables to Docker Containers](https://www.cloudsavvyit.com/14081/how-to-pass-environment-variables-to-docker-containers/)
* [dev.to: One does not "just containerize" an app](https://dev.to/tylerlwsmith/one-does-not-just-containerize-an-app-5eae)
    * The Docker ecosystem is filled with leaky abstractions. The utopian vision of Docker containers is a world where a developer can grab a base container for a language, copy in their code with a minimal Dockerfile, and be ready to develop and deploy instantly.
    * Unfortunately, this landscape is filled with per-language gotchas that make this world a far cry from reality. Here are some of the wonky things I've run into when working with containers.
* [cloudsavvyit.com: How To Clean Up and Delete Docker Images](https://www.cloudsavvyit.com/14191/how-to-clean-up-and-delete-docker-images/)
* [==itnext.io: Software development in containers — a cookbook== 🌟🌟🌟](https://itnext.io/software-development-in-containers-a-cookbook-2ba14d07e535) A guide to developing containerized software
* [dev.to: How to create a production Docker image](https://dev.to/abdorah/how-to-create-production-docker-image-ready-for-deployment-4bbe)
* [dev.to: How to run docker on Windows without Docker Desktop](https://dev.to/_nicolas_louis_/how-to-run-docker-on-windows-without-docker-desktop-hik)
* [dev.to: Beginner's guide to Docker and Docker CLI commands](https://dev.to/paru429/beginner-s-guide-to-docker-and-docker-cli-commands-1p75)
* [testdriven.io: Docker Best Practices for Python Developers](https://testdriven.io/blog/docker-best-practices/)
* [freecodecamp.org: Learn How to Deploy 12 Apps to AWS, Azure, & Google Cloud](https://www.freecodecamp.org/news/learn-how-to-deploy-12-apps-to-aws-azure-google-cloud/)
* [cloudsavvyit.com: How to Assign a Static IP to a Docker Container](https://www.cloudsavvyit.com/14508/how-to-assign-a-static-ip-to-a-docker-container/)
* [cloudsavvyit.com: How to Inspect a Docker Image’s Content Without Starting a Container](https://www.cloudsavvyit.com/14663/how-to-inspect-a-docker-images-content-without-starting-a-container/)
* [freecodecamp.org: Why You Should Start Using Docker Right Now](https://www.freecodecamp.org/news/why-you-should-start-using-docker-now/)
* [infoworld.com: Docker really did change the world](https://www.infoworld.com/article/3639596/docker-really-did-change-the-world.html) Developers quickly understood the value of containers for building cloud-native applications, and that the Docker command-line tool was better than all of the bells and whistles they got with PaaS.
* [==dev.to: Top 8 Docker Best Practices for using Docker in Production== 🌟](https://dev.to/techworld_with_nana/top-8-docker-best-practices-for-using-docker-in-production-1m39)
* [cloudsavvyit.com: How (and Why) to Run Docker Inside Docker](https://www.cloudsavvyit.com/14890/how-and-why-to-run-docker-inside-docker/)

## Docker Swarm
- [linkedin.com: Docker Series : Docker Swarm - Lionel GURRET](https://www.linkedin.com/pulse/docker-series-swarm-lionel-gurret/)
- [cloudsavvyit.com: What is Docker Swarm Mode and When Should You Use It?](https://www.cloudsavvyit.com/13049/what-is-docker-swarm-mode-and-when-should-you-use-it/)

## Awesome Lists
* [Awesome Docker 🌟](https://github.com/veggiemonk/awesome-docker)
* [Awesome Compose 🌟](https://github.com/docker/awesome-compose)

## Docker VS Kubernetes
- [blog.testproject.io: A Comparison of Kubernetes and Docker](https://blog.testproject.io/2021/06/21/a-comparison-of-kubernetes-and-docker/)

## Docker Patterns and Antipatterns
- [codefresh.io: Docker anti-patterns 🌟](https://codefresh.io/containers/docker-anti-patterns/)

## Security
- [thehackernews.com: Docker Images Containing Cryptojacking Malware Distributed via Docker Hub](https://thehackernews.com/2020/06/cryptocurrency-docker-image.html)
- [acloudguru.com: 10 Docker Security Best Practices to Cut Container Chaos](https://acloudguru.com/blog/engineering/10-docker-security-best-practices-to-cut-container-chaos)
- [brianchristner.io: How to use Docker Security Scan Locally](https://brianchristner.io/how-to-use-docker-scan/) Docker included a new command called `docker scan` that scans local images against the Snyk security engine, providing you with security visibility into your local Dockerfiles and images.
- [snyk.io: 10 Docker Security Best Practices 🌟](https://snyk.io/blog/10-docker-image-security-best-practices/)
- [cheatsheetseries.owasp.org: Docker Security Cheat Sheet 🌟🌟](https://cheatsheetseries.owasp.org/cheatsheets/Docker_Security_Cheat_Sheet.html)
  
## How To Build a Smaller Docker Image
* [developers.redhat.com: Keep it small: a closer look at Docker image sizing](https://developers.redhat.com/blog/2016/03/09/more-about-docker-images-size/)
* [medium: How to build a smaller Docker image](https://medium.com/@gdiener/how-to-build-a-smaller-docker-image-76779e18d48a) When you’re building a Docker image it’s important to keep the size under control. Having small images means ensuring faster deployment and transfers.
* [itsopensource.com: How to Reduce Node Docker Image Size by 10X](https://itsopensource.com/how-to-reduce-node-docker-image-size-by-ten-times/)
* [blog.bitsrc.io: Best Practices for Writing a Dockerfile](https://blog.bitsrc.io/best-practices-for-writing-a-dockerfile-68893706c3) Optimize your Docker Image by following these best practices from day one.
* [sequoia.makes.software: Reducing Docker Image Size (Particularly for Kubernetes Environments) 🌟](https://sequoia.makes.software/reducing-docker-image-size-particularly-for-kubernetes-environments/)
* [itnext.io: Building Docker Images The Proper Way 🌟](https://itnext.io/building-docker-images-the-proper-way-3c9807524582) Let’s optimize Docker builds to create much smaller and more secure Docker images in a fraction of the usual build time…
* [returngis.net: Reduce el tamaño de tus imágenes con Dockerfiles multi-stage](https://www.returngis.net/2021/08/reduce-el-tamano-de-tus-imagenes-con-dockerfiles-multi-stage/)
* [slim.ai: Automatically reduce Docker container size using DockerSlim](https://www.slim.ai/blog/automatically-reduce-docker-container-size-using-dockerslim.html)
* [learnk8s.io: 3 simple tricks for smaller Docker images 🌟](https://learnk8s.io/blog/smaller-docker-images) When it comes to building Docker containers, you should always strive for smaller images. **Images that share layers and are smaller in size are quicker to transfer and deploy.**

## Reducing Build Time
* [nrmitchi.com: One Simple Trick for Building Images Faster 🌟](https://www.nrmitchi.com/2020/10/one-simple-trick-for-building-images-faster/?utm_sq=gkugwn5n5s)
    * ``BUILDKIT_INLINE_CACHE=1 build-arg`` is a neat flag that you could add to your docker build to reduce the build time upto 89%
* [pythonspeed.com: Docker BuildKit: faster builds, new features, and now it’s stable](https://pythonspeed.com/articles/docker-buildkit/) Building Docker images can be slow, and Docker’s build system is also missing some critical security features, in particular the ability to use build secrets without leaking them. So over the past few years the Docker developers have been working on a new backend for building images, BuildKit.

## Modify containers without rebuilding
* [cloudowski.com: How to modify containers without rebuilding their image](https://cloudowski.com/articles/how-to-modify-containers-wihtout-rebuilding/)

## Docker Tools
- [Top 50 Docker Tools](https://blog.inedo.com/top-50-docker-tools)
- [docker-ecs-plugin: Docker Releases Plugin for Simplified Deployments into AWS ECS and Fargate](https://www.infoq.com/news/2020/07/docker-ecs-plugin/)
- [dive 🌟](https://github.com/wagoodman/dive) A tool for exploring a docker image, layer contents, and discovering ways to shrink the size of your Docker/OCI image. Use the dive tool to analyze a Docker image of your application. What did I learn? While Jib creates 3 layers for Spring Boot app (dependencies, resources and classes), Paketo Buildpacks places resources and classes in the same layer.
- [ctop 🌟](https://github.com/bcicen/ctop) Top-like interface for container metrics
- [phpdocker](https://github.com/sherifabdlnaby/phpdocker) Production Grade, Rootless, Pre-configured, Extendable, and Multistage
PHP Docker Image for Cloud Native Deployments (and Kubernetes)
- [dev.to: Use Kool to Dockerize Your Local Development Environment the Right Way](https://dev.to/kooldev/use-kool-to-dockerize-your-local-development-environment-the-right-way-18gl)
- [sematext: Monitor Docker Metrics & Logs 🌟](https://sematext.com/docker/) Full Docker observability: Docker metrics, logs, and events. Yes, Kubernetes & Swarm, too!
- [stepchowfun/docuum: Docuum: LRU eviction of Docker images 🌟](https://github.com/stepchowfun/docuum) Docuum performs least recently used (LRU) eviction of Docker images.
    - Docker's built-in docker image prune --all --filter until=… command serves a similar purpose. However, the built-in solution isn't ideal since it uses the image creation time, rather than the last usage time, to determine which images to remove. That means it can delete frequently used images, which may be expensive to rebuild.
    - **Docuum is ideal for use cases such as continuous integration (CI) workers, developer workstations, or any other environment in which Docker images accumulate on disk over time.** Docuum works well with tools like Toast and Docker Compose.
    - Docuum is used by Airbnb on its fleet of 1.5k+ CI workers.

## Docker and WSL2
- [Creating the best Linux Development experience on Windows & WSL 2](https://www.docker.com/blog/creating-the-best-linux-development-experience-on-windows-wsl-2/)
- [andrewlock.net: Installing Docker Desktop for Windows and WSL 2](https://andrewlock.net/installing-docker-desktop-for-windows/)

## Docker and Docker Swarm Cheat sheets
* [Docker and Docker Swarm Cheat Sheets](cheatsheets.md)

## Docker Compose
- [freecodecamp.org: a beginners guide to docker - how to create a client server side with docker compose](https://www.freecodecamp.org/news/a-beginners-guide-to-docker-how-to-create-a-client-server-side-with-docker-compose-12c8cf0ae0aa/)
* [docker.com: Announcing the Compose Specification 🌟](https://www.docker.com/blog/announcing-the-compose-specification/)
* [infoworld.com: Docker's Compose specification is now an open standard](https://www.infoworld.com/article/3536573/dockers-compose-specification-is-now-an-open-standard.html) Docker’s system for creating applications from multiple containers is now available on GitHub for all to contribute to.
* [theregister.co.uk: Compose yourselves – Docker has published multi-container app spec, needs contributors to help maintain and develop it](https://www.theregister.co.uk/2020/04/08/docker_opens_up_compose_specification/) Now focused on developers, firm wants its tools to be more universally useful. Keep it light(weight), though.
* [Awesome Compose](https://github.com/docker/awesome-compose)
* [Visual docker-compose.yml file generator 🌟](https://nuxx.io/)
* [medium: How can we easily and visually explain the Docker Compose 🌟](https://medium.com/clarusway/how-can-we-easily-and-visually-explain-the-docker-compose-53df77e9f046)
* [docker.com: Docker Compose for Amazon ECS Now Available](https://www.docker.com/blog/docker-compose-for-amazon-ecs-now-available/)

## Moving Linux Services Into Containers
* [crunchtools.com: A Hacker’s Guide to Moving Linux Services into Containers. Epic 15 page blog post showing people how to move Wordpress (php), Mediawiki (php), and Request Tracker (perl) into containers](http://crunchtools.com/moving-linux-services-to-containers/)

## Windows Containers
- [medium: Windows Containers (personal) cheat sheet](https://medium.com/@sebagomez/windows-containers-personal-cheat-sheet-95c1c4d6bdf5)

## Portainer
* [Portainer 🌟](https://www.portainer.io/) Making Docker management easy
* [Portainer Community Edition](https://www.portainer.io/products/community-edition)

## DockStation
- [dockstation.io](https://dockstation.io/)

## Linux Container Base Images
* [crunchtools.com: A Comparison of Linux Container Images](http://crunchtools.com/comparison-linux-container-images/)
* [kubedex.com: Base images comparison](https://kubedex.com/base-images/)
* [developers.redhat.com: Red Hat Universal Base Images for Docker users](https://developers.redhat.com/blog/2020/03/24/red-hat-universal-base-images-for-docker-users/)
    * [developers.redhat.com: book: Red Hat Universal Base Images (UBI)](https://developers.redhat.com/books/red-hat-universal-base-images-ubi)
* [dev.to: The best Docker base image for your Python application](https://dev.to/pmutua/the-best-docker-base-image-for-your-python-application-3o83)
* [Red Hat Universal Base Images - hub.docker.com/u/redhat: UBI 8 standard, minimal, micro, and init from DockerHub 🌟](https://hub.docker.com/u/redhat) 
* [developers.redhat.com: Red Hat Universal Base Image and Docker Hub: Why should developers care?](https://developers.redhat.com/articles/2021/05/25/red-hat-universal-base-image-and-docker-hub-why-should-developers-care)
* [redhat.com: Red Hat Brings Red Hat Universal Base Image to Docker Hub](https://www.redhat.com/en/about/press-releases/red-hat-brings-red-hat-universal-base-image-docker-hub) Verified content from the world’s leading enterprise Linux platform aimed at helping developers and operators build more secure and scalable containerized solutions from the industry’s leading container registry

## Blogs
- [Digital Ocean: Docker Tutorials](https://www.digitalocean.com/community/tags/docker)

## Cloud Native Buildpacks
- [buildpacks.io: Cloud Native Buildpacks 🌟](https://buildpacks.io/) transform your application source code into images that can run on any cloud.
- [altoros.com: Streamlining the Creation of Docker Images with Cloud Native Buildpacks](https://www.altoros.com/blog/streamlining-the-creation-of-docker-images-with-cloud-native-buildpacks/) The new Cloud Native Buildpacks framework changes the obnoxious development chore of Dockerfile writing into a simple, automated operations pipeline. When deploying apps to Kubernetes or other container-as-a-service platforms, the proliferation of nonstandard, unauditable containers built manually via Dockerfiles is a real problem. A few products have emerged to solve this problem, among them Cloud Native Buildpacks (СNB). In this blog post, we explore the capabilities of these buildpacks and explain how to use them in build pipelines to deliver standardized, auditable images as artifacts suitable for deployment.
- [thenewstack.io: Container Images the Easy Way with Cloud Native Buildpacks](https://thenewstack.io/container-images-the-easy-way-with-cloud-native-buildpacks/)

## Alternatives to Docker. Available alternatives to Docker for OCI compliant container image building
- [blog.alexellis.io: Building containers without Docker 🌟](https://blog.alexellis.io/building-containers-without-docker/)
- [medium: nerdctl: Docker-compatible CLI for contaiNERD](https://medium.com/nttlabs/nerdctl-359311b32d0e)
- [jfrog.com: THE BASICS: 7 Alternatives to Docker: All-in-One Solutions and Standalone Container Tools 🌟](https://jfrog.com/knowledge-base/the-basics-7-alternatives-to-docker-all-in-one-solutions-and-standalone-container-tools/)
- [nerdctl 🌟](https://github.com/containerd/nerdctl) Docker-compatible CLI for containerd
- [img](https://github.com/genuinetools/img)
- [jib](https://github.com/GoogleContainerTools/jib)
- [kaniko](https://github.com/GoogleContainerTools/kaniko)
- [buildah](https://buildah.io/)
- [buildkit](https://docs.docker.com/develop/develop-images/build_enhancements/)
- [podman](https://podman.io/)

## Videos and Podcasts
<details>
  <summary>Click to expand!</summary>

<center>
<iframe scrolling="no" frameborder="no" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/273312823&amp;color=ff5500"></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/n-JwAM6XF88" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/EnJ7qX9fkcU" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</center>
</details>

## Tweets
<details>
  <summary>Click to expand!</summary>

<center>
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Environment variables in Docker:<br><br>Environment variables are dynamic-named values that affect how our app will behave when running.<br><br>We can define them with Docker:<br>- at runtime<br>- in the Dockerfile<br>- in the Compose file (2 ways)<br><br>Let&#39;s see in detail in 1 minute:<br><br>1/5</p>&mdash; Francesco Ciulla (@FrancescoCiull4) <a href="https://twitter.com/FrancescoCiull4/status/1393448190729465856?ref_src=twsrc%5Etfw">May 15, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
</center>
</details>