                                                                                                   # Aws-EKS-AutoScaler


# step 1)

create IAM Role for EKS cluster
=============================================================================

# step 2

create VPC for worker node with AWS CloudFormation using vpc.yml
=============================================================================

# step 3

create EKS Cluster and connect to it with cloudshell and execute these commands:

```bash
aws configure list 
aws eks update-kubeconfig --name <cluster-name>
kubectl get nodes
kubectl get pods -A
```
=============================================================================

# step 4

create IAM Role for worker node with these specific Roles

1) Amazon EKS worker node policy   #permissions for ec2 as desribe instance
2) Amazon EC2 container Regestiry  #permissions to ec2 to read from ecr
3) Amazon EKS CNI                  #gives IP address to ec2
   
Then create the worker node (node group)
=============================================================================

# step 5

add cluster Auto-scaler by making the policy then attach the policy to IAM Role





