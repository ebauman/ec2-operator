## ec2-operator

Launch and manage ec2 instances using K8S.

Sample manifest is as follows:
```
apiVersion: ec2.cattle.io/v1alpha1
kind: Instance
metadata:
  name: instance-demo
spec:
  # Add fields here
  credentialSecret: aws-secret
  imageID: ami-0051f0f3f07a8934a
  subnetID: subnet-4e1db116
  region: ap-southeast-2
  securityGroupIDS:
    - sg-072a1fd5523cb961a
  publicIPAddress: true
  instanceType: t2.medium
```