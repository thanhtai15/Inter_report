---
title: "Blog 1"
date: 2024-09-09
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# European Region Announcement for Amazon Q Developer

**By Brian Beach | April 14, 2025 | in Amazon Q Developer, Announcements, Regions**

As I sit down to write this post, my daughter just called from the top of the Eiffel Tower during her senior class trip. While she excitedly points her camera toward the Paris skyline, I suddenly realize how technology has changed our concept of distance. Her world, at eighteen, is infinitely more connected than the world I knew at her age. I can't help but smile at the timing of this call, because today Amazon Q Developer is expanding to Europe.

The launch of Amazon Q Developer Pro Tier in the Frankfurt region (eu-central-1) marks an important milestone for our European customers, addressing two critical needs: data residency and performance optimization. For organizations that need to meet EU data residency requirements, the ability to store customer content within EU boundaries can help provide the assurances they require. Beyond compliance, the presence in this region also brings performance benefits. European customers will experience reduced latency in their interactions with Amazon Q Developer, as requests are processed closer to home. This proximity not only improves response times but also enhances the overall development experience, making real-time interactions with Amazon Q Developer more fluid and natural.

Amazon Q Developer Pro tier users now have the choice to create profiles in N. Virginia (us-east-1) or Frankfurt (eu-central-1). Your content, including customizations, is stored in this region. Although your content is stored in Frankfurt, Amazon Q still uses multi-region inference to optimize request processing. At launch, this includes Frankfurt, Ireland, Paris, and Stockholm, as shown in the image below.

![Amazon Q Developer Regions](/images/3-Blog/Blog1.png)

---

## Multi-Region Request Processing

Finally, it's important to note that certain operations, such as querying AWS resources in other regions (e.g., "List my S3 buckets in Tokyo"), will naturally involve multi-region calls regardless of where your Q Developer profile is located.

The Frankfurt region includes all GA features except command line and the ability to chat with Support. You can read more in the Amazon Q Developer User Guide.

---

## Conclusion

We invite you to experience these new capabilities by upgrading to the Pro tier and selecting Frankfurt as your region during profile creation. Get started with Amazon Q Developer, and share your feedback with us as we continue to expand our global presence.
