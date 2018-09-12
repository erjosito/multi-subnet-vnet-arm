# Multi-subnet Vnet ARM template

This short template deploys a Vnet including subnets. Subnets are specified with a parameter as an array of objects. For each subnet different than the GatewaySubnet, an NSG is created and associated with it. This template demonstrates some advanced ARM template concepts:

* How to use and reference object-type parameters
* `copy` function to deploy multiple resources (NSGs) and multiple properties inside of a single resource (multiple subnets inside of a Vnet)
* `condition` function to conditionally deploy a resource (no NSG is provisioned for the Gateway subnet)
* Array functions such as `length` and `contains`
* Logical functions (`not`)
* `json` function to dynamically generate resource properties based on some condition (verified with the function `if`)

