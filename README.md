
[![Build Status](https://travis-ci.org/microservices-demo/microservices-demo.svg?branch=master)](https://travis-ci.org/microservices-demo/microservices-demo)

# Sock Shop : A Microservice Demo Application

The application is the user-facing part of an online shop that sells socks. It is intended to aid the demonstration and testing of microservice and cloud native technologies.

It is built using [Spring Boot](http://projects.spring.io/spring-boot/), [Go kit](http://gokit.io) and [Node.js](https://nodejs.org/) and is packaged in Docker containers.

You can read more about the [application design](./internal-docs/design.md).

## Deployment Platforms

The [deploy folder](./deploy/) contains scripts and instructions to provision the application onto your favourite platform. 

Please let us know if there is a platform that you would like to see supported.

## Bugs, Feature Requests and Contributing

We'd love to see community contributions. We like to keep it simple and use Github issues to track bugs and feature requests and pull requests to manage contributions. See the [contribution information](.github/CONTRIBUTING.md) for more information.

## Screenshot

![Sock Shop frontend](https://github.com/microservices-demo/microservices-demo.github.io/raw/master/assets/sockshop-frontend.png)

## Visualizing the application

Use [Weave Scope](http://weave.works/products/weave-scope/) or [Weave Cloud](http://cloud.weave.works/) to visualize the application once it's running in the selected [target platform](./deploy/).

![Sock Shop in Weave Scope](https://github.com/microservices-demo/microservices-demo.github.io/raw/master/assets/sockshop-scope.png)

## 
## Production and Security Best Practices
1. Pinned tag version for each container image
2. liveness probe for each container.
3. Readiness probe for each container.
4. Resource probe for each container
5. Resource requests for each container
6. Do not expose a Node prot.
7. Use labels for all resources
8. Uisng Namespaces to isolate resources.
## Step by Step Overview
1. Create a K8s cluster with EKS
2. Deploy Microservices app
3. Deploy prometheus monitoring stack
4. Monitor Cluster Nodes
5. Monitor K8s Components
6. Monitor 3rd party Applications
7. Monitor own Applications.

### Monitoring on different levels
- Infrastructure Level (CPU, RAM, Network etc)
- Platform Level (Kubernetes Components)
- Application Level (3rd-Party Applications)
