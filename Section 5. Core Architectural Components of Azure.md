# Core Azure Architecture

## Azure Regions 
## Region Pairs 
## Sovereign Regions

<br>

### Regions

- Areas of the world where Azure has a set of datacenters (minimum 3 in a set)
- Not necessarily "countries" but can be
- Usually each region is connected to another region to make a "region pair"
- Region pairs have highest speed connections and special treatment during Azure updates

<br>

### E.g Canda

- Canada has two regions - Canada Central and Canada East
- Data stored in these regions never leaves Canada
- Anyone can use these regions

<br>

### E.g Brazil

- Brazil only has one region - Brazil South
- Currently is the only region South America, but Chile is coming online soon
- Paired with South Central US (one way)
- Data does leave Brazil

<br>

### E.g Qatar

- Qatar is the first region that does not have a pair
- Dose not support Geo-Redundant Storage (GRS) option
- Uses Availability Zones for high availability

<br>

### Example Pairs
- Canada      Canada Central - Canada East
- Europe      North Europe - West Europe
- USA         East US - West US
- USA         East US 2 - Central US
- USA         North Central US - South Central US
- Brazil      Brazil South -> South Central US: one way pair

<br>

### When you create a resource in Azuree, you have the choice of where to deploy it to

<br>

### 60+ regions but most of them are not available to everyone


<br>
<br>


## Sovereign Regions

### Sovereign Azure

- These are not connected to the Azure Public Cloud
- Require approval to join / create a subscription
- Adhere to different compliance standards

<br>
<br>
<br>


# Availability Zones

## Azure availability zones are physically seperate locations within each Azure region
## Not every region supports Availability Zones

<br>

### Regions with Availability Zones

- <b><ins>The Americas</ins></b>
- Brazil South
- Canada Central
- Central US - East US - East US 2
- South Central US - West US 2 - West US 3
- US Gov Virginia

<br>

- <b><ins>Europe</ins></b>
- France Central
- Germany West Central
- North Europe - West Europe
- Norway East
- UK South
- Sweden Central
- Switzerland North

<br>

- <b><ins>Middle East</ins></b>
- Qatar Central
- UAE North

<br>

- <b><ins>Africa</ins></b>
- South Africa North

<br>

- <b><ins>Asia Pacific</ins></b>
- Austrailia East
- Central India
- Japan East
- Korea Central
- Southeast Asia - East Asia
- China North 3


<br>
<br>


## Not every service supports Availability Zones

### Three Types of AZ Services

- Zonal Services
- Zone-Redundant Services
- Always Available Services

<br>

### Zonal Services

- You can choose a specific Availability Zone to deploy the service too
- You then should deploy a duplicate service to another zone to achieve resiliency
- E.g: Virtual Machines

<br>

### Zone-Redundant Services

- Automatically deployed across zones for you
- You don't have to confifure it
- E.g: Azure SQL Database

<br>

### Always Available Services

- These are global services and Microsoft takes care of the ensuring that they are always on
- Also called "Non-regional services"
- E.g: Azure Portal, Azure Active Directory, Azure Front Door


<br>
<br>


## Some services give you the choice between zonal and zone-rediundant

<br>
<br>
<br>

# Resources & Resource Groups

### Resources

- A generic word to represent an Azure service that you have access to, such as a specific Virtual Machine, Storage Account, or Database
- You can create a resource in many different ways - Azure Portal, CLI, OowerShell, ARM Template, etc
- Each resource has a name created by you
- Sometimes it has to be unique, sometimes not
- Generally, you indicate the region where they are created

<br>

### All Resources

- A brand new subscription is created with no resources
- Most resources have costs associated with them
- The resource is associated with one (and only one) subscription, to which the cost gets billed

<br>

### Resource Group

- A logical grouping of resources
- Resource Group associated with a region, which can be different than the resources it contains
- All services in a resource group should have a similar lifecycle - deploy together, delete together

<br>

### Resource & Group

- All resources must belong to one and only one resource group
- Permissions can be assigned at the resource group level
- There is no security boundary offered by a resource group for communications

<br>
<br>
<br>

# Subscriptions

### What are Subscriptions

- The bulling unit within Azure
- Always a payment method associated with a subscription
- Users can have access to more than one subsciption, and different roles

<br>

### Subscription Plans

- Free plan - $200 credits first 30 days
  - Can only have one
- Pay as you Go - billed to credit card
- Enterprise Agreement - EA
- Free credits - MSDN, startup plans

<br>

### Multiple Subscriptions

- Some companies can chooes to have multiple subscriptions
- Can be used to seperate out business units within an organiztion - e.g. Sales, IT, Finance
- Or seperate by geography - e.g. North America, Europe, Asia


<br>
<br>


## It's possible to operate an entire organization on a single subscription
