# Article CMS (FlaskWebProject)


## Analyze, choose, and justify the appropriate resource option for deploying the app.

### Analyze costs, scalability, availability, and workflow.

| Command | Description |
| --- | --- |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |

VMs are more expensive than App Service because we also have to manage the middleware, operation system, runtime and it will increase cost.

| Scalability | Virtual Machines | App Service |
| --- | --- | --- |
| Autoscaling | Virtual machine scale sets | Built-in service |
| Load balancer | Azure Load Balancer | Integrated |
| Scale limit | Platform image: 1000 nodes per scale set, Custom image: 600 nodes per scale set | 30 instances, 100 with App Service Environment |

VMs are more scalable than App Service in term of Autoscaling, Load Balancer and Scale limit, as mentioned in table above. For example VMs have capability to make scale sets compared to App Service has only built-in service. 

Availability means to reduce the possibility of service impact in case of planned or unplanned downtimes. In this regards VMs have more availability because they have two options when it comes to scaling—Virtual Machine Scale Sets and Load Balancers. There are also constraints for the support of certain programming languages on Azure App Service. If we choose VM, we could create environment for the choosen programming language.

In term of workflow, the development of app is much simpler and faster in Azure App Service. 

### Choose the appropriate solution (VM or App  Service) for deploying the app

The choice depends on whether we need to build to simple, faster application and lest costly or the application that is complex and used by many people so we need scalability and availability. If workflow and cost is our main consideration, than we should choose App service, but if scalability or availability is our main consideration than we choose VM.

### Justify your choice
 
As CMS app is simple application and not used by many people, that is why I choose use VM.

## Assess app changes that would change your decision.

But if the user of application is increasing a lot and need more feature, than scalability and availability become main consideration, than we have to move the application to run in VM.
