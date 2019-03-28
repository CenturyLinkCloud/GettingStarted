{{{
  "title": "Launch Slave Build Environments with Jenkins and Cloud Application Manager",
  "date": "12-12-2016",
  "author": "",
  "attachments": [],
  "related_products": [],
  "related_questions": [],
  "preview" : "Launch slave build environments in any cloud with Jenkins and Cloud Application Manager",
  "thumbnail": "../images/cloud-application-manager-jenkins1.png",
  "contentIsHTML": false
}}}

<div class="no-pdf">
<iframe width="560" height="315" src="https://player.vimeo.com/video/113452091" frameborder="0" allowfullscreen></iframe>
</div>
### Introduction

Ease the pain of setting up build environments for every cloud and every project by automating builds using Jenkins slaves powered by Cloud Application Manager. This demo walks you through the process with a typical ticketing SaaS App based on JBoss.


### Define a JBoss Build Slave in Cloud Application Manager

Start with a JBoss Box in Cloud Application Manager that installs a ticketing app with runtime dependencies like Java, Maven and the JBoss app server, as well as installing a slave agent on the machine.

![Cloud Application Manager Jenkins Automating Builds](../images/cloud-application-manager-jenkins2.png)

To deploy the JBoss environment on any cloud, you can attach the deployment profiles for a variety of cloud providers, including CenturyLink, AWS, Google Cloud, Azure, vSphere, OpenStack, etc. This lets you migrate your workload to any cloud without rebuilding your environment. For this exercise, select **Google Cloud**.

![Cloud Application Manager JBoss Deployment Profile](../images/cloud-application-manager-jenkins3.png)

### Setup the Slave in Jenkins

Now go to Jenkins and log into Cloud Application Manager with an **Authentication Token**.

![Cloud Application Manager Jenkins Login](../images/cloud-application-manager-jenkins4.png)

Select the JBoss slave box from the workspace. For **Deployment Profile**, select **Google Cloud**.

![Cloud Application Manager JBoss Slave Box](../images/cloud-application-manager-jenkins5.png)

Now you need to tell JBoss how to use the slave. Select the maximum and minimum number of instances, and give the slave a **Label** to use in build jobs.

![Cloud Application Manager JBoss Slave Label](../images/cloud-application-manager-jenkins6.png)

Then tell Jenkins how long to keep an idle slave alive, by setting a **Retention Time** of 30 days.

![Cloud Application Manager JBoss Slave Retention](../images/cloud-application-manager-jenkins7.png)

Finally, to create a test build job, select the slave by its Label.

![Cloud Application Manager JBoss Slave Selection](../images/cloud-application-manager-jenkins8.png)

Since Jenkins is going to build and test the ticketing app by pulling the latest code from a repository, you'll also need to specify the repo URL.

![Cloud Application Manager Repo URL](../images/cloud-application-manager-jenkins9.png)

Next, add build commands. In our example, we're asking Maven to package and build a JBoss app and then run functional tests.

![Cloud Application Manager Build Commands](../images/cloud-application-manager-jenkins10.png)

Save the job and watch it build.

![Cloud Application Manager Watch Build](../images/cloud-application-manager-jenkins11.png)

### Review the Build Logs from the Jenkins Console Output

Once we trigger the job, the build logs show the slave environments deployed through Cloud Application Manager.

![Cloud Application Manager Build Logs](../images/cloud-application-manager-jenkins12.png)

At this point, the JBoss build environment is ready.

![Cloud Application Manager JBoss Build Environment ready](../images/cloud-application-manager-jenkins13.png)

The logs also show that Maven installed the ticketing app and ran tests on the slave machine successfully.

![Cloud Application Manager Tests Successful](../images/cloud-application-manager-jenkins14.png)

### Confirm the Build in Cloud Application Manager

Now from Cloud Application Manager, navigate to the Instance of the JBoss application and browse to its IP address.

![Cloud Application Manager Instances: JBoss Build Environment](../images/cloud-application-manager-jenkins15.png)


![Cloud Application Manager Instances: JBoss App URL](../images/cloud-application-manager-jenkins16.png)

That’s all there is to it.
