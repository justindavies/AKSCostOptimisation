# AKS Cost Optimisation demos

We will show a fictional GIS compmany who uses Vahalla to create routing tiles from Open Streetmap data.  The Planet data for OSM is a whopping 67G in size, and Valhalla has an ingestion and transform step to extract node, edges and ways into a format that can be used for routing, and route optimisation.

In this demo we will track the RSS feed for the OSM changes and create Valhalla tiles for those. 

As well as the Planet data, OSM also published data at the city / town level, which we will use to demonstrate ETL at scale.

## Manual
In this demo we will show the cost of spinning up the infrastructure needed pre-emtively to run these ETL workloads constantly.  This type of model would be the same as an on-premise, physical infrastructure provisioning.

When you buy physical hardware and host them yourself.  If the infrastructure isn't being used, or under utilised, you are paying for the resource overhead.  

This is the simplest model to setup, you sping up 10 nodes in a Kubernetes cluster and they sit there ready to take work.  

We will look at the monthly cost of this scenario, and work to cost optimise this through both infrastructure scaling, as well as eventually automation.

## Cost Optimised
In the cost optimised model we will explore cluster auto scaling and spot instances to attribute a cost per compute hour / job and compare this to the Manual model.

## Automated and Optimised
In this final model, we will look at scale to zero, KEDA and efficient workload placement to get the best performance for the price you pay.  The critical part of this is that the customer should see exactly the same runtime benefit (I get my ETL jobs to completion), but the cost benefit of being on-demand and efficient.
