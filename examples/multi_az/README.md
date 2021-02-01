# Single Worker Group per Availability Zone

This example creates an EKS cluster with three node groups. Each node group
spans a single availability zone.

It is based on the [basic](../basic) example, and includes the solution
mentioned in
[#346](https://github.com/terraform-aws-modules/terraform-aws-eks/issues/346).

In this example the VPC is created with three private subnets. Each subnet is
created in a different availability zone. By looping over the private subnets
when creating the worker groups, it is able to create one worker group per
availability zone.
