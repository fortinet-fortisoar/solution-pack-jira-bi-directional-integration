[Home](../README.md) |
|--------------------------------------------|

# Usage

This solution pack helps you to understand the steps FortiSOAR takes to respond to organisations that choose to keep SOC incident management on JIRA while utilising FortiSOAR's automation and orchestration capabilities. To discover how this solution bundle automation satisfies your needs, see the section [Jira](#jira).

# Jira

## Simulation Mode:

> **Note** Mark the global variable `Demo_mode` as `True` and mark all the playbook under collection **02-Use Case-jira** as `Active.`

The simulation mode has one sample data **Jira** that helps you get a better understanding of how the solution pack functions. Following steps help you use the solution pack with some included sample data.

- Browse to `Simulations` > `Jira` scenario and click **Simulate Scenario**.
- This scenario adds alert `Unable to log into VPN` as severity `Medium`.
- Open Alert module and execute playbook **Create Jira Ticket**. Specify `Jira Project Key` as in which you want to add this alert.
- Jira tickets are updated when the `Status`, `Severity`, or `Description` are changed.
- As soon as a comment or reply is added to an alert, Jira ticket data is synced.
- To sync the ticket status with the alert status, tigger **Jira: Sync Jira Ticket Status** playbook from Alert's `Execute`, entering the values for field `Jira Project KEY,` `Start At,` and `Max Result`.
- To delete all Jira ticket, trigger **Delete All Jira Tickets from Project** playbook from Alert's `Execute`, entering the values for field `Jira Project KEY,` `Start At,` and `Max Result`.

## Environment Mode:

> **Note** Mark the global variable `Demo_mode` as `False` and mark all the playbook under collection **02-Use Case-jira** as `Active.`

Solution pack contains playbook which helps in following ways:

* Using the playbook **Create Jira Ticket** on alert, you can generate a `Issue` in Jira with the same alert's `Severity,` `Status,` and `Description` by manually entering a value for the `Jira Project KEY.`
* The Post Update playbook **Update Jira Ticket** on alert enables an automated sync with Jira, allowing Jira **Issue** to be updated with the relevant changes made to the alert's `Severity,` `Status,` or `Description.` Playbook requires the value for key `jiraProjectKEY` in configuration step of playbook. 
* Playbook **Sync Alert Comment on Jira** is used to automatically update Jira **Issue** with comment whenever a new comment or reply is added to an alert.
* A manual trigger playbook **Jira: Sync Jira Ticket Status** is utilized to update alerts status as the corresponding **Issue** in Jira. Playbook requires the value for fields `Jira Project KEY,` `Start At, ` and `Max Result` on triggering the playbook.
* A manual trigger playbook **Jira: Delete All Jira Ticket** is implemented to delete all **Issue**(or ticket) associated with a specified project of Jira. Playbook requires the value for fields `Jira Project KEY,` `Start At, ` and `Max Result` on triggering the playbook.