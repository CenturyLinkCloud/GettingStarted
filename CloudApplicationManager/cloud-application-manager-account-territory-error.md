{{{
  "title": "Error when Creating a Provider Outside Territory",
  "date": "02-20-2017",
  "author": "Ben Swoboda",
  "attachments": [],
  "related_products": [],
  "related_questions": [],
  "preview" : "Error when Creating a Provider in Cloud Application Manager Beyond the Authorized Account Territory",
  "thumbnail": "../images/cloud-application-manager-territory1.png",
  "contentIsHTML": false
}}}

<iframe width="560" height="315" src="https://player.vimeo.com/video/204243434" frameborder="0" allowfullscreen></iframe>

### Introduction

CenturyLink Cloud is contractually obligated to limit resale of Azure from within Cloud Application Manager to specific countries. This tutorial demonstrates the alert message that will display if the CenturyLink Cloud billing address linked to an admin account is outside the territory permitted by Microsoft.

### Billing Address Must Match Territory

The following error will appear if the CenturyLink Cloud billing address associated with the user and alias is outside the territory permitted by Microsoft.

![Cloud Application Manager Error: Outside of Territory](../cloud-application-manager-territory2.png)

Here's how you can arrive at this error message. After you log into Cloud Application Manager, click the **Provider** tab on the top toolbar.

![Cloud Application Manager Create New Provider](../cloud-application-manager-error3.png)

Then click **New Provider** on the left navigation bar.

Select **Azure Resource Manager** to build a customer account in the current Microsoft Azure. Note: this is the new Azure, not the classic Azure. The dialog box that appears will enable you to create a new Azure customer account. Add a name for the account and select the **Create a new Azure customer account** option.

![Cloud Application Manager New Provider Details](../cloud-application-manager-error4.png)

Click **Connect a CenturyLink Cloud Account** and enter your CLC account admin credentials. This ties Azure directly into the CenturyLink Cloud billing service.

![Connect New Provider to a CenturyLink Cloud Account](../cloud-application-manager-error5.png)

### The Exception Message

If the CenturyLink Cloud billing address associated with the user and alias is outside the territory given to us by Microsoft, you will see an error message letting you know we are not permitted to offer the product to you. If you send us a ticket we can review your case for you.

![Cloud Application Manager Error: Account Outside of Terrritory](../cloud-application-manager-territory2.png)
