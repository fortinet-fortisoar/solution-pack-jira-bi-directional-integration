[Home](../README.md) |
|--------------------------------------------|

# Usage

The Jira bi-directional integration solution pack helps organizations keep SOC incident management on JIRA while utilizing FortiSOAR&trade;'s automation and orchestration capabilities. To discover how this solution bundle automation satisfies your needs, see the following section.

Jira solution pack functions in two modes:

- **Simulation Mode**: This mode helps experience Jira solution pack by creating example records that do not affect the Jira environment.

- **Environment Mode**: This mode is for using Jira solution pack in a Jira environment.

## Simulation Mode

Before you begin the simulation mode, make the following changes within the FortiSOAR&trade; instance:

1. Change the value of the global variable `Demo_mode` to `True`. For more information, refer to [Global Variables](https://docs.fortinet.com/document/fortisoar/7.2.2/playbooks-guide/488685/dynamic-values#Global_Variables) section in the *Playbooks Guide* of the FortiSOAR&trade; documentation.

2. Open the playbook collection **02-Use Case-jira** and select all the containing playbooks. Click the **Activate** button to activate all the selected playbooks.

**Jira Bi-Directions** solution pack includes a scenario that helps you get a better understanding of how the solution pack functions.

1. Browse to *Simulations* and select the *Jira Bi-Directions* scenario.

2. Click **Simulate Scenario**. This scenario adds an alert *Unable to log into VPN* with severity set to *Medium*.

3. Open the **Alerts** module and select the alert *Unable to log into VPN*.

4. Execute the playbook **Create Jira Ticket**. Specify the *Jira Project Key* in which to add this alert.

5. Jira tickets are updated when the ticket's *Severity*, *Status*, and *Description* are changed.

6. Jira ticket data is synced as soon as a comment or reply is added to an alert.

7. Trigger **Jira: Sync Jira Ticket Status** to sync the ticket status with the alert status in FortiSOAR&trade;. Enter values for fields *Jira Project KEY*, *Start At*, and *Max Result* when prompted.

8. Trigger **Delete All Jira Tickets from Project** playbook to delete all Jira tickets. Enter values for fields *Jira Project KEY*, *Start At*, and *Max Result* when prompted.

## Environment Mode

Before you begin the environment mode, make the following changes within the FortiSOAR&trade; instance:

1. Change the value of the global variable `Demo_mode` to `False`. For more information, refer to [Global Variables](https://docs.fortinet.com/document/fortisoar/7.2.2/playbooks-guide/488685/dynamic-values#Global_Variables) section in the *Playbooks Guide* of the FortiSOAR&trade; documentation.

2. Open the playbook collection **02-Use Case-jira** and select all the containing playbooks. Click the **Activate** button to activate all the selected playbooks.

**Jira Bi-Directions** solution pack contains playbooks that help in the following:

- Trigger the playbook **Create Jira Ticket** on an alert to generate a corresponding *Issue* in Jira.

    - Enter a value for the *Jira Project KEY* and update the Jira issue with the *Severity*, *Status*, and *Description* values contained in FortiSOAR&trade;'s alert.

- Trigger the playbook **Update Jira Ticket** on an alert to sync the FortiSOAR&trade; alert with the corresponding issue in Jira.

    - Enter a value for the *Jira Project KEY* and update the Jira issue with the *Severity*, *Status*, and *Description* values contained in FortiSOAR&trade;'s alert.

- Trigger the playbook **Sync Alert Comment on Jira** to update the Jira issue with the comment or reply added to the corresponding FortiSOAR&trade; alert.

- Trigger the playbook **Jira: Sync Jira Ticket Status** to update the Jira issue with the corresponding FortiSOAR&trade;'s alert. 

    - Enter a value for the *Jira Project KEY* and update the Jira issue with the *Severity*, *Status*, and *Description* values contained in FortiSOAR&trade;'s alert.

- Trigger the playbook **Jira: Delete All Jira Tickets** to delete all Jira issues associated with a project.

    - Enter values for *Jira Project KEY*, *Start At*, and *Max Result* when prompted.

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
|-----------------------------------------|-------------------------------------------|---------------------------|