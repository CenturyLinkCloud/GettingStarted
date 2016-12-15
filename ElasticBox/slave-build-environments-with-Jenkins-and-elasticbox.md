{{{
  "title": "Launch Slave Build Environments with Jenkins and ElasticBox",
  "date": "12-12-2016",
  "attachments": [],
  "related_products": [],
  "related_questions": [],
  "preview" : "Launch slave build environments in any cloud with Jenkins and ElasticBox",
  "thumbnail": "../images/elasticbox-jenkins1.png",
  "contentIsHTML": false
}}}

<iframe width="560" height="315" src="https://player.vimeo.com/video/113452091" frameborder="0" allowfullscreen></iframe>

### Introduction

Ease the pain of setting up build environments for every cloud and every project by automating builds using Jenkins slaves powered by ElasticBox. This demo walks you through the process with a typical ticketing SaaS App based on JBoss.


### Define a JBoss Build Slave in ElasticBox

Start with a JBoss Box in ElasticBox that installs a ticketing app with runtime dependencies like Java, Maven and the JBoss app server, as well as installing a slave agent on the machine.

![ElasticBox Jenkins Automating Builds](../images/elasticbox-jenkins2.png)

To deploy the JBoss environment on any cloud, you can attach the deployment profiles for a variety of cloud providers, including CenturyLink, AWS, Google Cloud, Azure, vSphere, OpenStack, etc. This lets you migrate your workload to any cloud without rebuilding your environment. For this exercise, select **Google Cloud**.

![ElasticBox JBoss Deployment Profile](../images/elasticbox-jenkins3.png)

### Setup the Slave in Jenkins

Now go to Jenkins and log into ElasticBox with an **Authentication Token**.

![ElasticBox Jenkins Login](../images/elasticbox-jenkins4.png)

Select the JBoss slave box from the workspace. For **Deployment Profile**, select **Google Cloud**.

![ElasticBox JBoss Slave Box](../images/elasticbox-jenkins5.png)

Now you need to tell JBoss how to use the slave. Select the maximum and minimum number of instances, and give the slave a **Label** to use in build jobs.

![ElasticBox JBoss Slave Label](../images/elasticbox-jenkins6.png)

Then tell Jenkins how long to keep an idle slave alive, by setting a **Retention Time** of 30 days.

![ElasticBox JBoss Slave Retention](../images/elasticbox-jenkins7.png)

Finally, to create a test build job, select the slave by its Label.

![ElasticBox JBoss Slave Selection](../images/elasticbox-jenkins8.png)

Since Jenkins is going to build and test the ticketing app by pulling the latest code from a repository, you'll also need to specify the repo URL.

![ElasticBox Repo URL](../images/elasticbox-jenkins9.png)

Next, add build commands. In our example, we're asking Maven to package and build a JBoss app and then run functional tests.

![ElasticBox Build Commands](../images/elasticbox-jenkins10.png)

Save the job and watch it build.

![ElasticBox Watch Build](../images/elasticbox-jenkins11.png)

### Review the Build Logs from the Jenkins Console Output

Once we trigger the job, the build logs show the slave environments deployed through ElasticBox.

![ElasticBox Build Logs](../images/elasticbox-jenkins12.png)

At this point, the JBoss build environment is ready.

![ElasticBox JBoss Build Environment ready](../images/elasticbox-jenkins13.png)

The logs also show that Maven installed the ticketing app and ran tests on the slave machine successfully.

![ElasticBox Tests Successful](../images/elasticbox-jenkins14.png)

### Confirm the Build in ElasticBox

Now from ElasticBox, navigate to the Instance of the JBoss application and browse to its IP address.

![ElasticBox Instances: JBoss Build Environment](../images/elasticbox-jenkins15.png)


![ElasticBox Instances: JBoss App URL](../images/elasticbox-jenkins16.png)

That’s all there is to it.
