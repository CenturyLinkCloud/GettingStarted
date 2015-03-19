{{{
  "title": "Create Custom Server",
  "date": "01-18-2015",
  "author": "Nathan Young",
  "attachments": [],
  "related_products": [],
  "related_questions": [],
  "preview" : "",
  "contentIsHTML": false
}}}

The heart of the CenturyLink Cloud is the ability to create and manage virtual infrastructure. This guide will demonstrate how to provision a new virtual server in the CenturyLink Cloud.

##Navigate to “Create Server”

There are two places to initiate this process. The first is from the top-most navigation menu under the Servers section.

The second place to trigger this process is from within the Servers UI. From the Servers page, select the New Server (+) icon. 

##Create Server Form: Provide Basic Server Information

From top to bottom, the Create Server page will walk you through the required feels in order to successfully provision a new virtual server.

Select a Data Center, Group, and Server Type ([Standard](http://www.centurylinkcloud.com/servers) or [Hyperscale](http://www.centurylinkcloud.com/hyperscale)) to deploy to. Then choose the operating system template for this server from any of the available Windows and Linux templates offered by CenturyLink Cloud. If you have created custom templates in your account, they will be available in this list as well.

##Define Server Resources

Specify CPU and memory allocation using the input box or slider. As resource values are changed, the estimated hourly and monthly prices will reflect those changes. Note, we can not foresee how you will utilize the server resource (for example, your server maybe powered off), this estimate isn’t a guarantee of actual costs, and is meant to provide a base level pricing transparency. If after a period of time you find that you need to increase or decrease resources, they can be changed after the server is provisioned. 

If you’ve selected an operating system that supports CPU Autoscale, and you have a already defined a CPU Autoscale Policy, that will be available for selection. CPU Autoscale makes it possible to scale servers vertically based on utilization, ensuring optimal deployment of resources for cloud environments under a variety of conditions.

Add storage disks to the server up to platform maximums based on server type. Storage disks can be expanded, added, and removed after the server is built. Choosing a Partition results in a formatted disk in the operating system. Raw Disk provides an unformatted volume.

Select a CPU Autoscale Policy making it possible to scale servers up and down based on utilization ensuring optimal deployment of resources for cloud environments under a variety of conditions.

For standard server types, select an appropriate backup level for your new virtual machine. WIth Hyperscale servers, there is no built in storage redundancy or snapshot capability. You are responsible for any storage backups for Hyperscale servers.

##Network

Select the account network, primary DNS and secondary DNS for this server. Accounts can have multiple networks within a particular data center.

##Server Lifespan (Time To Live)

We recognize that sometimes server lifespans should coincide with a project lifespan, so we offer an optional time-to-live that allows you to schedule when the server should automatically be deleted. Setting a time to live results in a new [Scheduled Task](http://www.centurylinkcloud.com/scheduling) added to the server. If you need to extend the life of the server, this scheduled task can be changed after the server is provisioned.

##Queue The Server Build

Confirm your server settings, then select the **create server** button to queue the server build. Once the server is built, it will appear in the group that you selected it be placed. Congratulations, you’ve successfully built a new virtual server on the CenturyLink Cloud!
