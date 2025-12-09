---
title: "Blog 3"
date: 2024-09-09
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---

# Introducing Quick Start Experience for Amazon Q Developer Pro

**By Matt Laver | April 7, 2025 | in Amazon Q, Amazon Q Developer, Launch**

For software developers, development teams, and IT professionals, the Pro tier of Amazon Q Developer is recommended. The pro tier provides higher limits, enterprise-grade administration, analytics dashboards, code customizations, and IP indemnification. Additionally, the Amazon Q Developer Pro tier requires AWS IAM Identity Center. For most production deployments, an organization instance of IAM Identity Center is recommended. An organization instance supports identity-aware sessions which are required to use the pro tier in the AWS Console, in addition to the benefits outlined in the IAM Identity Center user guide.

However, what if your team wants to get started quickly to try out the Amazon Q Developer Pro Tier features in their IDE but there are barriers slowing you down, such as:

 You don''t have plans to adopt IAM Identity Center across your entire organization.

 You have an organization instance of IAM Identity Center, but you want to deploy Amazon Q Developer Pro for a separate group of users, different from the users in your organization instance.

 You don''t control the AWS Organization you''re operating in. For example, a third party controls the AWS organization that manages your AWS accounts and needs time to approve changes.

To address these situations, we recently announced a new, simplified two-step setup experience that makes it easier for teams looking to try out the features of Amazon Q Developer Pro in their Integrated Development Environment (IDE).

---

## Management Account and AWS IAM Identity Center

Before we dive into the quick start setup tour, let''s take a step back and consider AWS''s recommendation to use a multi-account setup to organize your workloads. You can see the benefits in the AWS whitepaper on Organizing Your AWS Environment Using Multiple Accounts and the recommended approach is to implement this using AWS Organizations. The management account is the AWS account you use to create your organization and this account should be kept minimal and secure, hosting only essential administrative tools like AWS Organizations setup and deploying single sign-on through IAM Identity Center.

IAM Identity Center is core to the Amazon Q Developer Pro setup. IAM Identity Center users can access AWS accounts and applications using their existing organizational credentials, without having to create and manage separate AWS accounts and passwords.

For example, IAM Identity Center can connect and automatically provision users from standards-based identity providers, including Microsoft Active Directory, Okta, Microsoft Entra ID, Google Workspace, or another supported identity provider (IdP) through Security Assertion Markup Language (SAML) 2.0 or OIDC.

![Amazon Q Developer Access Management](/images/3-Blog/Blog3-1.png)

**Figure 1**  Amazon Q Developer Access Management through AWS IAM Identity Center.

This is a great experience for developers as they only need to authorize their Q Developer session using the normal sign-in process through the Identity source already available in their enterprise. Administrators benefit from features like centralized access management, streamlined permission management, and advanced administrator capabilities to view Amazon Q user activity.

---

## Simplified Setup Experience for Amazon Q Developer Pro

The above approach to setting up IAM Identity Center in a management account is ideal but not always feasible, so we created a new getting started experience that makes it easier for teams looking to try out the features of Amazon Q Developer Pro in their Integrated Development Environment (IDE), starting with:

 A standalone account that is not part of an organization managed by AWS Organizations.

 A member account, not the management account, that is part of an AWS Organization but does not have organization-level users managed in IAM Identity Center.

For both standalone accounts and member accounts, there is a two-step process. The first step to set up Amazon Q Developer Pro starts by navigating to the Amazon Q console and selecting Get started:

![Amazon Q Console](/images/3-Blog/Blog3-2.png)

**Figure 2**  Amazon Q Console  Get started with Amazon Q.

The setup will guide you through creating your first user and activating the Amazon Q Developer Pro subscription in your account, this initial step also includes creating an account instance of IAM Identity Center and an AWS-managed Amazon Q Developer application instance. Detailed instructions are available in our documentation  Subscribing users to Amazon Q Developer Pro.

When complete, the first user can be seen in the Amazon Q subscription section:

![Amazon Q Subscription](/images/3-Blog/Blog3-3.png)

**Figure 3**  Amazon Q Subscription.

The second step is to subscribe additional team members to the account instance of IAM Identity Center and then subscribe them to Amazon Q Developer Pro through the Amazon Q console.

![IAM Identity Center Users](/images/3-Blog/Blog3-4.png)

**Figure 4**  IAM Identity Center Users.

Once users have successfully subscribed, they will receive an email with instructions on how to activate their Amazon Q Developer Pro subscription and start using the features.

Note that account instances of IAM Identity Center have limitations. For example, account instances do not support console access. (Users can still use Amazon Q in the console, they will just be subject to the monthly limits of the Free tier.) If you want to use Amazon Q Developer Pro in the console and other AWS sites, you must be a user in an organization instance of IAM Identity Center, in a management account.

At this point, it''s worth noting that IAM Identity Center can now be configured to change its identity source to a Federated Identity Provider (IdP), see our documentation pages on how to change your identity source.

---

## Cleanup

To clean up the resources created in this blog post, first delete the Amazon Q Developer Pro users by following our instructions:

 Unsubscribe users from Amazon Q Developer Pro

Second, delete the IAM Identity Center instance:

 Delete your IAM Identity Center instance

---

## Conclusion

Getting started with Amazon Q Developer Pro is now even easier with the new, simplified setup experience, you can experience pro features in your IDE, such as higher limits for advanced features like:

 Chat, debug code, add tests, and more in your integrated development environment (IDE).

 Speed up tasks with Amazon Q Developer agents for software development.

 Upgrade applications in a fraction of the time with Amazon Q Developer agent for code transformation.

Get started with the Amazon Q Developer User Guide on Subscribing users to Amazon Q Developer Pro.

Read more about how the community is using Amazon Q to code and build applications faster and easier with Amazon Q on community.aws and explore what we''re building with Amazon Q Developer here.

Note that while this post focuses on Amazon Q Developer Pro, developers can still get started at no cost and without an AWS account; Amazon Q Developer offers a perpetual Free tier with monthly limits available to users, see our user guide on the Amazon Q Developer Free tier.

---

## About the Author:

**Matt Laver**

Matt Laver is a Senior Specialist Solutions Architect at Amazon Web Services (AWS) with a focus on Developer Experience. He is passionate about helping customers find simple solutions to difficult problems.
