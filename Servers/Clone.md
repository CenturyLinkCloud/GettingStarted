{{{
  "title": "Clone",
  "date": "03-05-2015",
  "author": "Rich DuBose",
  "attachments": [],
  "related_products": [],
  "related_questions": [],
  "preview" : "",
  "contentIsHTML": false
}}}

Clones created for a variety of reasons including standardization, availability across platforms, & to create a baseline from which future virtual machines could be generated. Compatibility with the original system is usually the explicit purpose of cloning VM’s. Once you are satisfied with your server original server, this guide will walk you through the process of cloning your existing server.

**Navigate to the Status Page for the Server you wish to clone**

Once you are on the Status Page for the server you wish to clone, click on the ‘action’ menu option.  From the list, select ‘clone’.

**You are now on the Clone Server Page.**
The cloning process is very similar to the steps taken to create your original server.  However the Data Center, Operating System & Server Resources options have been removed.  The origin servers resources will be applied to the cloned server.

Complete the basic information by giving the new server a Name, Description & Root Password.

**Network**

Select the account network, primary DNS and secondary DNS for this server. Accounts can have multiple networks within a particular data center.

**Server Lifespan (Time To Live) (Optional)**

We recognize that sometimes server lifespans should coincide with a project lifespan, so we offer an optional time-to-live that allows you to schedule when the server should automatically be deleted. Setting a time to live results in a new Scheduled Task added to the server. If you need to extend the life of the server, this scheduled task can be changed after the server is provisioned.

**Queue The Server Build**

Confirm your server settings, then select the clone server button to queue the server build. Once the server is built, it will appear in the group that you selected it be placed. Congratulations, you’ve successfully built a new virtual server on the CenturyLink Cloud!




 
