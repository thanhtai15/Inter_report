---
title: "Blog 2"
date: 2024-09-09
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---

# Combining Snyk Insights with Amazon Q Developer Support to Streamline Secure Development

**By Omar Faruk and David Schott | April 28, 2025 | in Amazon Q Developer, Developer Tools, Partner solutions, Security**

Today, developers face a constant balancing act  building new features and functionality while ensuring the security and reliability of their codebase. Two powerful tools, Snyk and Amazon Q Developer, can work in tandem to help developers navigate this challenge with greater efficiency and productivity.

Snyk is a leading developer security platform that empowers developers to seamlessly secure their code, open-source dependencies, container images, and cloud infrastructure, all from a single unified platform. Amazon Q Developer is a generative AI-powered assistant designed to accelerate various tasks throughout the software development lifecycle. By combining security insights from Snyk with Amazon Q Developer''s assistance capabilities, developers can streamline their workflows and focus on shipping products.

---

## Getting Started with Amazon Q Developer and Snyk IDE Plugins

To get started with Amazon Q Developer, you need to have an AWS Builder ID or be part of an organization with an AWS IAM Identity Center instance that enables you to use Amazon Q. To use Amazon Q Developer agents for software development in Visual Studio Code, start by installing the Amazon Q extension. Find the latest version of the extension on the Amazon Q Developer page. This extension is also available for JetBrains IDEs, Eclipse (Preview), and Visual Studio. For a detailed list of supported IDEs and features available in each IDE, refer to the Amazon Q Developer documentation.

To get started with Snyk, sign up for a free Snyk account or log in with your existing account. To use Snyk in your IDE to automatically find security issues, review the IDE documentation and install Snyk using your IDE''s extension marketplace. After Snyk is installed, navigate to the Snyk panel in your IDE and follow the on-screen instructions to authenticate with your Snyk account.

After authentication, Snyk will automatically scan your entire codebase for security issues. Snyk will continue to scan periodically as you write code or generate code using Amazon Q Developer.

---

## Walkthrough

Let''s explore how Snyk and Amazon Q Developer can be used together through a few examples. Imagine you''re maintaining an open-source project. As a new Snyk user, you want to find and fix security issues in the project. In this first, simple scenario, Snyk has identified multiple instances of security vulnerabilities in specific lines of code. Among the vulnerabilities, we''ll focus on the Information Exposure vulnerability.

![Snyk IDE Plugin](/images/3-Blog/Blog2-1.png)

**Figure 1**  Snyk IDE Plugin displaying vulnerability analysis of the Information Exposure issue, showing severity, affected code, and mitigation tips.

Instead of researching and implementing the fix yourself, you simply highlight the flagged line of code, invoke Amazon Q Developer''s inline chat by pressing +I (Mac) or Ctrl+I (Windows), and ask for assistance. Amazon Q Developer will analyze the issue, suggest necessary code changes, and provide you with an inline diff to review and accept. This enables quick remediation of security bugs, saving time while improving the code.

![Amazon Q Developer Inline Fix](/images/3-Blog/Blog2-2.png)

**Figure 2**  Triggering Amazon Q Developer''s inline code generation feature to fix the detected information exposure vulnerability.

We''re happy with the change Amazon Q Developer has suggested, so we simply press enter to accept the suggestions. Of course, we can always press escape to reject the suggestion if needed.

![Code Generation Process](/images/3-Blog/Blog2-3.png)

**Figure 3**  Amazon Q Developer displaying the inline code generation process to fix the detected information exposure vulnerability.

---

## Using the /dev Agent

Beyond inline chat, you can pass vulnerability details directly from the Snyk plugin''s Problems view to Amazon Q Developer''s /dev agent capability.

In Q Developer''s chat interface, the /dev agent capability allows for longer conversations, broader workspace context, and handling changes across multiple files and topics. When this workflow is invoked, the Amazon Q Developer Agent generates code based on the description and existing code in the workspace, provides a list of suggestions to review and add to the workspace, and if needed, iterates on code generation based on feedback.

![Dev Agent Project-wide Fixes](/images/3-Blog/Blog2-4.png)

**Figure 4**  Using Amazon Q''s /dev agent to implement project-wide fixes for vulnerabilities detected by Snyk across multiple files.

---

## Handling Complex Issues

Not all issues are as straightforward as the previous example. In a more complex case, Snyk may expose a vulnerability that requires deeper understanding of the code and potential risks. Let''s consider another issue that Snyk has identified in the project we''re discussing.

![Snyk XSS Vulnerability](/images/3-Blog/Blog2-5.png)

**Figure 5**  Snyk Plugin highlighting a cross-site scripting (XSS) vulnerability, showing affected code lines and mitigation recommendations.

Here, you can turn to Amazon Q Developer''s chat interface, provide details about the issue, and request a more thorough explanation. Amazon Q Developer can then dig deeper into the codebase, explain the issue in detail, and guide you on how to remediate it appropriately. This collaborative approach empowers developers to make informed decisions and gain broader knowledge, rather than simply executing a suggestion.

![Amazon Q Developer Chat Interface](/images/3-Blog/Blog2-6.png)

**Figure 6**  Amazon Q Developer''s chat interface explaining the XSS vulnerability and its security implications through natural language dialogue.

Note that Amazon Q Developer provides links to documentation and other resources for further reading. Additionally, you can continue the discussion to learn more. For example, imagine you want to understand real-world breaches that have occurred due to the issues Snyk identified. Q provides several examples for me to learn more.

![Real-world XSS Examples](/images/3-Blog/Blog2-7.png)

**Figure 7**  Amazon Q Developer discussing notable real-world XSS breach examples and their security impacts.

Beyond fixing issues, Amazon Q Developer can also assist with other development tasks identified by Snyk, such as updating dependencies, refactoring code, or optimizing cloud infrastructure. By integrating these two tools, developers can streamline security scanning, issue investigation, and remediation, thereby significantly increasing their overall productivity.

---

## Conclusion

In this blog post, we''ve explored how Snyk and Amazon Q Developer are a powerful duo in the modern developer''s toolkit. Integrating Snyk''s leading security insights with Amazon Q Developer''s generative AI capabilities empowers developers to identify, understand, and resolve security vulnerabilities more effectively. This combination allows developers to enhance their skills and improve their capabilities as they tackle security issues. Get started by installing Amazon Q Developer in your IDE and the Snyk plugin.

---

## Snyk  AWS Partner Spotlight

Snyk empowers developers worldwide to build secure applications and equips security teams to meet the demands of the digital world. Used by 1,200 customers globally, Snyk''s Developer Security Platform automatically integrates with developer workflows and is purpose-built for security teams to collaborate with their development teams.

---

## About the Authors:

**Omar Faruk**

Omar Faruk is a DevOps Partner Solutions Architect at Amazon Web Services. He helps DevSecOps partners design, build, and operate their workloads and those of mutual customers in AWS. He is passionate about CI/CD, Infrastructure as Code, and next-generation developer experience. Outside of work, he enjoys spending time with family and traveling.

**David Schott**

David is a seasoned DevSecOps Solutions Engineer with over 15 years of experience helping Fortune 100 companies optimize their security and software delivery efficiency. After driving DevOps adoption and CI development at CloudBees, he now focuses on DevSecOps at Snyk, where he collaborates with strategic partners to enable secure innovation at scale.
