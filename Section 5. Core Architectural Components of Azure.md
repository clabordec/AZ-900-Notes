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

- <b><u>The Americas<u></b>
- Brazil South
- Canada Central
- Central US - East US - East US 2
- South Central US - West US 2 - West US 3
- US Gov Virginia
