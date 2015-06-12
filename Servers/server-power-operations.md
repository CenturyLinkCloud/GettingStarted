{{{
  "title": "Server Power Operations",
  "date": "04-09-2015",
  "author": "",
  "attachments": [],
  "related_products": [],
  "related_questions": [],
  "preview" : "Understand the differences between each power command for a server.",
  "thumbnail" : "../images/servers-power-ops-preview.png",
  "contentIsHTML": false
}}}

<iframe width="560" height="315" src="https://www.youtube.com/embed/ScVa998pY2s?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

### Introduction

Easily issue power commands against an individual server in the Control Portal.

![Server power operations on CenturyLink Cloud](../images/servers-power-ops.png)

### On

Applies to servers that are powered off. Initiates the operating system boot sequence. Billing charges for memory, CPU, and software licensing fees (if applicable) start accruing, and monitors are re-enabled.

### Shut Down

Initiates a graceful shutdown of the corresponding server or servers. Like the “off” power command, all memory and CPU charges cease, monitors are disabled, and the machine is left in a powered off state. Any licensing charges (if applicable) and storage charges continue accruing.

### Pause

When a server is paused, its state is frozen (e.g. memory, open applications) and monitoring ceases. Billing charges for CPU and memory stop. A paused machine can be quickly brought back to life by issuing the **On** power command. Any applicable licensing charges continue to accrue while a machine is paused.

### Reboot

Executes a graceful reboot of the target server or servers. Unlike the forced “reset” power command, this instructs the operating system to initiate a proper stop and restart.

### Power Off

Applies to This is a forced shutdown of a server. It’s the equivalent of unplugging a physical machine. All memory and CPU charges stop accruing, monitors are disabled, and the machine ends up in a powered off state. Any licensing charges (if applicable) and storage charges continue accruing. If the server is moved to archive storage, then any applicable licensing charges cease.

### Reset

Similar to the relationship between **Off** and **Stop OS**, the reset command is a forced power off + power on combination. It is equivalent to the reset button on a physical computer.

### Maintenance

This command puts a server or servers into maintenance mode which means that monitors are disabled.
