---
layout: bt_wiki
title: Deployments Page
category: Cloudify Console
draft: false
abstract: Deployment Page Reference
weight: 135
aliases: /manager_webui/deployments-page/

terminology_link: reference-terminology.html
node_types_link: dsl-spec-node-types.html
relationships_link: dsl-spec-relationships.html
---

The default `Deployments` page displays the Deployments widget which provides a list of all deployments 
and enables you to create, update and delete deployments and execute workflows.

You can list only deployments created basing on specific blueprint by selecting 
the blueprint from Resource Filter widget below Create Deployment button. 

You can also use **Search** input inside Deployments widget to filter deployments list.

![Deployments Page]( /images/ui/ui-deployments-page.png )

Each deployment in the list includes details about the attached blueprint, when the deployment was created (if it was updated icon indicating that will be shown near creation date) and the nodes on which it is deployed. 

You can also quickly check status and logs of the last workflow executed on the deployment by hovering over the status icon in the top left corner of deployment. Depending on the type of the execution there are additional action buttons there.

The last execution staus is indicated as follows:

![Last Execution Status]( /images/ui/deploymentActions/last-execution-status.png ) 

* **Red** X cross - execution has failed
* **Yellow** spinner - execution is in progress (meaning that it is in one of the following states: pending, started, cancelling, force_cancelling, kill_cancelling)
* **Orange** ban sign - execution has been cancelled
* **Green** checkmark - execution has been completed


The status of the deployments' node instances is indicated as follows:

![Node Instance Statuses]( /images/ui/deploymentActions/node_statuses.png )

* **Blue:** The number of node instances that are not initialized
* **Yellow:** The number of node instances that are in active state (one of: initializing, creating, created, configuring, configured, starting, stopping, stopped and deleting)
* **Green:** The number of node instances that are started
* **Black:** The number of node instances that are deleted


## Creating a Deployment

1. Click **Create Deployment** button.
2. Enter a name for the deployment.
3. Select a blueprint from the dropdown list.
4. Specify the deployment inputs for the blueprint or use the defaults.
5. Click **Deploy**.

The deployment is added to the list.


## Deployment Details and Actions

When you click on a deployment in the list, a deployment-specific page opens that, by default, displays the following widgets. 

* Deployment Topology
* Deployment Nodes
* Deployment Inputs
* Deployment Outputs
* Deployment Executions
* Deployment Events/Logs with Events/Logs filter above
* Deployment Sources

You can also execute workflows, update or delete deployment from this page.

More about widgets listed above you can find in [Default Widgets Reference]({{< relref "working_with/console/widgets/_index.md" >}}).


### Execute a Workflow

Each of the actions are described in detail [here]({{< relref "working_with/workflows/built-in-workflows.md" >}}).

1. Click **Execute workflow**.
2. Click the action you want to perform (eg. Install, Uninstall, Scale, ...).
3. Provide values for workflow parameters. 
4. Click **Execute**.


### Updating a Deployment

1. Click **Update deployment**.
2. Select the blueprint for the updated deployment.
3. Select the inputs file for the blueprint or provide values for the inputs.
4. Set actions to be performed during the update or use defaults.  
5. Click **Update**.

For more information about updating a deployment, [click here]({{< relref "working_with/manager/update-deployment.md" >}}).

For more information about creating custom workflows, [click here]({{< relref "working_with/workflows/creating-your-own-workflow.md" >}}).


### Deleting a Deployment

1. Click **Delete deployment**.
2. When prompted to verify that you want to remove the deployment, click **Yes**.


