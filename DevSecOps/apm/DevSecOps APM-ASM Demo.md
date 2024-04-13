# DevSecOps APM-ASM Demo

###### Introduction

While handling performance issues surrounding your applications is top of mind, we’re increasingly seeing a disconnect between observability and application security. 

Thus, leaving application development teams in the dark regarding their vulnerabilities.

###### Pivot into APM Service Catalog

With Datadog’s Application Vulnerability Management, we can highlight and correlate your application observability data alongside your security insights. 

###### Pivot into Security tab within APM Service Catalog

From here, we can capture those open source code vulnerabilities associated with your application and gain visibility into your attack exposure to monitor suspicious requests. This allows you the ability to begin your security investigation surrounding your applications and highlight issues you were unaware of. 

###### Hover over any critical vulnerabilities and click into a vulnerability 

Let’s say we’re curious about a specific vulnerability. 

We can pivot into the vulnerability itself and obtain details surrounding what has happened and the associated remediation steps. 

Although, I’d like a more formalized review and deeper insights -- as this is a critical vulnerability within my application. 

###### Vulnerability Sidepanel

Software Composition Analysis (SCA) offers built-in detection capabilities that warn you about vulnerabilities detected in your services’ open source dependencies. 

Details of that information are shown in the Vulnerability Sidepanel, such as identifying the severity, affected services, potentially vulnerable infrastructure, and remediation instructions to solve the surfaced risks.

###### Remain in the Vulnerability and expand “what happened”

Within the signal we have details surrounding what this exact vulnerability contains and its impact on your application. I can see when this was last detected and the window of exposure enabling you to gain insight as to how long this issue has been unpatched. (POINT TO AFFECTED INFRA). To understand the breadth of the attack you can check into the underlying infrastructure to see if anything else was compromised. 

###### Scroll Down to Datadog Severity Breakdown

We then analyze the severity of the application vulnerability against a base score with the associated CVSS. With our Datadog Severity Score for Vulnerabilities we build upon the industry standard CVSS score and add Datadog specific runtime context to help customers focus on the most important vulnerabilities that need immediate attention. We take into consideration services being deployed in production and whether they’re exposed to attack traffic and to rescore the severity of the vulnerability. This helps determine if the vulnerability is critical and needs immediate attention or if you can wait to patch at a later time.

###### Click into Remediation Options

Now you’re given all this context, how would we resolve this issue? With our smart remediation tool we not only provide you with all the remediation options but the best option for your environment. Thus helping you quickly resolve as needed. As you can see we’re able to obtain a wide range of coverage within this single pane. 

###### ASM Overview (click into tab)

Finally, with Datadog ASM you can enable our Threats and Protection with just 1 click to capture malicious requests for when your applications are running. The overview page is the headquarters of your application vulnerabilities with top vulnerabilities and posture evolution to give you a bird’s eye view of everything that is malicious within your environment. This enables for quick detection and investigation. 

