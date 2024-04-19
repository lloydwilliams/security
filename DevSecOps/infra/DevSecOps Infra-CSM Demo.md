# DevSecOps Infra-CSM Demo

###### [Introduction](https://app.datadoghq.com/process?selectedTopGraph=timeseries)

![0-Infra-CSM-Start](images/0-Infra-CSM-Start.png)

Just as your team is responsible for monitoring and proactively responding to discrepancies and issues in your infrastructure, we're increasingly seeing many DevOps teams becoming explicitly responsible for tackling security issues.

That's a difficult ask for teams new to security or have enough on their plates already, which is why we make that responsibility as intuitive as possible with our infrastructure and security correlation.

###### [**Pivot into Infra Resource Catalog (list)**](https://app.datadoghq.com/infrastructure/catalog?activePanel=resource-catalog-main-panel&fillBy=cspm&groupBy=resource_category&page=0&pageSize=50&sort=team&tab=security&viz=list)

![1-Resource-Catalog](images/1-Resource-Catalog.png)

Here we can see a list of all your resources with the misconfigurations and threat signals highlighted at the top. 

Below, we see all of our resources distributed by resource categories and associated threat signals and misconfigurations. 

This helps us determine where many of the issues are located. We can click into them and see the exact resource name, region and other details pinpointing the location. 

###### [Pivot into Infra Resource (Map) fill by signals (last dropdown)](https://app.datadoghq.com/infrastructure/catalog?activePanel=resource-catalog-main-panel&fillBy=cws&groupBy=resource_category&page=0&pageSize=50&sort=team&tab=security&viz=map)

![2-Resource-Catalog-Map-Signals](images/2-Resource-Catalog-Map-Signals.png)

The list view is great, but with a resource map, this provides us a bird eye’s view of all the information -- allowing us to quickly locate and investigate any issues. 

Think of this as the host map from a security context.

###### Click into a finding (hexagon)

###### ![3-Resource-Catalog-Map-Finding.png](images/3-Resource-Catalog-Map-Finding.png)

I’m able to hop right into any resource that has an issue and begin investigating. 

###### [Click on Security tab](https://app.datadoghq.com/infrastructure/catalog?activePanel=resource-catalog-main-panel&fillBy=cws&groupBy=resource_category&page=0&pageSize=50&resourceId=1ddb90ec2bbf34cb03d70e0d796bb978&sidePanelTab=security&sort=team&sp=%5B%7B%22sa%22%3Atrue%2C%22i%22%3A%22resource-catalog-main-panel%22%7D%2C%7B%22sa%22%3Atrue%2C%22i%22%3A%22resource-catalog-main-panel%22%7D%5D&tab=security&viz=map) 

![4-Resource-Catalog-Infra-Host-Security-Tab.png](images/4-Resource-Catalog-Infra-Host-Security-Tab.png)

From here, I’d like to go even further and understand what else could potentially be happening.

###### [Click on a finding within the right side panel (Investigate Button)](https://app.datadoghq.com/infrastructure/catalog?activePanel=resource-catalog-security-signals-panel&fillBy=cws&groupBy=resource_category&page=0&pageSize=50&resourceId=1ddb90ec2bbf34cb03d70e0d796bb978&secId=AQAAAY7YZEC8wcCyngAAAABBWTdZWkVDOEFBRG9PRlltU0F1VzV3QUE&secTab=overview&sidePanelTab=security&sort=team&sp=%5B%7B%22sa%22%3Atrue%2C%22i%22%3A%22resource-catalog-main-panel%22%7D%2C%7B%22sa%22%3Atrue%2C%22i%22%3A%22resource-catalog-main-panel%22%7D%2C%7B%22i%22%3A%22resource-catalog-security-signals-panel%22%7D%5D&tab=security&viz=map)

![5-Resource-Catalog-Infra-Security-Signal-Investigate](images/5-Resource-Catalog-Infra-Security-Signal-Investigate.png)

Right from infrastructure, I’m able to easily pivot into Cloud Security Management (CSM) and proceed with my analysis. 

###### [Click on "View In Signal Explorer" -- Currently in CSM Security Signal](https://app.datadoghq.com/security?query=%40workflow.rule.type%3A%22Workload%20Security%22&column=time&event=AQAAAY7dwYlHw2AcXwAAAABBWTdkd1lsSEFBQkt2RWRfSWhDZm5nQUE&fromUser=false&order=desc&product=cws&start=1712584751278&end=1713189551278&paused=false) 

Welcome to CSM! 

Here I can get deeper insights into malicious actions within my workloads and misconfigurations as well as compliance checks surrounding my cloud resources. 

We’re currently scoped to a security signal allowing you to further investigate this attack and correlate against the observability metrics. 

(close the side panel)

![6-CSM-Signals.png](images/6-CSM-Signals.png)

###### [Click into “Security Inbox”](https://app.datadoghq.com/security/issues?si-type=cloud_security_management)

![7-CSM-Inbox](images/7-CSM-Inbox.png)

With the amount of signals coming in, I’m sure you’d prefer a way to prioritize the most important security issues impacting your workloads. 

You can do just that with our security inbox. 

This cuts down the noise to help you manage different factors of risk.

###### [Click into a Critical Signal  (e.g. “IAM Role”)](https://app.datadoghq.com/security?query=%40workflow.rule.type%3A%22Workload%20Security%22%20status%3Acritical&column=time&fromUser=false&order=desc&product=cws&viz=stream&start=1712941506184&end=1713546306184&paused=false)

Right from here we can dive into an investigation with a description as to why this is an issue. 

We provide remediation steps on how to resolve this and pinpoint the resources that were impacted by this event. 

This provides us with all the context to understand the full scope of the security event.

###### [Click into CSM Vulnerabilities](https://app.datadoghq.com/security/csm/vm?query=severity%3A%28Critical%20OR%20High%20OR%20Medium%20OR%20Low%29%20status%3A%28Open%20OR%20%22In%20progress%22%29%20fix_available%3AAvailable&group=vulnerability) -> click into a critical finding -> click into resource in the dropdown

Now let’s say we want deeper insights combining that infra observability with security insights. 

###### Now Pivot to CSM Vulnerabilities 

We can do exactly that with CSM Vulnerabilities. 

This continuously scans for vulnerabilities

	- within your container images and 
	- hosts within your infrastructure 

and provides you with a description of what happened -- so you’re not left in the dark -- and a window of exposure to understand how long this vulnerability was unpatched in your environment. 

Additionally, with our Datadog severity breakdown, we will analyze the resource and adjust the CVSS score to help you determine whether this needs to be remediated immediately or not. 

Once that’s been determined, you can follow the next steps to remediate this vulnerability and resolve the issue. 

###### [Click into Identity Risk](https://app.datadoghq.com/security/identities) 

Now, pivoting into risk surrounding your IAM configurations within your cloud environment, Datadog **Cloud Infrastructure Entitlement Management**, also known as CIEM, enables you to identify and address - identity risks in your IAM configurations before a threat actor can exploit them.

Mismanagement of these permissions can cause breaches and insider threats. 

Therefore, getting ahead of this, reduces that potential of risk whilst leveraging identity best practices. 

###### [Click into Compliance](https://app.datadoghq.com/security/compliance/home) 

When there’s a lack of visibility within infrastructure, it most likely will be the same with compliance. 

And so, with our compliance overview, we’re breaking down those siloes and enabling visibility. 

Here we can detect misconfigurations around your resources and evaluate your environment against a variety of frameworks. 

The posture scores help you determine how compliant you are against those benchmarks. 

Additionally, it’s easy to share this information within your applicable teams or auditors for evidence during an evaluation.

###### [Click into SOC 2 Framework](https://app.datadoghq.com/security/compliance/home/soc-2?) -> [click into any critical/high finding](https://app.datadoghq.com/security/compliance/home/soc-2?panels=cprule%7Crule%7CruleId%3Adef-000-91j%7CresourceId%3A%7Ccontext%3A%7CshowEvaluation%3Atrue&timestamp=1713546847504&live=true)

Lets take for example SOC 2. 

We can dive into our findings and we’re provided with a description and rationale as seen earlier in our demo as well as the remediation steps.

###### [Click into one of “resources impacted”](https://app.datadoghq.com/security/compliance/home/soc-2?panels=cprule%7Crule%7CruleId%3Adef-000-91j%7CresourceId%3A%7Ccontext%3A%7CshowEvaluation%3Atrue&timestamp=1713546968242&live=true)

But I’d like to gather deeper insights into the resources that were impacted.

###### [Click into resource](https://app.datadoghq.com/security/compliance/home/soc-2?panels=cprule%7Crule%7CruleId%3Adef-000-91j%7CresourceId%3A%7Ccontext%3A%7CshowEvaluation%3Atrue%2Ccpfinding%7C2869%7CruleId%3Adef-000-91j%7CresourceId%3Abaefef872beaecea49d0f4b5ac21748c%7CtabId%3Aoverview%7Ccontext%3A&timestamp=1713546968242&live=true) 

From here, I can obtain the resource type with its ID. 

With our relationships view, we can get insights on where the resource exists and what it is communicating with. 

But I’m also able to triage my findings and: 

	- kick off a workflow, 
	- pivot into my AWS account and view it there, 
	- or I can mute the findings to cut down the noise. 

All accomplished within this single pane, thus cutting down time to detection and resolution.

###### [CSM Overview](https://app.datadoghq.com/security/csm)  

Finally, with our CSM overview, you get a bird eye’s view of everything from: 

	- your threats, 
	- misconfiguration, 
	- vulnerabilities and compliance posture score, 

to help enable broad coverage of your resources from a security perspective and dive back into investigation wherever you'd like -- bridging the gap between siloes across your infrastructure and associated security insights.