# Istio - Service Mesh
- [Docs](#docs)
- [API Access Control](#api-access-control)
- [Maistra Istio](#maistra-istio)
- [Admiral](#admiral)
- [Kiali project, observability for the Istio service mesh](#kiali-project-observability-for-the-istio-service-mesh)
- [Jaeger tracing. Open source, end-to-end distributed tracing](#jaeger-tracing-open-source-end-to-end-distributed-tracing)
- [Envoy micro proxy](#envoy-micro-proxy)
- [Kibana](#kibana)
- [AWS App Mesh](#aws-app-mesh)
- [Istio and AWS EKS](#istio-and-aws-eks)
- [Tweets](#tweets)

## Docs
- [Istio.io](https://istio.io/)
- [github.com: Istio](https://github.com/istio/istio)
- [blog.openshift.com: How to Explain Service Mesh in Plain English](https://blog.openshift.com/from-the-enterprisersproject-how-to-explain-service-mesh-in-plain-english/)
- [Red Hat Developer: Istio Service Mesh](https://developers.redhat.com/topics/service-mesh/)
- [karlstoney.com: Istio 503's with UC's and TCP Fun Times](https://karlstoney.com/2019/05/31/istio-503s-ucs-and-tcp-fun-times/)
- [medium.com/solo-io blog](https://medium.com/solo-io) Connecting the world’s applications with APIs and Service Mesh
- [medium.com/solo-io: Istio the Easy Way (Again!)](https://medium.com/solo-io/istio-the-easy-way-again-b0504347b7ce)
- [blog.christianposta.com: Istio as an Example of When Not to Do Microservices](https://blog.christianposta.com/microservices/istio-as-an-example-of-when-not-to-do-microservices/)
- [istiobyexample.dev 🌟](https://istiobyexample.dev/)
  - [istiobyexample.dev: Fault Injection](https://istiobyexample.dev/fault-injection/)
- [medium.com: Getting started with Istio](https://medium.com/swlh/getting-started-with-istio-524628c025)
- [blog.openshift.com: Red Hat OpenShift Service Mesh is now available: What you should know 🌟](https://blog.openshift.com/red-hat-openshift-service-mesh-is-now-available-what-you-should-know/)
- [magalix.com: Getting Started With Istio: Overview And Installation](https://www.magalix.com/blog/getting-started-with-istio-overview-and-installation)
- [The Istio project just consolidated its control plane services: Pilot, Citadel, Galley, and the sidecar injector, into a single binary, **Istiod**](https://istio.io/blog/2020/tradewinds-2020/#fewer-moving-parts)
- [magalix.com: Working with Istio: Track your services with Kiali](https://www.magalix.com/blog/working-with-istio-track-your-services-with-kiali)
- [banzaicloud.com: Istio telemetry V2 (Mixerless) deep dive](https://banzaicloud.com/blog/istio-mixerless-telemetry/)
- [medium.com: How to Manage Microservices on Kubernetes With Istio](https://medium.com/better-programming/how-to-manage-microservices-on-kubernetes-with-istio-c25e97a60a59) How to implement DevSecOps on microservices architecture with a service mesh
- [github.com/askmeegs/learn-istio 🌟](https://github.com/askmeegs/learn-istio)
- [banzaicloud.com: What's new in Istio 1.6, a quick walkthrough](https://banzaicloud.com/blog/istio-1.6/)
- [Riding the Tiger: Lessons Learned Implementing Istio 🌟](https://zwischenzugs.com/2020/05/05/riding-the-tiger-lessons-learned-implementing-istio/)
- [dev.to/aurelievache: Understanding Istio: part 1 – Istio Components](https://dev.to/aurelievache/understanding-istio-part-1-istio-components-4ik5)
  - [dev.to/aurelievache: Understanding Istio: part 9 – DestinationRule](https://dev.to/aurelievache/understanding-istio-part-9-destinationrule-1g7e)
  - [dev.to/aurelievache: Understanding Istio: part 16 – Observability / Metrics](https://dev.to/aurelievache/understanding-istio-part-16-observability-metrics-2m8p)
- [banzaicloud.com: Controlling egress traffic with Istio](https://banzaicloud.com/blog/istio-external-demo/)
- [banzaicloud.com: Istio ingress controller as an API gateway](https://banzaicloud.com/blog/backyards-api-gateway)
- [openshift.com: Monitoring Services like an SRE in OpenShift ServiceMesh Part 2: Collecting Standard Metrics 🌟](https://www.openshift.com/blog/monitoring-services-like-an-sre-in-openshift-servicemesh-part-2-collecting-standard-metrics-3)
- [istio.io: Learn Microservices using Kubernetes and Istio 🌟](https://istio.io/latest/docs/examples/microservices-istio/) step-by-step tutorial
- [thenewstack.io - Service Mesh: The Gateway to Cloud Migration](https://thenewstack.io/when-you-need-or-dont-need-service-mesh/)
- [thenewstack.io: Kubernetes, Microservices, and Istio  — A Great Fit!](https://thenewstack.io/kubernetes-microservices-istio%E2%80%8A-%E2%80%8Aa-great-fit/)
- [medium: Observability With Istio, Kiali, and Grafana in Kubernetes and Spring Boot 🌟](https://medium.com/swlh/observability-with-istio-kiali-and-grafana-in-kubernetes-and-spring-boot-743af225c24f)
- [solo.io: Learn how to rate limit requests in Istio 🌟](https://www.solo.io/blog/tutorial-rate-limiting-of-service-requests-in-istio-service-mesh)
- [solo.io: Identity Federation for Multi-Cluster Kubernetes and Service Mesh](https://www.solo.io/blog/identity-federation-for-multi-cluster-kubernetes-and-service-mesh/)
- [sysdig.com: How to monitor Istio, the Kubernetes service mesh](https://sysdig.com/blog/monitor-istio/)
- [tetrate.io: VM to container communications 101](https://www.tetrate.io/blog/vm-to-container-communications-101/) How can I use Istio Service Mesh to make VMs and containers talk to each other?
- [redhat-scholars: istio-tutorial 🌟](https://github.com/redhat-scholars/istio-tutorial) Polyglot microservices (Java, Node, .NET) + Istio on Kubernetes/OpenShift
- [medium: Introduction to Istio Traffic Management. Traffic Routing with Istio by Example 🌟](https://medium.com/swlh/introduction-to-istio-traffic-management-6b62c86f8cb4) 
- [loginradius.com: Istio Service Mesh: A Beginners Guide 🌟](https://www.loginradius.com/blog/async/istio-service-mesh/) This post will give a high-level introduction to Istio and its related concepts and terminologies.
- [dzone: The Kubernetes Service Mesh: A Brief Introduction to Istio 🌟](https://dzone.com/articles/the-kubernetes-service-mesh-a-brief-introduction-t) In this blog we explore what the Istio service mesh is, its architecture, when and where to use it, plus some criticisms of the platform.
- [blog.jetstack.io: Istio OIDC Authentication](https://blog.jetstack.io/blog/istio-oidc/) A service mesh is an architectural pattern that provides common network services as a feature of the infrastructure. This typically includes features such as service discovery and policy enforcement to control how services within the mesh can communicate with each other.
- [medium.com: Increasing observability on Istio: The new Kiali health configuration](https://medium.com/kialiproject/increasing-observability-on-istio-the-new-kiali-health-configuration-3c91852c1bfe)
- [dzone: Istio Service Mesh, the Step-by-Step Guide, Part 1: Theory 🌟](https://dzone.com/articles/metadata-management-in-big-data-systems-a-complete-1) In Part 1, we go over the concepts behind Istio and Service Mesh, such as their architecture, how they function, and more.
  - [dzone: Istio Service Mesh, the Step-by-Step Guide, Part 2: Tutorial 🌟](https://dzone.com/articles/istio-service-mesh-the-step-by-step-guide-part-2-t)
- [solo.io: The evolution of VM support in Istio 1.8 (with video)](https://www.solo.io/blog/the-evolution-of-vm-support-in-istio-1-8-with-video/)
- [jetstack.io: Securing Istio workloads with mTLS using cert-manager](https://www.jetstack.io/blog/cert-manager-istio-integration/)
- [thenewstack.io: Why Do You Need Istio When You Already Have Kubernetes? 🌟](https://thenewstack.io/why-do-you-need-istio-when-you-already-have-kubernetes)
- [medium: Managing Microservices With Istio Service Mesh in Kubernetes](https://medium.com/avmconsulting-blog/managing-microservices-with-istio-service-mesh-in-kubernetes-36e1fda81757)
- [thenewstack.io: Solo.io: Istio Is Winning the Service Mesh War](https://thenewstack.io/solo-io-istio-is-winning-the-service-mesh-war/)
- [dzone: vice Meshes: Why Istio? An Introduction](https://dzone.com/articles/why-istio-intro) There are 3 leading contenders in the cluster ecosystem for service mesh, all open source. We compare and discuss why Istio is the best choice in most scenarios.
- [tetrate.io: Why do you need Istio when you already have Kubernetes?](https://www.tetrate.io/blog/why-do-you-need-istio-when-you-already-have-kubernetes/)
- [learncloudnative.com: Attach multiple VirtualServices to Istio Gateway](https://learncloudnative.com/blog/2020-11-23-multiple-vs-gateway)
- [thenewstack.io: What Is Istio and Why Does Kubernetes Need it? 🌟](https://thenewstack.io/what-is-istio-and-why-does-kubernetes-need-it/)
- [youtube: Istio & Service Mesh - simply explained in 15 mins 🌟](https://www.youtube.com/watch?v=16fgzklcF7Y&ab_channel=TechWorldwithNana)
- [dev.to: A GitOps recipe for Progressive Delivery with Istio 🌟](https://dev.to/stefanprodan/a-gitops-recipe-for-progressive-delivery-2pa3) GitOps and Progressive Delivery featuring 
IstioMesh, PrometheusIO, Flux v2 & Flagger.
- [samos-it.com: Securing Redis with Istio TLS origination](https://samos-it.com/posts/securing-redis-istio-tls-origniation-termination.html) Istio is daunting and not all use cases are well documented. The public docs focus mostly on using the egress gateway for TLS orignation. The use case of using the sidecar for TLS origination with a database isn't documented well. This blog post hopes to solve that.
- [solo.io: Istio multi-cluster on Red Hat OpenShift with Gloo Mesh](https://www.solo.io/blog/istio-multi-cluster-on-red-hat-openshift-with-gloo-mesh/)
- [giffgaff.io: Using Istio with Nginx ingress](https://www.giffgaff.io/tech/using-istio-with-nginx-ingress)
- [solo.io: Ode to Istio 🌟](https://www.solo.io/blog/ode-to-istio/)
- [thenewstack.io: Istio 1.10 Improves Scalability and Revision Control](https://thenewstack.io/istio-1-10-improves-scalability-and-revision-control/)
- [istio.io: Configuring failover for external services](https://istio.io/latest/blog/2021/external-locality-failover/) Learn how to configure locality load balancing and failover for endpoints that are outside of your mesh.
- [medium: Automated canary deployments with Flagger and Istio](https://medium.com/google-cloud/automated-canary-deployments-with-flagger-and-istio-ac747827f9d1)
- [thenewstack.io: Multicluster Management with Kubernetes and Istio](https://thenewstack.io/multicluster-management-with-kubernetes-and-istio/)
- [piotrminkowski.com: Multicluster Traffic Mirroring with Istio and Kind](https://piotrminkowski.com/2021/07/12/multicluster-traffic-mirroring-with-istio-and-kind)
- [thenewstack.io: Securing Istio Workloads with Auth0](https://thenewstack.io/securing-istio-workloads-with-auth0/)
- [tetrate.io: Multicluster Management with Kubernetes and Istio 🌟](https://www.tetrate.io/blog/multicluster-management-with-kubernetes-and-istio/)
- [thenewstack.io: Why Do You Need Istio When You Already Have Kubernetes? 🌟](https://thenewstack.io/why-do-you-need-istio-when-you-already-have-kubernetes/)
- [solo.io: Upgrading Istio without Downtime](https://www.solo.io/blog/upgrading-istio-without-downtime/)
- [tetrate.io: Using Istio Service Mesh as API Gateway 🌟](https://www.tetrate.io/blog/istio-servicemesh-api-gateway/)
- [mirantis.com: Your App Deserves More than Kubernetes Ingress: Kubernetes Ingress vs. Istio Gateway [webinar]](https://www.mirantis.com/blog/your-app-deserves-more-than-kubernetes-ingress-kubernetes-ingress-vs-istio-gateway-webinar)
- [solo.io: Configuration as Data, GitOps, and Controllers: it’s not simple for multi-cluster](https://www.solo.io/blog/configuration-as-data-gitops-and-controllers-its-not-simple-for-multi-cluster/)
- [solo.io: Istio’s networking: An in-depth look at traffic and architecture 🌟](https://www.solo.io/blog/istios-networking-in-depth) Istio’s networking in a demo environment

## API Access Control
- [medium: API Access Control using Istio Ingress Gateway](https://medium.com/@senthilrch/api-access-control-using-istio-ingress-gateway-44be659a087e)
- [medium: API Authentication using Istio Ingress Gateway, OAuth2-Proxy and Keycloak](https://medium.com/codex/api-authentication-using-istio-ingress-gateway-oauth2-proxy-and-keycloak-a980c996c259)

## Maistra Istio
- [Maistra.io](https://maistra.io)
- [github.com: Maistra Istio](https://github.com/maistra/istio)
- [Installing on OKD/OCP](https://maistra.io/docs/getting_started/install/)

## Admiral
- [istio-ecosystem/admiral](https://github.com/istio-ecosystem/admiral) Admiral provides automatic configuration and service discovery for multicluster Istio service mesh. Istio has a very robust set of multi-cluster capabilities. Managing this configuration across multiple clusters at scale is challenging. Admiral takes an opinionated view on this configuration and provides automatic provisioning and syncing across clusters. This removes the complexity for developers and mesh operators.

## Kiali project, observability for the Istio service mesh
- [kiali.io](https://www.kiali.io/)
- [github.com: kiali](https://github.com/kiali/kiali)
- [medium.com: kiali project](https://medium.com/kialiproject)
- [itnext.io: Find issues in your Istio mesh with Kiali](https://itnext.io/find-issues-in-your-istio-mesh-with-kiali-89d37d5e1fb1)
- [dzone: Deployment Monitoring Tools — Kiali](https://dzone.com/articles/kubernetes-deployment-monitoring-tools-kiali) A description of common issues with deployment monitoring, and a features list of Kiali and how to use it.

## Jaeger tracing. Open source, end-to-end distributed tracing
- Monitor and troubleshoot transactions in complex distributed systems
- [jaegertracing.io](https://www.jaegertracing.io/)
- [hackernoon.com: A Guide to Deploying Jaeger on Kubernetes in Production](https://hackernoon.com/a-guide-to-deploying-jaeger-on-kubernetes-in-production-0p2n3tub)
- [hackernoon.com: How To Use OpenTelemetry And Jaeger To Implement Distributed Tracing And APM](https://hackernoon.com/how-to-use-opentelemetry-and-jaeger-to-implement-distributed-tracing-and-apm-jcx34fi)

## Envoy micro proxy
- [envoyproxy.io](https://www.envoyproxy.io/)
- [getenvoy.io](https://www.getenvoy.io/)
- [Controlling outbound traffic from Kubernetes](https://monzo.com/blog/controlling-outbound-traffic-from-kubernetes)
- [medium: Troubleshooting Envoy with Kiali](https://medium.com/kialiproject/troubleshooting-envoy-with-kiali-7f78a57b16ad) Inspect and debug your Envoy configuration

## Kibana
- [kibana](https://www.elastic.co/products/kibana)
- [The Best Tools for Exporting Elasticsearch Data from Kibana](https://www.skedler.com/blog/the-best-tools-for-exporting-elasticsearch-data-from-kibana/)

## AWS App Mesh
- [aws.amazon.com/app-mesh](https://aws.amazon.com/app-mesh/)
- [allthingsdistributed.com: Redefining application communications with AWS App Mesh](https://www.allthingsdistributed.com/2019/03/redefining-application-communications-with-aws-app-mesh.html)

## Istio and AWS EKS
- [itnext.io: Observing gRPC-based Microservices on Amazon EKS running Istio](https://itnext.io/observing-grpc-based-microservices-on-amazon-eks-running-istio-77ba90dd8cc0) Observing a gRPC-based Kubernetes application using Jaeger, Zipkin, Prometheus, Grafana, and Kiali on Amazon EKS running Istio service mesh

## Tweets
<details>
  <summary>Click to expand!</summary>

<center>
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">💎 Hidden gem feature<br><br>Did you know that Kiali can automatically generate all the Authorization Policies of a namespace?<br><br>Via telemetry, Kiali can define one Authz Policy per each service in the mesh.<a href="https://twitter.com/IstioMesh?ref_src=twsrc%5Etfw">@IstioMesh</a> <a href="https://twitter.com/hashtag/servicemesh?src=hash&amp;ref_src=twsrc%5Etfw">#servicemesh</a> <a href="https://twitter.com/hashtag/authorization?src=hash&amp;ref_src=twsrc%5Etfw">#authorization</a> <a href="https://twitter.com/hashtag/security?src=hash&amp;ref_src=twsrc%5Etfw">#security</a> <a href="https://twitter.com/hashtag/k8s?src=hash&amp;ref_src=twsrc%5Etfw">#k8s</a> <a href="https://t.co/YlEKRq6nq0">pic.twitter.com/YlEKRq6nq0</a></p>&mdash; Kiali (@KialiProject) <a href="https://twitter.com/KialiProject/status/1393940551637127168?ref_src=twsrc%5Etfw">May 16, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
</center>
</details>