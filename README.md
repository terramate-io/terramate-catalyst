# Terramate Catalyst

Access our early [Documentation of Terramate Catalyst](CATALYST.md).

> [!TIP]
> Terramate Catalyst is currently only available for design partners. If you are interested in joining our design partner programm, please [contact us].

## What is Terramate Catalyst?

Terramate Catalyst is a special distribution of Terramate CLI supporting all the same base features but adding powerful additional capabilities to make itt scalable for any size of teams.

The main goal is to enable self service by abstracting away all the details from the end user.

## Important personas and how we see them

We differentiate between two main groups of users in Terramate Catalyst.

- Platform Engineers - provide, maintain, and are responsible for infrastructure
- Application Engineers/Developers - require infrastructure and run-time environments to execute their applications/services

While platform engineers are infrastructure experts, and need to keep risk potential low and security high, application engineers shall not require to know about all the details but instead just require a new service to store data (e.g. databases, cloud storage) or send/receive events (e.g. queueing service).

The ideas is that platform engineers provide easy to use abstraction layers for application engineers to spawn new services and required backing infrastructre in very short amounts of time.

In addition application engineers should be able to easily promote their work through various pre-production and finally to producation environments.

This can be considered as self-service and be integrated into internal developer portals as well as any other automation or existing workflows.

## How can catalyst help to provide self-service

The interface for application engineers is a simple YAML file.

The best simple case can be that the engineer requiring to spawn a new service just gives that service a name, selects the required backing cloud services, creates a pull request and can start adding the required business logic within minutes instead of days.

All the required details like what run-time environment shall be used, into what network a required database shall be deployed, how does the application access the database, how does the application deploy shall not be of any concern and just be forgotten about the application developer.

On the other side the required details shall be the concern of a platform engineer. Catalyst provides the capability to translate the inputs the application developer provides into more complex configurations. The platform engineer defined how a cloud resources need to be configured to be compliant, where the resources need to be deployed, how the resources are grouped together into stacks to lower risks of later changes (reduce the blast radius, reduce deployment times on changes in configuration).

The platform team also decides what technologies are used as an "engine" behind the scenes: Terraform, OpenTofu, Helm, Kustomize, CloudFormation, or any combination of those or other IaC tools.

Catalyst can be used to genearte any combination, any complexity, and any scale based on a simple interface that is provided to the aplication developer and filled with pre-selected set of possible values.

When promoting the service through environments e.g. from dev to staging to production, the application developer should only choose where to go next and what differences in scale are required.

Catalyst takes the responsibility to:
- provide standardized interfaces to application developers
- hide the complexity from non-experts
- allow to define those interfaces to the needs of applications developers by platform teams
- provide standardized, compliant and secure configuration behind the scenes
- allow experts to build whatever is required and decide on the flexibility given to the user
- create a collection of different service types to choose from: frontends, backends, consumers, wokers
- integrate new services into existing configurations like DNS, load-balancers, networks
- promote configurations through environments with easy

Catalyst enables non-cloud-experts by empowering cloud-experts to hide all the rrequired details and complexity from the end-users.

The benefits are
- standadized interfaces prevent misconfigurations
- simpler configurations lead to faster go to market for new services/workloads/applications.
- hidden details allow for transparent refactors and contineous improvements of the platform behind the scenes.
- single points of truth allow to roll out any on required security, compliance or performance upgrades globally without bothering application developers

[contact us]: https://terramate.io/demo
