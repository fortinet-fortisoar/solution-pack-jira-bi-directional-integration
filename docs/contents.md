| [Home](../README.md) |
|--------------------------------------------|

# Contents

The **Jira** solution pack contains the following resources.

## Module Schema

|**Name**|**Description**|
| :- | :- |
| Alerts | Added new field "Jira Ticket ID" |

## Connector

|**Name**|**Description**|
| :- | :- |
| Jira | Jira Service Desk Connector for issue creating, updating and deleting |

## Playbook Collection

### 02 - Use Case - JIRA

|**Playbook Name**|**Description**
| :- | :- |
| Sync Jira Tickets Status on FortiSOAR | Update FortiSOAR Alert Status as per Jira Status. |
| Update Jira Ticket | Update Jira ticket if its corresponding FortiSOAR alert status, severity or description is updated. |
| Delete All Tickets from Project | Playbook clean up all JIRA tickets based on a specific Project Key. |
| Create Jira Ticket | Playbook creates its corresponding ticket on Jira |
| Sync Alert Comment on Jira | When a comment is added to an alert, adds the same comment to the corresponding Jira ticket |

>**Warning:** We recommend that you clone these playbooks before customizing to avoid loss of information while upgrading the solution pack.
