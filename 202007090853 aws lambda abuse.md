# aws-lambda-abuse

- **tags**:  #aws #lambda #serverless #attacks
- **sources**:
	- https://luminousmen.com/post/aws-lambda-abuse

![2020-07-09-09-24-02.png](_images/2020-07-09-09-24-02.png)

---
## background
Advantages of using the AWS Lambda:

- **Cost-effective.** You only pay when the service is running(but some services cost a lot).
- **No ops.** You do not need to manage anything yourself. AWS takes care of the operating system, deployment, scaling, and so on.
- **Speed.** The lambda itself goes up and runs very fast(but there are overhead on spinning up the runtime).
- **Scalability.** Functions can be run in parallel with limit depending on the region, from 1000 to 3000 copies maximum. And if you want, this limit can be increased.
 
 ## problem
-  Each function of AWS Lambda works in its own isolated environment, with its own resources and file system. When deployed with API gateways or other services, they could be left exposed to the public Internet.
 
 ## [[attacks]]
 - execution environment for the big 3
 	| function | OS | dir | user |
	| --- | --- | --- | --- |
	| nodeJS 12 | amazon linux 2 | `/var/task` | sbx_user1051 | 
	| .NET core 3.1 | debian GNU/Linux 9 | `/` | app |
	| Go 1.11 | ubuntu 18.04.2 LTS | `/srv/files` | root | 
	
 - [[ddos]]
	- [ ] add section for ddos [[attacks]]

- [[reverse-shell]]
	- since lambdas and serverless components inherently provide a small formed shell environment which to execute commands, one could theoretically gain persistence
	- _basically an sshd for cloud functions_: https://github.com/pumasecurity/serverless-prey

![prey](https://raw.githubusercontent.com/pumasecurity/serverless-prey/main/docs/diagram.png)

