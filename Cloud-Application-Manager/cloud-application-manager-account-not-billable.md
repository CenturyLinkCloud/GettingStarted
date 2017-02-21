{{{
  "title": "Error When Alias is Not Billable",
  "date": "02-20-2017",
  "author": "Ben Swoboda",
  "attachments": [],
  "related_products": [],
  "related_questions": [],
  "preview" : "Error When CenturyLink Cloud Alias Selected in Cloud Application Manager Is Not Billable",
  "thumbnail": "../images/cloud-application-manager-billable1.png",
  "contentIsHTML": false
}}}

<iframe width="560" height="315" src="https://player.vimeo.com/video/204243772" frameborder="0" allowfullscreen></iframe>

### Introduction

CenturyLink Cloud does not currently sell Azure through [Cloud Application Manager](https://www.ctl.io/cloud-application-manager) to the following types of accounts:
* Resellers
* Internal accounts
* Demo accounts
* Sub-accounts of those categories listed above

### Non-Billable Accounts

The following error will appear if the CenturyLink Cloud account alias you provide is a reseller, internal, demo or sub-account, and is therefore designated "not billable."

![Cloud Application Manager Error: Account Not Billable](../images/cloud-application-manager-billable2.png)

Here's how you might arrive at this error message. After you log into Cloud Application Manager, click the **Provider** tab on the top toolbar.

![Cloud Application Manager Create New Provider](../images/cloud-application-manager-error3.png)

Then click **New Provider** on the left navigation bar.

Select **Azure Resource Manager** to build a customer account in the current Microsoft Azure. Note: this is the new Azure, not the classic Azure. The dialog box that appears will enable you to create a new Azure customer account. Add a name for the account and select the **Create a new Azure customer account** option.

![Cloud Application Manager New Provider Details](../images/cloud-application-manager-error4.png)

Click **Connect a CenturyLink Cloud Account** and enter your CLC account admin credentials. This ties Azure directly into the CenturyLink Cloud billing service.

![Connect New Provider to a CenturyLink Cloud Account](../images/cloud-application-manager-error5.png)

### The Exception Message

If the CenturyLink Cloud billing account is the wrong account type, the following error message will appear, indicating we're not permitted to offer the product to you.

"Thank you for your interest in integrated Azure. Our apologies, but we are not able to provide this functionality for your account. Please submit a support request if you would like us to review your situation in further detail."

If you send us a support request we will review your case.

![Cloud Application Manager Error: Account Not Billable](../images/cloud-application-manager-billable2.png)
