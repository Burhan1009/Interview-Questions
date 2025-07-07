# Interview-Questions
Interview, Certification preparation guide for Cloud DevOps professionals

**DevOps & Cloud Interview Questions (1.5 to 2 Years Experience)**

**Section 1: AWS (Amazon Web Services)**

1. What is the difference between an EC2 instance and a Lambda function?
2. How do you configure a highly available architecture on AWS?
3. What is the difference between Security Groups and NACLs?
4. How does Auto Scaling work in AWS?
5. What are the different types of load balancers in AWS?
6. What is an IAM role and how is it different from IAM users?
7. What is the difference between public and private subnets in a VPC?
8. How do you implement S3 bucket policies to allow access from specific IPs?
9. What is an AMI and how do you create a custom AMI?
10. How do you monitor AWS resources?

**Section 2: Docker**

11. What is Docker and how does it differ from a virtual machine?
12. What is the difference between Docker image and container?
13. How do you create a Dockerfile?
14. How can you persist data in Docker containers?
15. What is Docker Compose and how do you use it?
16. What is a Docker volume?
17. How do you optimize Docker images?
18. How do you check running containers and stop them?
19. How do you access a running Docker container?
20. What are best practices for writing Dockerfiles?

**Section 3: Jenkins**

21. What is Jenkins and why is it used?
22. What is the difference between freestyle and pipeline job?
23. How do you create a Jenkins pipeline using a Jenkinsfile?
24. How can you integrate Jenkins with GitHub?
25. How do you trigger builds automatically?
26. What is a Jenkins agent and master?
27. How do you handle credentials in Jenkins?
28. How can you deploy to AWS from Jenkins?
29. What is a parameterized build in Jenkins?
30. How do you archive artifacts in Jenkins?

**Section 4: CI/CD Concepts**

31. What is Continuous Integration?
32. What is Continuous Deployment?
33. What are the key benefits of CI/CD pipelines?
34. How do you handle rollback in CI/CD?
35. What are blue-green deployments?
36. What is a canary deployment?
37. What tools have you used for CI/CD?
38. What is the role of version control in CI/CD?
39. How do you manage secrets in CI/CD pipelines?
40. What are the common stages in a CI/CD pipeline?

**Section 5: Terraform**

41. What is Terraform and why is it used?
42. What is the difference between Terraform and CloudFormation?
43. What are providers in Terraform?
44. What is the purpose of the "terraform init" command?
45. What are Terraform modules?
46. How do you manage multiple environments (dev/prod) in Terraform?
47. What is the Terraform state file?
48. What are the best practices to manage Terraform state?
49. What is "terraform plan" and how is it useful?
50. How do you handle Terraform secrets?

**Section 6: Git & GitHub**

51. What is the difference between Git and GitHub?
52. What is the difference between git pull and git fetch?
53. How do you resolve merge conflicts in Git?
54. What is a pull request?
55. How do you revert a commit?
56. What is the difference between rebase and merge?
57. How do you create and switch branches?
58. What is a .gitignore file and how is it used?
59. How do you squash commits in Git?
60. What are Git tags?

**Section 7: Real-Time Scenarios**

61. Describe a CI/CD pipeline you created and maintained.
62. How do you handle failure in a deployment pipeline?
63. How do you monitor container health in production?
64. Explain a time when you had to debug a failed Jenkins build.
65. How did you optimize a slow running Terraform apply?
66. Describe an issue with an EC2 instance you troubleshooted.
67. How do you secure access to a production S3 bucket?
68. Explain a real-time use of a Docker multi-stage build.
69. How do you manage infrastructure drift?
70. Describe how you set up a VPC with public and private subnets.

**Section 8: Scripting & Automation**

71. How do you automate daily backups using AWS CLI?
72. Share a Bash script you wrote for automating deployments.
73. How do you use cron jobs in Linux servers?
74. What scripting languages do you use and why?
75. How do you monitor cron job execution?
76. What is a common error you’ve encountered in Bash scripting?
77. How do you check disk usage with a script?
78. How do you automate log cleanup?
79. How do you write a script to check service health?
80. How do you send alerts from a script?

**Section 9: DevOps Culture & Practices**

81. What is Infrastructure as Code?
82. How do you practice DevOps in your team?
83. What’s your experience with Agile or Scrum methodologies?
84. How do you handle postmortems after failures?
85. What tools do you use for monitoring?
86. What is observability?
87. How do you ensure zero-downtime deployments?
88. How do you collaborate with developers in your team?
89. What is shift-left testing?
90. How do you ensure code quality in CI/CD?

**Section 10: Miscellaneous/Advanced Topics**

91. What is the difference between vertical and horizontal scaling?
92. What is serverless computing?
93. What is container orchestration?
94. How do you manage secrets securely in AWS?
95. What is an Elastic IP in AWS?
96. What is a bastion host and why is it used?
97. How do you use AWS CloudWatch?
98. What is a dead-letter queue in SQS?
99. What is the shared responsibility model in AWS?
100. What is the difference between fault tolerance and high availability?

## With Answers 

Here are concise, interview-ready answers (2-3 lines each) for DevOps roles with 1.5-2 years experience:

### **AWS**  
1. **EC2 vs Lambda**:  
   EC2 is a virtual server for long-running workloads. Lambda is serverless for event-driven tasks, scaling automatically with zero administration.

3. **SG vs NACL**:  
   Security Groups are stateful firewalls at instance level. NACLs are stateless subnet-level firewalls with explicit allow/deny rules.

5. **Load Balancers**:  
   ALB (HTTP/HTTPS), NLB (TCP/UDP performance), and Classic (legacy). Use ALB for web apps, NLB for high-throughput.

7. **Public/Private Subnets**:  
   Public subnets route traffic via Internet Gateway. Private subnets use NAT Gateway for outbound-only internet access.

9. **AMI**:  
   Template for EC2 instances. Create custom AMI by snapshotting a configured EC2 instance via AWS Console/CLI.

---

### **Docker**  
11. **Docker vs VM**:  
   Docker containers share the host OS kernel, making them lightweight. VMs virtualize hardware with full OS stacks.

14. **Data Persistence**:  
   Use Docker volumes (`docker volume create`) or bind mounts. Volumes survive container restarts/deletion.

17. **Optimize Images**:  
   Multi-stage builds, minimal base images (Alpine), and combine RUN commands to reduce layers.

20. **Dockerfile Best Practices**:  
   Use official images, non-root users, and `.dockerignore`. Order commands from least to most frequently changed.

---

### **Jenkins**  
22. **Freestyle vs Pipeline**:  
   Freestyle: Simple GUI jobs. Pipeline: Code-defined (Jenkinsfile) for complex CD workflows with stages.

25. **Auto-Trigger Builds**:  
   Configure GitHub webhooks or use "Poll SCM" in Jenkins. Triggers builds on code commit/push.

28. **Deploy to AWS**:  
   Use AWS CLI in Jenkins scripts or plugins like AWS CodeDeploy. Authenticate via IAM roles/credentials.

30. **Archive Artifacts**:  
   In Jenkinsfiles: `archiveArtifacts artifacts: '**/target/*.jar'`. Stores build outputs for later use.

---

### **CI/CD**  
32. **Continuous Deployment**:  
   Automated release of validated code to production. Requires robust testing and monitoring pipelines.

35. **Blue-Green**:  
   Two identical environments. Route traffic from old (blue) to new (green) after testing for zero-downtime.

38. **Version Control**:  
   Single source of truth for code/infrastructure. Enables traceability, rollbacks, and collaboration.

---

### **Terraform**  
42. **Terraform vs CloudFormation**:  
   Terraform is cloud-agnostic with HCL syntax. CloudFormation is AWS-specific using JSON/YAML.

46. **Multiple Environments**:  
   Use Terraform workspaces or directory structure (dev/prod) with variable files (`terraform.tfvars`).

49. **terraform plan**:  
   Preview infrastructure changes before apply. Essential for validation and change control.

---

### **Git**  
52. **Pull vs Fetch**:  
   `git fetch` retrieves remote changes without merging. `git pull` = fetch + merge (can cause conflicts).

55. **Revert Commit**:  
   `git revert <commit-hash>` creates new undo commit. Safer than reset for shared branches.

59. **Squash Commits**:  
   `git rebase -i HEAD~3`, mark commits as "squash". Combines multiple commits into one.

---

### **Real-Time Scenarios**  
61. **CI/CD Pipeline**:  
   Built Jenkins pipeline: GitHub → Build → Dockerize → ECS deploy. Used Terraform for AWS infrastructure.

67. **Secure S3**:  
   Block public access, bucket policies with IP restrictions, encryption (SSE-S3/KMS), and access logs.

---

### **Scripting**  
72. **Bash Deployment Script**:  
   ```bash
   #!/bin/bash
   aws s3 sync build/ s3://my-bucket/ --delete
   aws cloudfront create-invalidation ...
   ```

79. **Service Health Check**:  
   ```bash
   curl -sf http://localhost:8080/health || exit 1
   ```

---

### **DevOps Culture**  
81. **Infrastructure as Code (IaC)**:  
   Manage infrastructure via code (Terraform/CloudFormation). Enables versioning, reuse, and consistency.

87. **Zero-Downtime Deployments**:  
   Use blue-green, canary, or rolling updates. Validate health checks before traffic shift.

---

### **Advanced**  
92. **Serverless**:  
   Event-driven compute (Lambda). No server management, pay-per-use, auto-scaling.

100. **FT vs HA**:  
   Fault tolerance: System operates despite failures. High availability: Minimal downtime via redundancy.

**Pro Tips**:  
- Quantify achievements: "Reduced deployment time by 40% using Docker"  
- For "Describe..." questions: Use **STAR** method (Situation, Task, Action, Result)  
- Always mention security: "I encrypted S3 buckets and used IAM roles for least privilege"
