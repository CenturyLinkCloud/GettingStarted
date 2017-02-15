{{{
  "title": "Application Deployment with Cloud Application Manager",
  "date": "12-12-2016",
  "author": "",
  "attachments": [],
  "related_products": [],
  "related_questions": [],
  "preview" : "How to deploy any application using Cloud Application Manager",
  "thumbnail": "../images/cloud-application-manager-deploy-preview.png",
  "contentIsHTML": false
}}}

<iframe width="560" height="315" src="https://player.vimeo.com/video/135104898" frameborder="0" allowfullscreen></iframe>

This video shows how to quickly deploy a sample WordPress blog.

### Introduction

Cloud Application Manager is a scalable platform for deploying enterprise mission-critical applications across any cloud infrastructure &ndash; private, public or hosted. It provides interactive visualization to automate application provisioning, including configuration, deployment, scaling, updating and migration of applications in real-time. Cloud Application Manager manages both traditional and cloud-native applications provisioned on bare metal and virtual machines across any type of infrastructure.

### Log Into Cloud Application Manager

To get started with Cloud Application Manager, sign up for an account and register your cloud service (CenturyLink, AWS or Azure, for example) as a provider.

![Cloud Application Manager Login](../images/cloud-application-manager-dashboard.png)

### The Box Catalog

The Box catalog has many sample applications you can readily deploy, including WordPress.

![Cloud Application Manager Box Catalog](../images/cloud-application-manager-deploy-preview.png)

### Deploying WordPress

Here you can see that WordPress will install from a Chef recipe that uses Chef Solo to configure it.

![Cloud Application Manager WordPress Installation](../images/cloud-application-manager-wp-install.png)

Once you click Deploy, you can view the lifecycle of how the app installs and configures. It’s all detailed in the event scripts.

![Cloud Application Manager Event Script](../images/cloud-application-manager-event-scripts.png)

Select a cloud deployment policy. Cloud Application Manager automatically creates this policy, which includes all the infrastructure meta data required to deploy successfully in your cloud.

![Cloud Application Manager Deployment Policy](../images/cloud-application-manager-policy.png)

On the WordPress instance page, you can track the instance of the deployment and see the entire step-by-step history of how WordPress is installed and configured.

![Cloud Application Manager Instance Activity](../images/cloud-application-manager-instance-activity.png)

### Start Using Your App

Once completed, the you'll be alerted that WordPress has successfully deployed and is online. You can now browse to its endpoint and start using WordPress right away.

![Cloud Application Manager WordPress Endpoint](../images/cloud-application-manager-wp-endpoint.png)
