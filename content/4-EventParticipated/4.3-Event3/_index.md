---
title: "Event 3"
date: 2024-09-09
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Mastering AWS DevOps: CI/CD, IaC, and Containers 


### 1. EVENT INFORMATION

**Event Name:** Mastering AWS DevOps: CI/CD, IaC, and Containers

**Time and Location:**
- Date: Monday, November 17, 2025
- Time: 8:30 AM  5:00 PM
- Location: AWS

**Scope:** In-depth workshop on DevOps on the AWS platform, focusing on CI/CD, Infrastructure as Code, and Container technologies.

---

### 2. MAIN CONTENT AND KEY CONCEPTS

#### A. DevOps Mindset and Principles

**DevOps Definition:**
- DevOps is the **bridge between Development (Dev) and Operations (Ops)**
- Requires DevOps practitioners to understand both areas thoroughly
- **Solves the problem:** Why code runs on developer''s machine but fails on server

**Core Objectives:**
- **Automation** is the primary focus of DevOps
- Purpose: Minimize errors caused by human factors

**Key Metrics:**
1. **DORA** (DevOps Research and Assessment)
2. **MTTR** (Mean Time to Resolution)
3. **Deployment Frequency**

**Value of Metrics:**
- Tracking these metrics creates a **comprehensive picture** for stakeholders
- Helps them see the value of DevOps investment

---

#### B. CI/CD Pipeline on AWS

The workshop focuses on AWS core services for **Continuous Integration/Continuous Deployment (CI/CD)**.

**1. Source Control:**
- Using **AWS CodeCommit**
- Git strategies:
  - GitFlow
  - Trunk-based development

**2. Build & Test:**
- Configuring **CodeBuild**
- Building test pipelines
- **Important:** Not just building, but continuously testing code
- **Applied to AI:** Even AI-generated code requires testing

**3. Deployment:**
- Using **CodeDeploy** with advanced deployment strategies:
  - **Blue/Green**: Parallel deployment, fast switching
  - **Canary**: Gradual deployment, risk reduction
  - **Rolling updates**: Sequential updates

**4. Orchestration:**
- Automating the entire process with **AWS CodePipeline**

**Distinguishing CI, CD, and Continuous Deployment:**

**Continuous Integration (CI):**
- Dev team workflow process
- Includes:
  - Source code management
  - Authorization
  - Container building (e.g., Docker file)
  - Automated code scanning for quality and security checks

**Continuous Delivery (CD):**
- Automated product deployment process
- **Requires manual intervention** (approval button click)
- After passing testing stages

**Continuous Deployment:**
- **Fully automated** deployment process
- From code commit to production application
- **No manual intervention required**

---

#### C. Infrastructure as Code (IaC)

**What is IaC:**
- Using **code to deploy and manage infrastructure**

**Advantages of IaC:**

1. **Rapid Automation:**
   - Create hundreds of servers with just one template

2. **Consistency:**
   - Ensures configuration doesn''t drift

3. **Portable:**
   - Easy environment transition
   - Just move code to different environment

4. **Documentation:**
   - Code serves as documentation
   - Others can read and understand how infrastructure works

**Click Ops Problem:**
- Configuring by **"clicking" on console (Click Ops):**
  -  Great for learning services
  -  Inefficient in enterprise environment
- **Reasons:**
  - Slow
  - Error-prone
  - Lacks consistency

**Main IaC Tools:**

**1. AWS CloudFormation:**

**Basic Concepts:**
- Uses templates (recipes, menus) to define AWS resources
- Supports YAML or JSON

**Stack:**
- Collection of AWS resources deployed according to template

**Drift Detection:**
- Important feature that detects manual changes made on console (Click Ops)
- Changes not in template
- Ensures infrastructure always matches code

**2. AWS CDK (Cloud Development Kit):**

**Features:**
- Framework using familiar programming languages:
  - Python
  - TypeScript
  - Java
  - C#

**Constructs:**
- Basic building blocks
- Three levels:
  - **Level 1:** Close to CloudFormation (L1 constructs)
  - **Level 2:** High-level abstractions (L2 constructs)
  - **Level 3:** Ready-made architectural patterns

**Process:**
- CDK converts code to CloudFormation template
- Then deploys to AWS

**3. Terraform:**

**Features:**
- **Multi-cloud** IaC tool
- Can be used for:
  - AWS
  - Azure
  - GCP

**Language:**
- Uses **HCL (HashiCorp Configuration Language)**
- Considered easy to understand

**Terraform Plan:**
- Important feature
- Allows **preview of changes** that will occur
- Before applying to infrastructure
- Better control

---

#### D. Container Services and Monitoring

**Container Services:**

**Docker:**
- Basic containerization platform

**Microservices:**
- Distributed application architecture

**Amazon ECR (Elastic Container Registry):**
- Image storage

**Orchestration Services:**
- **Amazon ECS** (Elastic Container Service)
- **Amazon EKS** (Elastic Kubernetes Service)

**AWS App Runner:**
- Simplified container deployment solution
- Quick containerized application deployment

**Monitoring & Observability:**

**CloudWatch:**
- Metrics collection
- Log management
- Alarm configuration
- Dashboard creation

**AWS X-Ray:**
- Provides **distributed tracing** capability
- Understand service performance
- Analyze bottlenecks

**Importance of Monitoring:**
- Building monitoring system is essential
- Evaluate system performance
- Example: Website runs under 1 second, under 5 seconds
- Measure and improve user experience

---

### 3. BEST PRACTICES

#### A. T-shaped Skills

**T-shaped Model:**
- **Vertical (Depth):** Deep dive into specific area
  - Example: Linux, Docker
- **Horizontal (Breadth):** Expand general knowledge
  - Example: Kubernetes, AI application support

**Benefits:**
- Specialized in one field
- Capable of diverse work
- Good communication with other teams

#### B. Focus on Fundamentals

**Important Starting Point:**
- Should start from foundational knowledge:
  - **System Fundamental:** Understand systems, networking, OS
  - **Developer Fundamental:** Programming, algorithms, design patterns

**Why Important:**
- Strong foundation helps learn new technologies faster
- Deeper understanding of how tools work

#### C. Documentation

**Importance:**
- Record entire process, features, and structure
- Share knowledge within team
- **Avoid having to repeatedly explain** to other members

**Good Documentation Criteria:**
- Write clearly
- **Even non-technical people can understand**
- Include specific examples
- Update regularly

#### D. Practice

**Learning Principles:**
- **Avoid:** Watching tutorial videos and moving on
- **Should:** Practice hands-on

**Reasons:**
- Practice reveals many emerging problems
- Helps understand technology more deeply

**With AI-generated Code:**
- **Avoid:** Copying AI-generated code without understanding
- **Should:** Read and understand code, test thoroughly

#### E. Project Management

**During development (e.g., project work):**

**Use task management tools:**
- Jira
- Trello
- GitHub Projects

**Components to manage:**
- **Task breakdown:** Break work into small tasks
- **Backlog management:** List of work to be done
- **Future roadmap:** Long-term development plan

**Benefits:**
- Clear progress tracking
- Efficient work allocation
- Easy review and improvement

#### F. Soft Skills

**Importance:**
- Soft skills are **very important for technical people**
- Especially in DevOps role

**Communication Skills:**
- Ability to convey information clearly and understandably
- **DevOps acts as bridge between groups:**
  - Development team
  - Operations team
  - Business stakeholders

**Necessary Soft Skills:**
- Communication
- Collaboration
- Problem-solving
- Empathy
- Presentation

---

### 4. KEY TAKEAWAYS

#### 1. DevOps is Culture, Not Just Tools
- DevOps success requires:
  - Right mindset
  - Collaboration between teams
  - Automation and continuous improvement

#### 2. Infrastructure as Code is Mandatory
- Cannot rely on Click Ops in production environment
- IaC ensures:
  - Consistency
  - Reproducibility
  - Version control

#### 3. Automated Testing is Essential
- Even with AI-generated code, testing is needed
- CI/CD pipeline must include:
  - Unit tests
  - Integration tests
  - Security scans
  - Performance tests

#### 4. Monitoring is Continuous Process
- Not "set and forget"
- Need to:
  - Track metrics continuously
  - Analyze trends
  - Improve based on data

#### 5. T-shaped Skills Help Career Development
- Specialize in one field
- Expand diverse knowledge
- Increase value in job market

---

### 5. APPLICATION TO WORK

#### A. Build Complete CI/CD Pipeline
- Apply CodeCommit, CodeBuild, CodeDeploy, CodePipeline
- Implement automated testing
- Use Blue/Green or Canary deployment

#### B. Transition to Infrastructure as Code
- Start with CloudFormation or Terraform
- Document entire infrastructure
- Version control all IaC code

#### C. Containerize Applications
- Use Docker for containerization
- Deploy to ECS or EKS
- Implement proper logging and monitoring

#### D. Improve Observability
- Setup CloudWatch dashboards
- Implement X-Ray tracing
- Define meaningful alarms

#### E. Build Documentation Culture
- Document architecture decisions
- Write runbooks
- Share knowledge with team

---

### 6. CONCLUSION

The **"Mastering AWS DevOps: CI/CD, IaC, and Containers"** workshop provided comprehensive knowledge about:
- DevOps mindset and principles
- CI/CD implementation on AWS
- Infrastructure as Code with CloudFormation, CDK, Terraform
- Container orchestration and monitoring
- Best practices for DevOps engineers

**Key Highlight:**
> DevOps is not just about using tools or automation, but a **work culture** that requires collaboration between teams, thinking about automation and continuous improvement, along with good communication skills to bridge Development and Operations.

**This workshop is an important foundation** that helps:
- Understand modern DevOps practices
- Apply AWS services effectively
- Develop T-shaped skills
- Prepare for DevOps Engineer career

#### Some event photos
*Add your event photos here*
