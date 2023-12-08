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


## Scalability

- The ability of a system to accommodate increasing demand by adding or removing resources as needed.


### Why is it Needed

- It allows a system to adapt to changing usage patterns and handle increased traffic without requiring changes to the application code or system design.


