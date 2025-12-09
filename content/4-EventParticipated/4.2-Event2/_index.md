---
title: "Event 2"
date: 2024-09-09
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# GenAI-powered App-DB Modernization Workshop & DevOps on AWS Workshop Takeaway

### 1. PURPOSE OF THE EVENT

This combined event aims to **share DevOps culture and principles** along with best practices on the AWS platform. Additionally, the workshop provides an opportunity for learners to **access Cloud and AI platforms**.

**Context and Importance:**
- Legacy physical machines, virtual machines, and old servers in enterprises **cannot support AI technology chips**
- Businesses are focusing on investing in Cloud to support AI technology
- Opens up great opportunities for young people in Cloud and AI fields

**The workshop aims to equip knowledge about:**
1. **Core DevOps performance metrics:**
   - DORA (DevOps Research and Assessment)
   - MTTR (Mean Time to Resolution)
   - Deployment Frequency

2. **Deploying modern technologies on AWS:**
   - Continuous Integration/Continuous Deployment (CI/CD)
   - Infrastructure as Code (IaC)
   - Monitoring & Observability

3. **Building a solid foundation:**
   - AI and Cloud
   - Leveraging great opportunities in the future

---

### 2. SPEAKER LIST

Main speakers sharing content include:

**Lam Thu Kiet** - Senior DevOps Engineer at FPT Software
- Shared experience in banking domain
- Practical chatbot deployment
- Shared about DevOps processes in enterprise environment

**Danh Hoang Hieu Nghi** - AI Engineer at Renob (AWS partner company)
- Shared experience deploying real-world AI applications
- Guided best practices in AI deployment

**Linh Lan Hoang Anh** - Senior student
- Shared perspectives on the latest AWS AI services
- Especially services beyond Bedrock/SageMaker

---

### 3. HIGHLIGHTED CONTENT

The workshop's highlighted content includes main parts about **DevOps on AWS** and **core AI techniques**.

#### A. DevOps Mindset and Principles

**DevOps Spirit:**
- Sharing DevOps culture and principles
- Benefits and key metrics:
  - **DORA** (DevOps Research and Assessment)
  - **MTTR** (Mean Time to Resolution)
  - Deployment Frequency
  - Change Failure Rate

#### B. CI/CD Pipeline on AWS

**1. Source Control:**
- Using **AWS CodeCommit**
- Git strategies:
  - GitFlow
  - Trunk-based development

**2. Build & Test:**
- Configuring **CodeBuild**
- Automated testing
- Build optimization

**3. Deployment:**
- Using **CodeDeploy** with deployment strategies:
  - **Blue/Green**: Parallel deployment, fast switching
  - **Canary**: Gradual deployment, risk reduction
  - **Rolling updates**: Sequential updates

**4. Orchestration:**
- Pipeline automation with **CodePipeline**
- Workflow automation
- Multi-stage deployment

#### C. Infrastructure as Code (IaC)

**AWS CloudFormation:**
- Template-based infrastructure
- Stack management

**AWS CDK (Cloud Development Kit):**
- Multi-language support (TypeScript, Python, Java, C#)
- Reusable patterns
- Type-safe infrastructure

#### D. Monitoring & Observability

**CloudWatch:**
- Metrics collection
- Logs aggregation
- Alarms configuration
- Dashboards visualization

**AWS X-Ray:**
- Distributed tracing analysis
- Performance bottleneck detection
- Full-stack observability

#### E. Foundation Models (FM)

**Foundation Models Characteristics:**
- Trained on very large datasets with **billions of parameters**
- Uses **self-supervised learning**
- **Differences from traditional ML:**
  - Traditional ML: Only handles one specific task
  - FM: Can handle broader tasks and generalize multiple tasks with just one prompt

#### F. Prompting Techniques

**1. Zero-shot:**
- Basic instruction only
- No examples needed

**2. Few-shot:**
- Provides context and examples
- Refines model output

**3. Chain of Thought (CoT):**
- **Foundation technique** helping LLM break down questions
- Step-by-step reasoning for more accurate results
- **Foundation for AI Agent operation**

#### G. Retrieval-Augmented Generation (RAG)

**RAG** - Model adopted by many companies

**Three operational steps:**
1. **Retrieval**: Retrieve internal information from knowledge space
2. **Argumentation**: Combine information with user question
3. **Generation**: Generate answer

**Embedding Technology:**
- Converts text to N-dimensional vector space
- Helps machine learning understand sentences
- Example: Amazon Titan Embedding

#### H. Amazon Bedrock Agent Core

**Essential framework for deploying and scaling AI applications**

**Solves complex problems:**

1. **Memory Management:**
   - Helps AI remember user context
   - Maintains context across multiple sessions

2. **Identity:**
   - Authorization
   - User management

3. **Tool Calling:**
   - Automates actions
   - Calls internal APIs
   - Uses browser tool to interact with web browsers

#### I. AWS Pre-trained AI Services

**Pre-trained AI Services** - Accessible via API only:

**1. Amazon Recognition**
- Computer Vision

**2. Amazon Translate**
- Natural language translation
- Different from query-based translation

**3. Amazon Transcribe**
- Speech-to-text conversion
- Supports streaming
- Multi-speaker recognition

**4. Amazon Polly**
- Text-to-speech conversion
- Text-to-speech for call centers

**5. Amazon Comprehend**
- Natural Language Processing (NLP)
- Sentiment analysis
- Sensitive information detection

**6. Amazon Kendra**
- Enterprise search
- Supports semantic search
- Supports RAG in internal documents

---

### 4. LESSONS LEARNED

#### Comprehensive DevOps Process
- Mastered components of **CI/CD pipeline on AWS**
- Understand advanced deployment strategies:
  - Blue/Green deployment
  - Canary deployment
  - Rolling updates

#### Product Evaluation Criteria
- For a product to be considered **"passed"** (to get points):
  - Must be a **"working product"** not just on paper
  - Complete approximately **5 to 6 features** out of 10 proposed features
- Example: E-commerce website must:
  - Display products
  - Add to cart
  - Complete payment

#### Infrastructure Modernization Mindset
- Clearly recognize that businesses are focusing on investing in Cloud
- Legacy systems don't support AI chips
- **This opens up great opportunities for young people**

#### AI Cost Optimization
- Need to optimize phrasing and refine keywords in prompting
- Avoid verbosity, reduce input tokens
- Save computation costs of LLM models

#### AI Reasoning Capability
- **CoT is an important technique** helping LLM reason
- Deliver more accurate results
- **Foundation for complex AI Agent tasks**

---

### 5. APPLICATION TO WORK

#### A. CI/CD Integration

**Automated deployment process:**
- Apply **CodePipeline** and related services
- Automate deployment process
- Use strategies like **Blue/Green** to minimize downtime

**Benefits:**
- Increase delivery speed
- Reduce human error
- Improve quality assurance

#### B. Incident Management

**Incident Management:**
- Apply incident management processes
- Postmortem reporting
- Continuous improvement in DevOps environment

#### C. Developing Scalable AI Products

**Transition from Local to Production:**
1. Use **Bedrock Agent Core**
2. Transform AI applications from localhost to multi-user systems
3. Ensure management of:
   - **Memory** (context retention)
   - **Identity** (authorization)
   - **Tool calling** (API integration)

#### D. Building Professional Portfolio

**Portfolio Development:**
- Complete products meeting **"working"** standards
- Include in portfolio and CV
- Increase internship or job opportunities

---

### 6. EVENT EXPERIENCE

#### CI/CD and Observability Demo
- Watched **live demo** of complete CI/CD pipeline deployment
- Full-stack observability setup
- Understand how components interact

#### Bedrock Agent Core Browser Tool
- Introduced and saw demo of Bedrock Agent Core usage
- **Browser tool** for automating actions on web browsers
- Witnessed powerful AI automation capabilities

#### Expert Interaction
- Had opportunities to **interact with experts**
- Real-world experience in banking domain
- Chatbot deployment in production environment

#### Career Roadmap
- Understand DevOps career paths
- AWS certification roadmap
- Career guidance from senior engineers

#### Pre-trained AI Services
- Understand how to use AWS pre-trained AI services
- Examples: Translate, Transcribe, Polly, Kendra
- Solve specific problems **without training models from scratch**

---

### 7. KEY TAKEAWAYS

#### 1. Product Quality in Practice
- **Technology products must be working products**
- Complete proposed core features
- Not just stopping at design or documentation

#### 2. Prompting Optimization
- Optimizing phrasing and keywords is **very important**
- Reduce token costs
- Improve response quality from Large Language Models (LLM)

#### 3. RAG as Knowledge Integration Solution
- RAG model is an effective solution
- Integrates **Foundation Model** with enterprise internal knowledge
- Through **Embedding** process

#### 4. DevOps Requires Synchronization
- Success in DevOps is not just using tools
- Need to apply **appropriate culture and principles**
- Use tools like CloudWatch/X-Ray to maintain system observability

---

### 8. CONCLUSION AND ASSESSMENT

The **"GenAI-powered App-DB Modernization & DevOps on AWS"** workshop provided comprehensive insights into:
- Modern DevOps processes on AWS
- Generative AI technology and practical deployment
- Combination of DevOps and AI to build scalable products

#### Illustrative Comparison

> **Developing AI today is like building a city:**
>
> - Initially, you can build a **single house** (localhost application)
> - But if you want **thousands of people to use simultaneously** (scale)
> - You cannot just copy that house
> - But need a **management system**:
>   - Traffic (routing)
>   - Utilities (resources)
>   - Public security (security)
> - **Bedrock Agent Core** plays the role of this management system
> - Ensures everything runs smoothly and can scale

**This is an important foundation** helping students prepare for:
- Labor market in the AI era
- Careers in Cloud and DevOps fields
- Building modern technology products

#### Some event photos
*Add your event photos here*
