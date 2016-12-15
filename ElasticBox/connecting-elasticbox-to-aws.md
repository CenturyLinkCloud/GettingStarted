{{{
  "title": "Connecting Your AWS Account in ElasticBox",
  "date": "12-12-2016",
  "attachments": [],
  "related_products": [],
  "related_questions": [],
  "preview" : "Connecting Your AWS Account in ElasticBox",
  "thumbnail": "../images/elasticbox-provider4.png",
  "contentIsHTML": false
}}}

<iframe width="560" height="315" src="https://player.vimeo.com/video/126177639" frameborder="0" allowfullscreen></iframe>

### Introduction

You need to connect your cloud account before you can deploy workloads from ElasticBox. Here's a quick step-by-step demo of how to connect to an AWS account.

### Create Custom AWS Policy

First, you need to create a custom AWS policy. From within your AWS account, click on the **Services** tab at the top of the page. From the drop down, select **IAM** &msash; Amazon’s Identity and Access Management service.

![ElasticBox Select AWS IAM](../images/elasticbox-aws-iam.png)

From the IAM **Dashboard** menu, select **Policies**.

![ElasticBox AWS Create Policy Step 1](../images/elasticbox-aws-iam-policy1.png)

Select **Create Policy**. Next to **Create Your Own Policy**, click **Select**.

![ElasticBox AWS Create Policy Step 2](../images/elasticbox-aws-iam-policy2.png)

Give your policy a name, drop in your policy document and click **Validate Policy**. When the policy has been validated successfully, click **Create Policy**.

![ElasticBox AWS Create Policy Step 3](../images/elasticbox-aws-iam-policy3.png)

Your ElasticBox Policy has now been successfully created.

![ElasticBox AWS Create Policy Step 4](../images/elasticbox-aws-iam-policy.png)

### Create IAM Role and Attach Policy

From your **Services** Dashboard in AWS, select **Roles**.

![ElasticBox AWS New Role](../images/elasticbox-aws-iam-role1.png)

  * Click **Create a New Role**.
  * Set **Role Name**.
  * For **Role Type**, click on **Role for Cross-Account Access**.
  * Select the option **"Allows IAM users from a 3rd party AWS account to access this account.”**

![ElasticBox AWS Role Type](../images/elasticbox-aws-iam-role3.png)

In **Establish Trust**, enter your **Account ID** and an **External ID**.

![ElasticBox AWS Role Trust](../images/elasticbox-aws-iam-role4.png)

Now attach the new policy you just created to this role.

![ElasticBox AWS Attach Policy](../images/elasticbox-aws-iam-role5.png)

Review your newly defined role. If you're satisfied, click **Create Role** in the lower right hand corner.

![ElasticBox AWS Review Role](../images/elasticbox-aws-iam-role6.png)

From the list of **Roles**, select the role you just created.

![ElasticBox AWS Select Role](../images/elasticbox-aws-iam-role7.png)

On the **Role Summary** page, you can now see the **Role ARN** (Amazon Resource Name.) Make a note of this name, because you'll need it for the last part of this exercise.

### Register IAM Role in ElasticBox

From your workspace in ElasticBox, select the **Providers** tab. Then click **New Provider**.

![ElasticBox New Provider](../images/elasticbox-provider.png)

Select AWS from the cloud providers listed.

![ElasticBox New Provider](../images/elasticbox-provider2.png)

Give this **New Provider** a name. Then input your **Account Role ARN** that you just identified in AWS.

![ElasticBox New Provider ARN](../images/elasticbox-provider3.png)

### This is What Success Looks Like

You’re done! Click on the **Logs** or **Configuration** tabs to view your settings.

![ElasticBox New Provider Success](../images/elasticbox-provider4.png)
