## High Availability (HA)

Availability by itself can also be called uptime.

- Ability of a system to remain operational to users during planned or unplanned outages.

<br>

### Planned Outages

- Operating System security patches
- Application updates
- Hardware replacement
- Migrating to a new hosting provider


### Unplanned Outage

- Hardware failure
- Network disruptions
- Power outages
- Natural disasters
- Cyber attacks
- Software bugs
- Poor scaling / architecture design

<br>

## Methods to Avoid Planned Outage

- Gradual deployment strategy
  - 1-10-100-etc
    - Company with hundreds or thousand don't deploy all servers at once, they'll deploy to just a handful of servers maybe one server, then they'll deploy to a few dozen servres or a hundred servers, and then they will grow to being the entire application.
  - Testing and monitoring of deployment
    - Monitoring the deployement, checking to see if there's been errors, if there is an increase number of 500 server errors or 400 errors, and they can stop the deployment if something has been adversely affected.
  - Easy rollback plan
    - If something does go wrong, and you want to stop and go back to the previous version, Azure has tools to make rolling back deployment easy, including deployment slots.
  - Small deployments
    - If you have less features, less changes in every deployment, then this method will reduce the risk of there being a buug and having to do any kind of rollback.
  - Frequent deployemnts
    - If you do only one deployment a year, then something can go wrong, but if you do deployment every day, then the chances of something going are actually lower.
  - Automation
    - Using pipelines that follow the standards, and avoiding manual deployments

  <br>

  ## Methods to Avoid Unplanned Outage

  - Every single core component has redundancy
    - So you're not going to have a single server, web app, network, regoin that is going to be the dependency for your entire application, so you spread things around and then it affects the cost, but it does improve ypur ability to handle a unplanned outage.
  - Use Azure's built-in features for availability
    - Availability Sets
    - Availability Zones
    - Cross-Region Load Balancing / Front Door
  - Constant health monitoring / probes
    - In an on-going production envoirnment, you want to have health probes and health monitoring, making sure that you can detect if something goes wrong
  - Automation
  - Strong security practices
  - Be geographically distributed
    - Have your application already deployed to multiple regions around the world, they will then take over while the region is dealing with those issues.
  - Have a disaster recovery plan
  - Test that disaster recovery plan / fire drills!
  - Load Testing
    - Send hundreds of concurrent users to your application, finding where that capacity limit is, find out how many users at once can your application can handle, this will help fix any bottlenecks to improve the efficiency of your application, rewrite that code, add additional servers, auto scaling etc. Then push the boundary to get more and more concurrent users in your application.


<br>
<br>


## Scalability

- The ability of a system to accommodate increasing demand by adding or removing resources as needed.

<br>

### Why is it Needed

- It allows a system to adapt to changing usage patterns and handle increased traffic without requiring changes to the application code or system design.

<br>

### Does Traffic Fluctuate

- Some businesses have traffic that fluctates based on time of day of the year
- E-commerce websites have increased traffic on Black Friday
- School registrations are busy in September
- Tax systems are busy in April or depending on where you live

<br>

### The $1M Question

- Can you expand the capacity of a system very easily, by adding more servers?
- Or will it be massive undertaking to do that?

<br>

### Vertical Scaling
- Also called <i>"scaling up"</i> or <i>"scaling down"</i>
- Adding more resources to a single server
- Increase the amount of memory, the number of CPUs
- There is an upper limit
- Azure - 96 vCPUs, 384 GB memory
- Does not improve availability

<br>

### Horizontal Scaling

- Also called <i>"scaling out"</i> or <i>"scaling in"</i>
- Adding more servers to a system
- No limits to scaling
- Additional complexities for load balancing
- Can improve availability

<br>

### Impact on System Cost

- Adding more resources to a system adds to cost
- Reducing resources can reduce cost
- Having a scalable system allows for a system to be perfected sized
- This optimizes the cost by reducing wasted computing resources


<br>
<br>


## Elasticity

- The ability of a system to quickly and easily scale up or down the amount of resources that a system uses in response to changing demand

<br>

### Quickly and Easily

- Has to involve some sort of automation
- Often called "autoscaling" in cloud computing
- The system monitors some metric (such as CPU utilization) to determine how busy a system us
- Adds resources when it exceeeds a limit for being busy
- Remove resources when it falls below a limit for being not busy

<br>

### Why is it Needed

- More efficient and cost-effective use of resources
- Minimizes computing "waste" - resources paid for and not used
- Self-hosted systems tend to have a large percentage of "over-provisioned" resources for anticipated future growth

<br>

### Save Here, Spend There

- Also have the potential to have a minimum capacity higher than you could afford if you had a static provisioning of resources


<br>
<br>


## Reliability

### All Three Relating to High Quality Service

- Availability
- Reliablity
- Predictability

<br>

### Reminder: Availability

- The ability of a system to be accessible and usable by users when they need it


### Reliability

- The ability of a system to perform its intended function without interruption and with a high degree of accuracy
- How dependable a system is
- The ability of a system to perform its intended function without interruption and with a high degree of accuracy

<br>

### Why is it Needed

- You have to trust that your cloud provider is doing everything it can to make its platform reliable
- This includes transparency during service issues

<br>

### How is it Achieved

- Auto-scaling
- Multi-region deployments
- Data backup and replication
- Health probes and self-healing

<br>

### Availability vs Reliability

- A system can be highly available to users
- In that it responds instantly to every request
- The system itself might be highly unreliable
- For example, what use is a calculator that can answer every question with the wrong answer?
- Availability is an appearance to end users
- Reliability is the underlying truth


<br>
<br>


## Predictability

- The ability to forecast and control the performance and behavior of a system
- Includes the ability to predict the future costs

<br>

### Why is is Needed

- Predictability gives you the confidence that the system will continue to perform at the expected level in the future
- And of course that you won't get a crazy bill unexpectedly

<br>

### How is it Achieved

- Auto-scaling
- Load Balancing
- Different instance types, sizes, pricing tiers
- Cost management tools
- API
- Pricing calculators

<br>
<br>

## Security

- Cloud providers are obviously massive targets for hackers, and so they righly spend a lot of time, money and effort on platform security
- Cloud providers go through security audits and compliance certifications
- And provide customers (you) the tools they need to enable and monitor security with their own applications/data

<br>

### Why is it Needed

- Security is a fundamental challenge in IT
- You want confidence that your cloud provider cannot easily be defeated by hackers and those with malicious intent

<br>

### How is it Achieved

- Industry standard compliance certifications
- Microsoft Security Response Center (MSRC)
- Always-on DDoS
- Azure Policy & Blueprint
- Role based access control (RBAC)
- Azure Active Directory
- Always up-to-date platforn services
- Update management
- Encryption by default
- Dozens of security services like firewall


<br>
<br>


## Governance

- How your organization does business
- The process of defining, implementing, and monitoring a framework of policies that guides an organization's cloud operations

<br>

### Why is it Needed

- Your company wants to ensure it's policies are followd in the cloud
- Includes basic auditing and reporting, as well as enforcement
- You want to be compliant with industry standards such as HIPPA or PCC or GDPR

<br>

### How is it Achieved

- Azure Policy & Blueprints
- Management groups
- Custom roles
- Soft delete
- Guides and best practices such as Cloud Adoption Framework


<br>
<br>


## Manageability

- Management of the cloud
- Management in the cloud

<br>

### Management of the Cloud

- Templates
- Automation
- Scaling
- Monitoring and alerts
- Self-healing

<br>

### Management in the Cloud

- Web portal
- Command line interface and scripts
- APIs
- PowerShell scripts

<br>

### Why is it Needed

- How easy it is to work with your applications in the cloud impacts cost, performance, security and other priorities
- Different cloud vendors are going to be easier or harder to work with

<br>

### How is it Achieved

- Azure Portal, CLI, PowerShell, Cloud Shell, REST APIs, and other programmatic methods
- Consolidated monitoring and alerting system
- Ability to use ARM templates, Bicep, Terraform, etc
- Autoscaling of most types of compute resources
 
