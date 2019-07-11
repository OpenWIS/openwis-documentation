---
title: Release Management
layout: page
---

## Overview of Continuous Integration (CI) and Continuous Delivery (CD)

### CI and CD Explained

**Continuous Integration**

Continuous Integration (CI) is a software development practice where members of a team integrate their work frequently - usually each person integrates at least daily - leading to multiple integrations per day. Each integration is verified by an automated build process (including testing), and this allows to detect integration errors as quickly as possible. Many teams find that this approach leads to significantly reduced integration problems, and allows a team to develop cohesive software more rapidly.

**Continuous Delivery**

Continuous Delivery (CD) is a software engineering approach in which teams produce software in short cycles, ensuring that the software can be reliably released at any time. It aims at building, testing, and releasing software with greater speed, frequency, and confidence. The approach helps reduce the cost, time, and risk of delivering changes, by allowing for more incremental updates to applications in production. A straightforward and repeatable deployment process is important for continuous delivery.

### Benefits of practicing CI and CD

1.  Risk Mitigation: Local development environments very often differ from where the application will actually operate, and such differences might lead to defective code. Continuous Integration allows to mitigate risk not only with automated testing, but also by enabling production parity. Quality Assurance (QA) tasks - such as browser testing - can also be automated, mitigating the risk of a bug making it all the way through to the production environment.
2.  Reduced Integration Effort: More often than not, software development requires multiple people working concurrently on different parts of the code. When the code will eventually be integrated problems may arise, and depending on their severity, debugging and solving them may require significant effort. Integrating on a daily basis - or even more frequently - can help reduce this effort to a minimum.
3.  Improved Code Quality: CI/CD environments allow the utilization of plugins that perform code quality metrics. These plugins produce reports which are then delivered to the development team, highlighting poor code and even suggesting remedies. Having a centralized point of code QA means that the overall quality will always exceed the minimum requirements, and thus lead to better software.
4.  Automated Analysis & Reporting: Incorporating continuous testing and inspection into the CI process is valuable to developers and managers alike. There are insights to be gained on the progressive health of the project, and it is useful to have a historical time-line of metrics to draw upon and look to for trends. The availability of these analyses tends to encourage a period of reflection after each integration, which will underpin the direction of the project.
5.  Increased Confidence: Writing high quality code that continuously passes tests increases self-confidence in developers, and this allows them to become more productive. It also increases the confidence of the stakeholders into the product itself, allowing them to focus more on "what next", rather than "what now".
6.  Automated Release/Deployment: The typical CI/CD life-cycle consists of building the project, automated unit (and functionality/integration) testing, deploying to the staging environment, and performing UAT. Once the project successfully passes all of these stages, it is ready for deployment to the production environment. Delivering a product to the production environment can be done automatically like the previous stages, but due to certain business concerns (e.g. notifying and getting feedback for potential downtime), it may be more suitable to do it manually.

### Points of Emphasis regarding CI and CD

- CI/CD platform licensing and maintenance: Free/OSS platforms do exist, but sometimes have limitations or require the integration of other free/OSS tools for added functionality, leading to an increase of maintenance effort. Commercial platforms still require DevOps for maintenance, but are usually more feature-rich and easy to use.
- Sufficient unit (and potential functionality/integration) test coverage: Developers need to invest significantly more effort in creating tests, since these tests will reflect the overall health of the software.
- Frequent code merging: In order to ease the integration process, developers must refrain from completing huge sections of code before they merge it back to the repository. Also, the utilization of feature flags might be necessary in order to keep incomplete features from reaching the production environment. All this - inevitably - leads to an increased development cost.
- Improved documentation: Since incomplete features might make it to the code repository, it is important that everything is fully documented, in order for developers to understand code produced by others, and also avoid code duplication.
- Developer education/culture: CI/CD is not the standard/mainstream practice for most developers. As a result, new team members need to be introduced and sufficiently educated around it, in order to adhere to its principles and become productive.

## The Current OpenWIS CI and CD infrastructure and processes

### OpenWIS Baseline Deloyment Architecture

The baseline deployment architecture for the proposed deployments is shown in the diagram below. All VMs are deployed within a Virtual Private Cloud (VPC) within Amazon Web Services (AWS) infrastructure (currently targeted at the European-West Region based in Ireland). The VPC comprises two subnets: a public subnet accessible to the outside world (subject to firewall constraints), and a private subnet accessible only from the public subnet.

The public subnet will contain a Bastion server to allow the VPC to be managed remotely, both by OpenWIS administrators and also the Jenkins platform. This is a Linux server (currently Ubuntu Linux) which accepts SSH access from selected IP addresses. A NAT server provides outbound access to the wider internet, to enable VMs to reach remote repositories for installation of required third party software if needed.

The public subnet will contain the VMs to which the OpenWIS subsystems are deployed. Nominally these are:
- Database subsystem (including Solr Tomcat)
- Security Service
- Data & Management Services
- Staging Post
- Administration Portal
- Public Portal

#### Database subsystem (including Solr Tomcat) Blurb

#### Security Service Blurb

#### Data & Management Services Blurb

#### Staging Post

#### Administration Portal

#### Public Portal

#### OpenWIS-Baseline-Deployment-Architecture Graphic
    insert graphic  Here!

## Repeatable OpenWIS Automated Deployment

The OpenWIS automated deployment approach makes use of the following elements:

- Cloudbees/Jenkins Continuous Integration Management (already set up for OpenWIS)
- Plug-ins added to Jenkins to support CloudFormation & invoking Linux commands/shell scripts via SSH
- Amazon Web Services CloudFormation scripts
- Linux shell scripts

The diagram below illustrates the way that Cloudbees/Jenkins orchestrates automated build, environment creation, and system deployment:

![alt text](http://github.com/OpenWIS/openwis-documentation/release-management/images/OpenWIS-Baseline-Deployment-Architecture.png)

The implementation of the above process on Cloudbees makes uses of the [Jenkins Build Pipeline plugin](https://plugins.jenkins.io/build-pipeline-plugin), and be seen in the image below:

Picture

## Repeatable Automated Regression Testing

The build process also provides the capability to execute a suite of repeatable automated tests against the OpenWIS codebase and deployed OpenWIS subsystems. This capability will have the following benefits:

- Ensure the continuing reliability of the OpenWIS codebase
- Reduce the overall time required in testing each release of OpenWIS
- Reduce the manual overhead required in testing each release of OpenWIS
- Allow testing to be scheduled outside of office hours
- Ensure repeatability between tests
- Provide support for upgrading underlying technology stack (‘Middleware’)

Picture

## Current OpenWIS Build State

This section outlines the current state of the OpenWIS build in Cloudbees/Jenkins.

## Forgerock OpenAM

OpenWIS develop branch currently uses Forgerock OpenAM 12.0 for authentication. A change in Forgerock policy in 2017, mandated a modification in the OpenWIS build process, since the required artifacts were no longer freely distributed, but needed to be "built from source" in order to be used.

This led to the creation of the forgerock-openam-12.0 build project on Jenkins, which is responsible for creating the required Forgerock artifacts, and then deploying them to an internal Cloudbees maven repository, so that they are available from the OpenWIS build projects. This build project depends mainly on a custom shell script which downloads the required source code, and afterwards builds and deploys the artifacts.

An important detail of this build project is that it does not need to execute repeatedly. Once it executes successfully, the artifacts become available for other projects on Cloudbees.

The project configuration can be seen below:

Picture

## OpenWIS Nightly

The main build task on Jenkins is the nightly build which - as the name suggests - runs every night, using the latest code from the develop branch. It uses the aforementioned Forgerock OpenAM 12.0 artifacts and will fail if they are not available in the referenced Cloudbees maven repository.

The project configuration can be seen below:

Picture

## OpenWIS 3.14.9

The development of OpenWIS 3.14.9 is a work in progress, and a build project is available on Jenkins. This version of OpenWIS uses the Forgerock OpenAM 13.0 artifacts, thus a new build project for those artifacts will eventually have to be created.

## Observations

European Dynamics engineers have been requested to perform tasks on the OpenWIS Cloudbees installation on several occasions, and although they do not claim expertise on the said platform, have noted the following items of interest:

1. Dedicated DevOps

In order for CI/CD processes to produce the best results, ensuring that the CI/CD pipeline is always operational has the highest priority. The impression received by the ED engineers is that although a Release Engineering team exists, it is not 100% available for the support of the OpenWIS CI/CD environment.

2. Test Coverage

There was no obvious way to measure Test Coverage, so ED engineers temporarily installed the Emma Jenkins plugin in order to examine the percentage of code covered by tests. As can be seen in the report below, only 2.3% of the total Lines Of Code are covered by the existing tests. This percentage is not adequate for a CI/CD process, since automated testing plays a very important role.

Picture

3. Static Code Analysis

No static code analysis reporting was found to be configured for the OpenWIS builds, even though this functionality is supported by Jenkins.

4. Disabled Latest Stable Branch Build

The latest production/stable OpenWIS branch (3.14.8) does have an associated build project, but that is disabled, as can be seen below. This creates a risk in a situation where changes are merged from the develop branch.

Picture



What's described below is an overview demonstrating the components and interactions involved in building, deploying and testing the OpenWIS application.

The CI process for the OpenWIS uplift is described in more detail below.  In short, the integration manager role(ops) is responsible for updating the scripts and updating the build profiles based on developers/testers contributions and requests.



