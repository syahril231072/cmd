# Article CMS (FlaskWebProject)


## Analyze, choose, and justify the appropriate resource option for deploying the app.

### Analyze costs, scalability, availability, and workflow.

|  Virtual Machines | App Service |
| --- | --- |
| There are 3 plans: Pay as You Go, Spot, Reserve (1year/ 3year), For PAYG there are basic and standard VM for Linux and Windows, and the price is hourly based |There are 5 plans, Free (F), Shared (D), Basic (B), Standard (S), Premium (P), and the price is monthly based F1 = Free D1 = 9.67 USD/month B1 = 55.80 USD/month B2 = 111.60 USD/month B3 = 223.20 USD/month S1 = 74.40 USD/month S2 = 148.40 USD/month S3 = 297.60 USD/month P1 = 223.20 USD/month P2 = 446.40 USD/month P3 = 892.80 USD/month |

VMs are more flexible as it is paid hourly, but app service is paid monthly, except for free tiers.

| Scalability | Virtual Machines | App Service |
| --- | --- | --- |
| Autoscaling | Virtual machine scale sets | Built-in service |
| Load balancer | Azure Load Balancer | Integrated |
| Scale limit | Platform image: 1000 nodes per scale set, Custom image: 600 nodes per scale set | 30 instances, 100 with App Service Environment |

VMs are more scalable than App Service in term of Autoscaling, Load Balancer and Scale limit, as mentioned in table above. For example VMs have capability to make scale sets compared to App Service has only built-in service. 

| Availability | Virtual Machines | App Service |
| --- | --- | --- |
| SLA | SLA for Virtual Machines | SLA for App Service |
| Multi region failover | Traffic manager | Traffic manager |

Availability means to reduce the possibility of service impact in case of planned or unplanned downtimes. In term of Multi region failover, VMs and App Service have trafic manager. However in term of SLA, VMs and App Service have different SLA. In this regards VMs have more availability because For all Virtual Machines that have two or more instances deployed across two or more Availability Zones in the same Azure region, Azure guarantee you will have Virtual Machine Connectivity to at least one instance at least 99.99% of the time. This more than App Service where Azure guarantee that Apps running in a customer subscription will be available 99.95% of the time. Only on Virtual Machines that have two or more instances deployed in the same Availability Set or in the same Dedicated Host Group, Virtual Machines that have two or more instances deployed in the same Availability Set or in the same Dedicated Host Group and Single Instance Virtual Machine using Standard HDD Managed Disks for Operating System Disks and Data Disks, azure gurantee less than 99,95%.

In term of workflow, the development of app is much simpler and faster in Azure App Service. 

### Choose the appropriate solution (VM or App  Service) for deploying the app

The choice depends on whether on our application.If we wanted to verify our server configurations and analyze some performance issues. It seems this isn’t possible, since App Service is a managed platform that handles deployment for us. There is no simple way to gain access to the app configuration files once it’s running. Virtual machine is also more scalable and available than App Service. In term of price we need to calculate first as both have different tier price. But for workflow App Service is more simple.   

### Justify your choice
 
As we assume CMS app is simple application, we better choose use App Service because managed platform that handles deployment for us. We can also use F1 Tier of App Service as it is free. Even the simplest VM (Compute (A0), PAYG, West US Region, Linux OS, Ubuntu Type, Basic Tier) cost US $ 0.018 per hour or US$13.14 Average per month.

## Assess app changes that would change your decision.

But if the user of application is increasing a lot and need more feature, than scalability and availability become main consideration and we want verify our server configurations and analyze some performance issues, than we have to move the application to run in VM.
