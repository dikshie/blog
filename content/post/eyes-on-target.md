---
authors:
- kstrini
- rkelapure
categories:
- App Transformation
- Modernization
- Pivotal Cloud Foundry
- Agile
- Secure fielding
- Mission Control
date: 2017-11-18T17:16:22Z
draft: true
short: Continuously Fielding Mission Driven Value
title: (-0-0-) Eyes on Target  
image:
---

**Sisu** - A Finnish term, meaning strength, perseverance and resilience.
>to commit oneself fully to a task and to bring that task to an end.

At Pivotal, when we entered the national security space we made a conscious effort to translate the shared values of our company and our commercial customers into those that were culturally aligned with this community. We did this with the stubborn intent to not sacrifice the speed at which we enable our customers to deliver innovation. It required us to extensively collaborate with national security customers to define an entire new primary goal in order to align value and distill the non-value added work in pursuit of this goal. This new primary goal was the development and implementation of a continuous fielding model. With this model we collectively are working to overcome the delivery challenges of fielding to the last mile, out to the edge through a unified fielding platform strategy.

In the national security space its not how fast can you get an idea into production but how fast can you deliver a compliant solution to a mission need. This continuum requires all of the pieces to be accounted for including compliancy and drives a single albeit complex KPI, the mean time between fielding. This KPI measures our  ability to deliver what is truly important, the velocity to maintain the Effective Operational Agility necessary to maintain a Continuous Advantage over our Adversaries.

## Factors impeding Goals

In the beginning, there were several challenges impeding our ability to deliver on the promise of velocity. We discovered that in order to reach the field, every application must pass through various organizations corresponding to delivery phases each with their own lead, review, and report generation time. There was no cross-functional platform or capability development teams and a general lack of transparency of an application’s progress across these vertical boundaries.

This was the primary root cause of what evolved into these complex high risk deployments per vertical that required high touch specialized skill sets which corresponded to higher costs to execute. These high touch processes were due to a general lack of a consistent governance model. This directly limited the acquisition community’s ability to respond to changes in the threat without accepting significant security risks and potential system impacts.

In addition, the fluctuating budgets of the delivery teams from code development through the fielding process had led over time to disparate code bases, development teams, and environments for each vertical delaying fielding time and making it cost prohibitive to even fielding a single capability. This led to spending a significant amount of time around the delicate nature of high touch delivery instead of investing in the robustness of non-functional needs leading to limited protection from failures in production.

Its important to understand that failure due to inadequately addressing non-functional aspects has severe impacts in this environment. Typically, requirements don’t sufficiently address non-functional needs. Budget drops result in even less interest in addressing non-functional requirements. So there are two basic approaches in addressing this impediment. We could have continued to respond to failures reactively (fire fighting) or offload these concerns to a platform technology that has built in non-functional aspects as a first class citizen. We needed to combine the technical enablement with the cultural enablement necessary to move from reactive to proactive operations.

## How Operators deploy and run software

So we began diligently working on the organizational transformation process but ran into several factors working against us. First, the federal acquisition process incentivizes schedule over performance. Couple this with the testing processes often result in meeting minimum requirements and this leads to little incentives to deliver exceptional products.

These two factors (performance and testing) are key building blocks necessary in both safely moving legacy workloads to the platform and building quality from the ground up in greenfield efforts going forward. We decided to start with changing the morale of the engineering culture, a critical base to win over. We needed to convince them that the idea that functionally acceptable is not acceptable. We wanted to remind them that the the warfighter/analyst/operator we are delivering to demands an individual personal drive to excellence in addition to an exceptional synergy within a team. These elements are critical in both fielding delivery and sustainment of every capability.

We discussed with teams how those factors that were necessary but not necessarily interesting to developers could be offloaded to a common platform. This would bother lower cost and barrier to entry for each development team. This was due to the reduction in the number of technical aspects their engineers needed to learn to be productive in delivering capabilities to the field. From each team’s perspective there would be a realized cost savings in the amount of training and maintenance required to sustain their capability for the end user. This promise was the first step in delivering a wider commercial opportunity in which the market’s invisible hand will increase the excellence of the capabilities being developed and the associated costs in producing them.

Finding empathy with the delivery teams, meant understanding how difficult safe software deployments are in the national security arena. Separate teams/organizations responsible for the different phase in a delivery mean less shared understanding. Lower deployment frequency is more prone to errors. You take this complexity and exponentially expand it when you approach the scale necessary to support national security. We recognized that the two major factors contributing this complexity.

The first factor was that there was no unified common platform strategy for the delivery teams to rally around and build a consistent knowledge base and governance control point. So to address the first factor knew that as a team we needed to be able to do repeatable deliveries with validate results that were defensible. This included using version control for all components in the platform inventory. Through automation this would significantly the traditional System Operational Verification Test (SOVT) and eliminate the far more System of System Enterprise (SOSE) tests.

The second factor was that there was a perpendicular communication flow being exercised yet the delivery flow was moving in a parallel direction. To address the second factor we began to have discussions about organizing around operational mission driven value streams. This meant recruiting direct warfighter involvement to drive product development. The benefits of this meant that the delivery team would have a better understanding of operational relevancy. They could better understand the decisions they make while still maintaining a high level of application knowledge. The result of this change meant that there was a higher level of accountability and ownership throughout the lifecycle of the application. This was true for the delivery team as well as the end user who was taking delivery of the application as they typically aided in its creation and maturity. We now had a parallel solution for the perpendicular communication flow problem.

One of the big, but necessary, impedances to continuous fielding is the security and accreditation compliancy issue. From an operations perspective, this breaks down into a number of different smaller challenges to consider and improve upon. For instance, maintaining patched systems and the latest capabilities at the scale of the entire enterprise. Doing this without scheduling downtime or even having to notify the end users at all is fundamentally necessary when supporting mission critical workloads.

In the past, this was an intricate dance between the developers and the operators.  Operators needed to schedule and coordinate patch changes, developers needed to test those changes, and then there was a back in forth between the groups needed to execute the timing of these patches into operations. By moving the demarcation line to the platform it allows the developers to offload the implementation responsibilities. It allows the operators to standup and test patches uniformly across the application portfolio and then report findings ahead of moving them into operations. Once the team agrees on the confidence of the CVE patch, Operators could move this patch across the entire operations enterprise in a canary style deployment maintaining 24/7 uptime in support of mission critical workloads. This is now possible because of the unified governance model the platform is able to enforce through api-level promises to each application within the foundation.

This same approach is how we can now maintain a unified security model across the entire application portfolio deployed within the platform. Authentication is offloaded to the Enterprise Identity Provider (ADFS) and the platform is authenticated using Single Sign On (SSO) via SAML. Application developers then receive an OAuth token back and can secure their protected resources to whatever granularity makes sense within their subject matter domain. This allows developers to test both inside the platform and in isolation prior to pushing. It also offloads the heavy weight portions of security to an already approved solution by security. In the past, the security and IA teams had to do extensive reviews to understand how each delivery would affect the overall security posture of the enterprise. This is another aspect that in the past that would slow down the fielding process, as each delivery was a security snowflake responsible for the entire systems set of controls. This often required an entire infrastructure support team just to deliver application code.

{{< responsive-figure src="/images/eyes-on-target/sfielding.png" alt="Securing Fielding" class="center" >}}

Understanding the how the runtime security model would be implemented cleared several challenges for continuous fielding. However, there were still the platform components and their updates to respond to changing cyber threats. In addition to this, new application feature developments necessary to evolve with the current and future threats. We approached this by focusing on the application bits as the currency throughout the whole delivery process. We separated concerns via clearly defined API level coordination between distributed components. Our underlying release engineering and deployment lifecycle tool chain could be defined via statically typed version controlled artifacts. These artifacts were executable and a microservice that is hashed and verifiable by the security team. This gave them a transparency into exactly what was running in operations. It has the secondary benefit of minimizing configuration drift common in large enterprises. This combined with the necessary security controls implemented and verified all the way to the container, left just the changing application bits as necessary continuously accredit.

## How Developers continuously field software

**Secure Software Delivery Pipeline**
{{< responsive-figure src="/images/eyes-on-target/ssdp.png" alt="Secure Software Delivery Pipeline" class="center" >}}

This was a fundamental change in how accreditation could be done. In order to take advantage of this opportunity, several threat vectors in the application delivery process had to be addressed.

First, we needed a way to verify that only approved developers were able to commit to the official source code repositories. There needed to be secure transport between the source code repository and the build servers. Credentials in the build process that required access to environment resources needed to be restricted to test authority scope only. Before any build executed the commit signatures in the source code repositories needed to be validated.

Next, once in the build process, a minimum set of security scans needed to be a part of every build session. These security scans needed to all be able to execute before failure findings are sent back to developers to minimize build sessions. Upon build success, security chain of trust needed to be initiated starting with both auditing and signed binary artifact. From here, an automated, independent reproducible build would be initiated and the resulting hash would be verified against the signed binary. This resulted in a successful push through a secure transport to release repository in which metadata and the appropriate Application Service Group (ASG) defining the production resources would be stored.

Finally, the operations pipeline would pick up the binary, ASG, and metadata, provision an ephemeral key promise, push the binary to a space within Cloud Foundry and apply the appropriate ASG. The runtime instance would ask for the authorization token and run time keys. This would guarantee only authorized instances in operations and eliminate configuration drift.

This is where the biggest reduction on an order of magnitude in fielding time occurs. This is due to the smaller scope of application accreditation vs. stack/type accreditation, automated security scanning pipeline, runtime authorization and verification of the binary artifact in an independent build process.

## How Operators continuously monitor/respond to running software

So now that we are in operations, how do we improve the run time experience for the warfighter? Well several factors aide in this goal. One, by being on Cloud Foundry all logging and metrics are treated the same. This allows the operators to build enterprise-wide monitoring of several different aspects of the environment. All metrics and logs are event streams and can be drained to a number of different 3rd party tools that allow them to watch aggregates of app/component health across the platform. They also can monitor for any security events, container events, and resource access. Since all the distributed components and application containers adhere to the API contracts enterprise alerting can be activated for relatively minimal effort. This also ensures that future workloads won’t require any understanding of how the event streams work in order to be added to the watch list.

These features combined with the built in resiliency and fault tolerance provide a comprehensive self-healing element to the platform. This removes most recovery burdens from the operator. These recovery capabilities include restarting failed system processes, recreating missing or unresponsive VMs, the deployment of new application instances if they crash or become unresponsive, application striping across availability zone and dynamic routing and load balancing all out of the box.

## How Developers build Mission Critical Apps

The key opportunity for developers is in designing mission critical resiliency into the application architecture by leveraging the distributed nature of the platform. By being able to field to the edge, you get performance improvements in end-user latency and transfer speed. This is due to a reduction in lag by eliminating the long haul physics. This will be especially evident in the increase in transfer speeds from imagery and command-and-control applications due to proximity of the provisioned resources.

The distributed platform has several components built-in that are designed to work across geographic boundaries. Applications deployed to the platform can now be evolved to take advantage of the platform level high availability and resiliency. This combined with the wan level caching technology can support the end user operating in both a connected and disconnected manner.

Additional capabilities in the platform include smart routing, service discovery, circuit breaker, data integration and real time processing at scale. These capabilities support multiple approaches to addressing the different mission functions. These include aspects such as the application’s data synchronization strategy, availability and consistency tolerance. These are all important element in designing how the applications will behave during a reduction in capability due to operations within Anti-Access/Area Denial (A2/AD) like conditions.

These behaviors would also support partial datacenter outages or remotely hosted services. These can be mitigated with service discovery and circuit breaker technologies that are native to the platform. These can help developers calculate latency penalties switching between instances and build this type of intelligence into the applications themselves. This becomes truly powerful when combined with Layer 2/3 Quality of Service (QoS) optimizations in data prioritization in degraded environments.

Finally, expected behavior in fail-over scenarios in the case of a full data center outage. The ability to exercise the applications resiliency on a monthly, weekly, daily basis is important especially once the application is fielded. The complexity of how programmatically the application will switch over to an available data center and all the elements within the application that will need to account for this change such as routing, storage for recovery of state, and data stores needs to be done often in order to reduce the operational risk associated with failures.

_Next in our Challenges in National Security Delivery series we will discuss a few related topics in more detail. In part 2, **Watching the Vapor Trail**, we cover how we fit our user-centric software design model into the DOD paradigm. In part 3, **Securing the Perimeter**, we cover how we are working to ensure chain of custody in the Continuous Integration/Continuous Delivery application pipelines. Finally in part 4, **We the Few**, we talk about critical team compositions for Day 2 platform operations._