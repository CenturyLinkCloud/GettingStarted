{{{
  "title": "Connecting Your AWS Account in Cloud Application Manager",
  "date": "12-12-2016",
  "author": "",
  "attachments": [],
  "related_products": [],
  "related_questions": [],
  "preview" : "Connecting Your AWS Account in Cloud Application Manager",
  "thumbnail": "../images/cloud-application-manager-provider4.png",
  "contentIsHTML": false
}}}

<iframe width="560" height="315" src="https://player.vimeo.com/video/126177639" frameborder="0" allowfullscreen></iframe>

### Introduction

You need to connect your cloud account before you can deploy workloads from Cloud Application Manager. Here's a quick step-by-step demo of how to connect to an AWS account.

### Create Custom AWS Policy

First, you need to create a custom AWS policy. From within your AWS account, click on the **Services** tab at the top of the page. From the drop down, select **IAM** &mdash; Amazon’s Identity and Access Management service.

![Cloud Application Manager Select AWS IAM](../images/cloud-application-manager-aws-iam.png)

From the IAM **Dashboard** menu, select **Policies**.

![Cloud Application Manager AWS Create Policy Step 1](../images/cloud-application-manager-aws-iam-policy1.png)

Select **Create Policy**. Next to **Create Your Own Policy**, click **Select**.

![Cloud Application Manager AWS Create Policy Step 2](../images/cloud-application-manager-aws-iam-policy2.png)

Give your policy a name, drop in your policy document and click **Validate Policy**. When the policy has been validated successfully, click **Create Policy**.

![Cloud Application Manager AWS Create Policy Step 3](../images/cloud-application-manager-aws-iam-policy3.png)

Your Cloud Application Manager Policy has now been successfully created.

![Cloud Application Manager AWS Create Policy Step 4](../images/cloud-application-manager-aws-iam-policy.png)

### Create IAM Role and Attach Policy

From your **Services** Dashboard in AWS, select **Roles**.

![Cloud Application Manager AWS New Role](../images/cloud-application-manager-aws-iam-role1.png)

  * Click **Create a New Role**.
  * Set **Role Name**.
  * For **Role Type**, click on **Role for Cross-Account Access**.
  * Select the option **"Allows IAM users from a 3rd party AWS account to access this account.”**

![Cloud Application Manager AWS Role Type](../images/cloud-application-manager-aws-iam-role3.png)

In **Establish Trust**, enter your **Account ID** and an **External ID**.

![Cloud Application Manager AWS Role Trust](../images/cloud-application-manager-aws-iam-role4.png)

Now attach the new policy you just created to this role.

![Cloud Application Manager AWS Attach Policy](../images/cloud-application-manager-aws-iam-role5.png)

Review your newly defined role. If you're satisfied, click **Create Role** in the lower right hand corner.

![Cloud Application Manager AWS Review Role](../images/cloud-application-manager-aws-iam-role6.png)

From the list of **Roles**, select the role you just created.

![Cloud Application Manager AWS Select Role](../images/cloud-application-manager-aws-iam-role7.png)

On the **Role Summary** page, you can now see the **Role ARN** (Amazon Resource Name.) Make a note of this name, because you'll need it for the last part of this exercise.

### Register IAM Role in Cloud Application Manager

From your workspace in Cloud Application Manager, select the **Providers** tab. Then click **New Provider**.

![Cloud Application Manager New Provider](../images/cloud-application-manager-provider.png)

Select AWS from the cloud providers listed.

![Cloud Application Manager New Provider](../images/cloud-application-manager-provider2.png)

Give this **New Provider** a name. Then input your **Account Role ARN** that you just identified in AWS.

![Cloud Application Manager New Provider ARN](../images/cloud-application-manager-provider3.png)

### This is What Success Looks Like

You’re done! Click on the **Logs** or **Configuration** tabs to view your settings.

![Cloud Application Manager New Provider Success](../images/cloud-application-manager-provider4.png)
