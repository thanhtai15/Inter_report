---
title: "Event 1"
date: 2024-09-09
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---


# Summary Report: AWS AI/ML and Generative AI Workshop

### I. EVENT INFORMATION AND AGENDA

**Time:** Saturday, November 15, 2025, from 8:30 AM to 12:00 PM  
**Location:** AWS Vietnam Office

#### A. Program Summary

The program focused on introducing AWS machine learning and generative AI services:

**1. AWS AI/ML Services Overview (9:00  10:30 AM)**
- Detailed introduction to **Amazon SageMaker** - AWS end-to-end Machine Learning (ML) platform
- Content includes:
  - Data preparation and labeling
  - Model training and fine-tuning
  - Model deployment
  - Integrated MLOps capabilities
- **Live Demo**: SageMaker Studio

**2. Generative AI with Amazon Bedrock (10:45 AM  12:00 PM)**
- Focus on using Amazon Bedrock to deploy Generative AI
- Key topics:
  - Comparing and selecting Foundation Models (Claude, Llama, Titan)
  - Prompt Engineering techniques
    - Chain-of-Thought reasoning
    - Few-shot learning
  - Retrieval-Augmented Generation (RAG) architecture
  - Knowledge Base integration
  - Bedrock Agents for multi-step workflows
  - Guardrails for safety and content filtering

---

### II. AI-DRIVEN DEVELOPMENT LIFECYCLE (AIDLC) METHODOLOGY

AIDLC (AI-Driven Development) is a methodology and approach aimed at accelerating software development, with the ability to **reduce working time from two weeks to approximately 1.5 days**.

#### A. Human-Centric Philosophy

**No Autonomous Decisions:**
- The core philosophy of AIDLC is to **not allow AI to make any decisions replacing humans**

**Human Role:**
- Responsibilities of developers and stakeholders:
  - **Validation**
  - **Decisioning**
  - **Oversight**
- If AI raises questions to clarify requirements, humans must answer for AI to proceed

**Mandatory Plan Creation:**
- When requesting AI to perform any task, it **must create a plan first**
- Benefits:
  - Helps users know exactly what AI wants to do
  - Avoids context overload
- If the plan is inaccurate, request AI to create a new plan
- **Iteration is a crucial part** of the AIDLC methodology

#### B. Process and Context Management

**1. AIDLC Phases (Faces):**

- **Inception**: Initial phase
  - Define requirements
  - Break down into User Stories
  - Group User Stories into Units (Unit of Work)

- **Construction**: Building phase
  - Implement based on grouped Units

- **Operation**: Operating phase
  - Deploy
  - CI/CD

**2. Context Management:**

- **Language Priority:**
  - AI understands language context better than code
  - Instead of providing entire source code as input, extract information into:
    - Project summary
    - Technical architecture
    - Domain model
  - This helps AI understand better and avoids context overload

- **Use Separate Sessions:**
  - Create separate work sessions for each task (like each Unit)
  - Better context control
  - Minimize hallucination risks from previous task contexts

**3. Mob Development:**

- AIDLC proposes Mob Development method
- Multiple roles working together on the same computer:
  - BA (Business Analyst)
  - Engineer
  - Solution Architect
  - QA (Quality Assurance)
- Benefits:
  - Everyone validates output immediately
  - Increases speed and work efficiency

---

### III. AI-INTEGRATED TOOL: KIRO IDE

**Kiro** is AWS Integrated Development Environment (IDE), built to **integrate AI from the start**, similar to Coder or VS Code.

- Currently uses Large Language Models (LLMs) like **Claude** (e.g., Claude 3.4, 3.7, 4.5)

#### A. Spec-Driven Development (SDD)

**Core Feature:**
- SDD is a built-in feature in Kiro
- Users don't start with code but by creating **spec documents**

**Default Spec Files:**
- Kiro creates three basic files in the `.kiro` folder:
  - `requirement`
  - `design`
  - `task list`

**Limitations:**
- SDD is evaluated as rigid and difficult to scale for large projects
- More suitable for:
  - Small projects
  - Creating prototypes
- Due to fewer documents, allows AI more "space" for errors compared to detailed AIDLC process

#### B. AIDLC Integration in Kiro

- Kiro supports applying custom methodologies through **Advanced Context Management**
- Implementation:
  - Define AIDLC workflow in `steering` file
  - Place in `.kiro/steering` folder
  - Kiro will automatically run phases (faces) according to AIDLC process

#### C. Agent Hooks

- Kiro allows creating **Agent Hooks**, similar to webhooks but for AI Agents
- Functions:
  - Define rules using natural language
  - Example: "whenever JS file is saved, run unit test"
  - Automate tasks based on events
  - Allow main AI Agent to focus on core logic

---

### IV. LESSONS LEARNED AND RECOMMENDATIONS

#### 1. Prompting Mindset
- When requesting AI, clearly define AI's **role (persona)**
- **Input and Output must be clear**
- Output should be recorded in a specific file (like Markdown) rather than just stored in temporary memory

#### 2. Avoid Prohibitions
- **Instead of:** "don't do this" (don't implement this)
- **Say:** "implement this"
- Reason: High probability that AI will do prohibited things

#### 3. Importance of Developers
- Although AI supports rapid development, **developer value** still lies in:
  - Monitoring capability
  - Validation
  - Decision making
- Time spent on validation and oversight is **"well-deserved time"**

---

### V. ILLUSTRATIVE EXAMPLE

Using AIDLC and Kiro in software development is like controlling a **self-driving car (AI)** on a complex route:

- **You (the developer)** are the one who:
  - Provides detailed map (Plan)
  - Identifies important stops (Units)
  - Continuously checks if the car is going in the right direction (Validation)

- **You don't need to drive every meter**, but you are fully **responsible for every decision** on the road to ensure safe and efficient arrival at the destination.

---

### VI. CONCLUSION AND PERSONAL ASSESSMENT

The AWS AI/ML and Generative AI Workshop event provided extremely valuable knowledge about:
- How to responsibly apply AI to software development processes
- AIDLC methodology helps accelerate development while ensuring quality
- Kiro IDE tool with powerful AI integration capabilities

The most notable point is the **Human-Centric** philosophy - emphasizing that AI is a support tool, not a human replacement. This helps me better understand the role and responsibility of developers in the AI era.

#### Some event photos
*Add your event photos here*
