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

### **AWS (Amazon Web Services)**  

1. **EC2 vs Lambda**:  
   EC2 virtual servers hain jo long-running tasks ke liye use hote hain, jinke liye aapko scaling manage karna padta hai. Lambda serverless hai, event-driven hai, aur automatically scale hota hai, pay-per-use model pe.  

2. **Highly Available Architecture**:  
   Multi-AZ deployments (RDS, ELB), Auto Scaling Groups, aur Route 53 failover use karke high availability achieve karte hain.  

3. **Security Groups vs NACLs**:  
   Security Groups instance-level firewalls hain (stateful), jabki NACLs subnet-level firewalls hain (stateless) jo explicit allow/deny rules follow karte hain.  

4. **Auto Scaling**:  
   Auto Scaling EC2 instances ko CPU/memory usage ke basis pe automatically increase/decrease karta hai. Launch Templates aur Scaling Policies define kiye jaate hain.  

5. **Load Balancers**:  
   ALB (HTTP/HTTPS), NLB (TCP/UDP), aur Classic Load Balancer (legacy). ALB web apps ke liye best hai.  

6. **IAM Role vs IAM User**:  
   IAM Roles temporary permissions dete hain aur services/users assume kar sakte hain. IAM Users permanent credentials hote hain (humans/scripts ke liye).  

7. **Public vs Private Subnet**:  
   Public Subnet mein IGW hota hai aur public-facing services (e.g., ALB) host kiye jaate hain. Private Subnet mein NAT Gateway se outbound internet access hota hai.  

8. **S3 Bucket Policy for IP Restriction**:  
   ```json
   {
     "Condition": {
       "IpAddress": {"aws:SourceIp": ["x.x.x.x/32"]}
     }
   }
   ```

9. **AMI (Amazon Machine Image)**:  
   EC2 instances ka template hota hai. Custom AMI banane ke liye EC2 instance ko configure karke snapshot lete hain.  

10. **AWS Monitoring**:  
    CloudWatch (metrics, logs), AWS Config (compliance), aur CloudTrail (API logging) use karte hain.  

---

### **Docker**  

11. **Docker vs VM**:  
    Docker containers host OS kernel share karte hain, lightweight hote hain. VMs pure OS virtualize karte hain, heavy hote hain.  

12. **Image vs Container**:  
    Image read-only template hota hai. Container us image ka running instance hota hai.  

13. **Dockerfile Banana**:  
    ```dockerfile
    FROM alpine:latest
    COPY app /app
    CMD ["/app/start.sh"]
    ```

14. **Data Persistence**:  
    Docker volumes (`docker volume create`) ya bind mounts (`-v /host/path:/container/path`) use karte hain.  

15. **Docker Compose**:  
    Multi-container apps ko `docker-compose.yml` mein define karte hain aur `docker-compose up` se run karte hain.  

16. **Docker Volume**:  
    Persistent storage jo container ke delete hone ke baad bhi survive karta hai.  

17. **Optimize Docker Images**:  
    Multi-stage builds, Alpine-based images, aur `.dockerignore` file use karke size kam karte hain.  

18. **Running Containers Check/Stop**:  
    `docker ps` se dekh sakte hain, `docker stop <container-id>` se stop karte hain.  

19. **Running Container Access**:  
    `docker exec -it <container-id> /bin/bash` se container ke andar access kar sakte hain.  

20. **Dockerfile Best Practices**:  
    Official images use kare, non-root user banaye, aur layers ko optimize kare.  

---

### **Jenkins**  

21. **Jenkins Kya Hai?**:  
    Open-source CI/CD tool jo automated builds, tests, aur deployments manage karta hai.  

22. **Freestyle vs Pipeline**:  
    Freestyle simple GUI-based jobs hote hain. Pipeline Jenkinsfile mein code se define hota hai aur complex workflows ko handle karta hai.  

23. **Jenkinsfile Example**:  
    ```groovy
    pipeline {
      agent any
      stages {
        stage('Build') { steps { sh 'make' } }
      }
    }
    ```

24. **Jenkins + GitHub Integration**:  
    GitHub webhooks ya "Poll SCM" use karke automatic builds trigger kar sakte hain.  

25. **Auto-Trigger Builds**:  
    GitHub mein webhook set karke Jenkins ko notify kar sakte hain ki naya code push hua hai.  

26. **Jenkins Agent vs Master**:  
    Master jobs ko schedule karta hai. Agent jobs ko execute karta hai (distributed workloads).  

27. **Credentials in Jenkins**:  
    Jenkins Credentials Manager mein SSH keys, API tokens, etc. securely store kiye jaate hain.  

28. **AWS Deployment from Jenkins**:  
    AWS CLI ya plugins (CodeDeploy) use karke Jenkins se AWS mein deploy karte hain.  

29. **Parameterized Builds**:  
    Build-time variables (e.g., `BRANCH`) pass kiye jaate hain.  

30. **Archive Artifacts**:  
    Jenkinsfile mein `archiveArtifacts` step use karke build outputs store kiye jaate hain.  

---

### **CI/CD Concepts**  

31. **Continuous Integration**:  
    Developers frequently code merge karte hain aur automated builds/tests run hote hain.  

32. **Continuous Deployment**:  
    CI pass hone ke baad code automatically production mein deploy ho jata hai.  

33. **CI/CD Benefits**:  
    Faster releases, fewer bugs, aur easy rollbacks possible hote hain.  

34. **Rollback Strategy**:  
    Blue-green deployment ya Terraform `plan` se changes verify karke rollback karte hain.  

35. **Blue-Green Deployment**:  
    Two identical environments (blue = live, green = new). Traffic switch karke zero-downtime deployments achieve karte hain.  

36. **Canary Deployment**:  
    New version ko small user base pe test karke gradually roll out karte hain.  

37. **CI/CD Tools**:  
    Jenkins, GitHub Actions, GitLab CI, CircleCI, etc.  

38. **Version Control in CI/CD**:  
    Git repository source of truth hota hai, jisse traceability aur rollback possible hota hai.  

39. **Secrets Management**:  
    HashiCorp Vault, AWS Secrets Manager, ya encrypted environment variables use karte hain.  

40. **CI/CD Stages**:  
    Build → Test → Deploy → Monitor.  

---

### **Terraform**  

41. **Terraform Kya Hai?**:  
    Infrastructure as Code (IaC) tool jo cloud resources declaratively manage karta hai.  

42. **Terraform vs CloudFormation**:  
    Terraform multi-cloud support karta hai (HCL syntax). CloudFormation AWS-specific hai (JSON/YAML).  

43. **Providers in Terraform**:  
    Plugins jo AWS, Google, Azure, etc. APIs se interact karte hain.  

44. **terraform init**:  
    Backend initialize karta hai aur providers/modules download karta hai.  

45. **Terraform Modules**:  
    Reusable Terraform configurations (e.g., VPC module).  

46. **Multiple Environments**:  
    Workspaces ya separate directories (`dev/`, `prod/`) use karke manage karte hain.  

47. **Terraform State File**:  
    Tracks real-world resources. Remote backend (S3) use karke team collaboration improve karte hain.  

48. **State Best Practices**:  
    Remote backend, state locking, aur manual edits avoid kare.  

49. **terraform plan**:  
    Changes preview karke validate karta hai before applying.  

50. **Terraform Secrets**:  
    `sensitive = true` mark kare ya HashiCorp Vault integrate kare.  

---

### **Git & GitHub**  

51. **Git vs GitHub**:  
    Git version control system hai. GitHub Git repositories ka cloud-based hosting platform hai.  

52. **git pull vs git fetch**:  
    `git fetch` remote changes download karta hai. `git pull` fetch + merge karta hai.  

53. **Merge Conflicts**:  
    Conflicted files edit karke `git add` aur `git commit` kare.  

54. **Pull Request**:  
    Code review process before merging into main branch.  

55. **Revert Commit**:  
    `git revert <commit-hash` se undo commit create hota hai.  

56. **Rebase vs Merge**:  
    Rebase linear history banata hai. Merge branch history preserve karta hai.  

57. **Create/Switch Branches**:  
    `git checkout -b new-branch` (create), `git checkout main` (switch).  

58. **.gitignore**:  
    Files (e.g., `node_modules/`) jo Git ignore karega.  

59. **Squash Commits**:  
    `git rebase -i HEAD~3` se multiple commits ko combine kare.  

60. **Git Tags**:  
    Releases mark karne ke liye (`git tag v1.0`, `git push --tags`).  

---

### **Real-Time Scenarios**  

61. **CI/CD Pipeline**:  
    GitHub → Jenkins → Docker → ECS pipeline banaya. Terraform se AWS infrastructure manage kiya.  

62. **Failed Deployment**:  
    Rollback script ya blue-green switch se previous stable version restore kiya.  

63. **Container Health Monitoring**:  
    Docker health checks, Prometheus, aur Grafana use karke monitor kiya.  

64. **Failed Jenkins Build Debug**:  
    Console logs check kiya aur `Jenkinsfile` mein syntax error fix kiya.  

65. **Slow Terraform Apply**:  
    `-parallelism` limit kiya aur modules ko optimize kiya.  

66. **EC2 Issue**:  
    High CPU usage `top` se debug kiya aur runaway process kill kiya.  

67. **Secure S3 Bucket**:  
    Bucket policy, encryption, aur access logs enable karke secure kiya.  

68. **Docker Multi-Stage Build**:  
    Final image size optimize karne ke liye multi-stage build use kiya.  

69. **Infrastructure Drift**:  
    Regular `terraform plan` aur Git diffs se changes track kiye.  

70. **VPC Setup**:  
    Public subnets (IGW) aur private subnets (NAT) ke saath VPC banaya.  

---

### **Scripting & Automation**  

71. **AWS CLI Backups**:  
    ```bash
    aws s3 sync /data s3://my-bucket/backups --delete
    ```

72. **Bash Deployment Script**:  
    ```bash
    #!/bin/bash
    docker build -t my-app .
    docker push my-registry/my-app
    ```

73. **Cron Jobs**:  
    `crontab -e` se schedule set kare (e.g., `0 3 * * * /backup.sh`).  

74. **Scripting Languages**:  
    Bash (quick tasks), Python (complex automation).  

75. **Monitor Cron Jobs**:  
    Logs (`/var/log/cron`) aur Slack alerts setup kare.  

76. **Bash Error**:  
    `unbound variable` error `set -u` se avoid kiya.  

77. **Disk Usage Script**:  
    ```bash
    df -h | grep -vE 'tmpfs|udev'
    ```

78. **Log Cleanup**:  
    ```bash
    find /logs -type f -mtime +7 -delete
    ```

79. **Service Health Check**:  
    ```bash
    curl -sSf http://localhost:8080/health || exit 1
    ```

80. **Script Alerts**:  
    `curl` ya `mail` command se Slack/Email alerts bheje.  

---

### **DevOps Culture**  

81. **Infrastructure as Code (IaC)**:  
    Terraform/CloudFormation se infrastructure code se manage karte hain.  

82. **DevOps in Team**:  
    CI/CD, automation, aur blameless postmortems practice karte hain.  

83. **Agile/Scrum**:  
    Daily standups, sprints, aur retrospectives follow karte hain.  

84. **Postmortems**:  
    Root cause analysis aur preventive actions document karte hain.  

85. **Monitoring Tools**:  
    Prometheus, Grafana, CloudWatch, ELK stack.  

86. **Observability**:  
    Logs, metrics, traces se system behavior samajhna.  

87. **Zero-Downtime Deployments**:  
    Blue-green, canary, aur health checks use karke.  

88. **Collaborate with Devs**:  
    Code reviews, pair programming, aur shared documentation.  

89. **Shift-Left Testing**:  
    Development phase mein hi testing start karna.  

90. **Code Quality in CI/CD**:  
    SonarQube, linters, aur unit tests enforce kare.  

---

### **Advanced Topics**  

91. **Vertical vs Horizontal Scaling**:  
    Vertical: Bigger servers. Horizontal: More servers.  

92. **Serverless**:  
    Lambda, FaaS, no server management, pay-per-use.  

93. **Container Orchestration**:  
    Kubernetes, ECS – containers ko manage karna.  

94. **AWS Secrets Management**:  
    Secrets Manager, Parameter Store, aur KMS use kare.  

95. **Elastic IP**:  
    Static public IP jo EC2 instances ko assign kar sakte hain.  

96. **Bastion Host**:  
    Secure jump server for accessing private instances.  

97. **CloudWatch**:  
    Metrics, logs, alarms, aur dashboards for monitoring.  

98. **Dead-Letter Queue (DLQ)**:  
    Failed SQS messages ka backup queue.  

99. **Shared Responsibility Model**:  
    AWS infrastructure secure karega, aap apna data/app secure kare.  

100. **Fault Tolerance vs High Availability**:  
     Fault Tolerance: Failures handle karna. High Availability: Minimal downtime.  

--- 

**Final Tip**:  
- **STAR Method** (Situation, Task, Action, Result) use karke real examples dijiye.  
- **Security** hamesha mention kare (e.g., "S3 encryption enable kiya").  
- **Numbers** add kare (e.g., "Deployment time 50% reduce kiya").  

Koi aur detail chahiye toh pooch sakte hain! 🚀
