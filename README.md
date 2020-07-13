# GCP-Checklist

Managing Identities — Manage your identities centrally. Make use of groups for ease of administration. Use os login to centrally manage who can SSH into your VM’s
IAM

Use principles of least privilege .

If the predefined IAM roles do not fit your use case create custom roles

If using Custom roles start from a pre-defined role first

Be aware of the operational overhead with using custom roles

Implement break glass access for elevated roles such as the organization admin role that will trigger more stringent auditing around the use of these roles.

Implement Org wide standardization using Organization policies

Network controls — allow you to implement boundaries based on traffic

Subnets to provide a logical boundary based on a subnet range. You have to explicitly allow traffic between subnets

Firewalls to manage what traffic is permitted between a source and target

Use service accounts to configure firewall rules between VM’s

Configure a shared VPC to allow central administration of your network

Use Security zones to provide defence in depth

Securing infrastructure — Take a defence in depth approach using features of the GCP platform and working inwards by implementing security controls applicable to the right layer for your use case

Use Global load balancing together with Cloud Armor to protect your internet facing applications

Use IAP to manage user access to your web facing applications

Use API proxies either Cloud endpoints or Apigee edge to manage authenticated calls to your API’s

Do not make cloud storage buckets publicly available use IAM to manage access

Manage downloaded security keys carefully. Implement a process to rotate, avoid the accidental loading of secrets to private and public repos.

Encryption reqs — If allowing Google to manage your encryption needs is not sufficient for your use case then you can use your own keys. Encrypt your secrets and downloaded keys using KMS

Securing data — classify data — Use the DLP API to classify and redact data , implement iam roles to restrict access to your datasets .Audit data access . Dat lineage and location are all important.

Inventory — Be aware of your GCP resources. Use the Cloud security command center and/or forseti

Auditing & alerting — These are typically the first indications that there is something amiss use Stackdriver to configure audit logging and to set up alerts

Data classification — Use the DLP API to classify and redact sensitive data

Compliance — Use the

Incident responses ( see operational efficiency)

Break glass access
