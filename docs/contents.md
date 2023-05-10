| [Home](../README.md) |
|----------------------|

# Contents

The **Bi-Directional Jira Sync** solution pack contains the following resources.

## Module Schema

| Name   | Description                                       |
|:-------|:--------------------------------------------------|
| Alerts | The alert module has a new field *Jira Ticket ID* |

> **NOTE**: This field can be added to the alert SVT.

## Connector

| Name | Description                                                           |
|:-----|:----------------------------------------------------------------------|
| Jira | Jira Service Desk Connector for issue creating, updating, and deleting |

## Playbook Collection

|02 - Use Case - JIRA|
|:-------------------|

| Playbook Name                                | Description                                                                                                 |
|:---------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| Sync Jira Tickets Status on FortiSOAR&trade; | Update FortiSOAR&trade; alert status as per Jira.                                                           |
| Update Jira Ticket                           | Update Jira ticket if its corresponding FortiSOAR&trade; alert status, severity, or description is updated. |
| Delete All Tickets from Project              | Clean up all JIRA tickets based on a project key.                                                           |
| Create Jira Ticket                           | Creates a ticket on Jira                                                                                    |
| Sync Alert Comment on Jira                   | Adds the comment added to an alert to the corresponding Jira ticket                                         |

## Scenario Record Set

| Name | Description                                                                             |
|:-----|:----------------------------------------------------------------------------------------|
| Jira | A demonstration of the Jira solution pack by creating an alert `Unable to log into VPN` |


>**Warning:** We recommend that you clone these playbooks before customizing to avoid loss of information while upgrading the solution pack.

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Usage](./usage.md) |
|-----------------------------------------|-------------------------------------------|---------------------|