# Overview
This is a Power Platform solution that provides Outlook and Teams adaptive card alerts for Microsoft 365 Service Health and Active issues. Adaptive card alerts can be sent to users via Outlook or Teams. Alerts can also be posted to Teams channels.

The UI was built using the Power CAT Creator Kit. Link: https://docs.microsoft.com/en-us/power-platform/guidance/creator-kit/overview

*Note: Adaptive Cards sent via email will only render in Outlook (Desktop/Mobile/Web).*

![Power App - Microsoft 365 Service Health](/images/M365_App_Overview.png)

Jump to [Installation Instructions](/README.md#installation-instructions)

## Features
- Subscribe to individual Microsoft 365 Services for health/issue alerts
- View Service Health
- View Active Issues and posts
- Receive adaptive card alerts via Outlook and Teams
- Supports Teams Channels

## Solution Specifications
- 10 Cloud flows
- 4 Dataverse Tables
- 4 Environment Variables
- 1 Custom Security Role
- 3 Connection References

## Requirements
- Premium connectors are used in this solution, so you'll need premium Power Apps/Automate licensing.
  - Power Automate per user or Power Automate per flow
  - Power Apps per user, Power Apps per app, or Power Apps Pay-As-You-Go
- Azure App Registration
  - ServiceHealth.ReadAll

## Notifications
Below are the different types of adaptive card notifications.
### Service Health Alert
![Service Health Alert](/images/M365_Teams_ServiceHealthAlert.png)

### Active Issue Update
![Active Issue Update](/images/M365_Teams_ActiveIssueUpdate.png)

## Home Screen
On the home screen, you can view Microsoft 365 Service Health, subscribe to service health for alerts, and view active issues.
![Power App - Microsoft 365 Service Health](/images/M365_App_Overview.png)

## Viewing Active Issue
![View Active Issue](/images/M365_App_ViewActiveIssue.png)

## Notification Settings
### Teams
![Teams Notification Settings](/images/M365_App_NotificationSettings_Teams.png)

### Email
![Power App - Microsoft 365 Service Health](/images/M365_App_NotificationSettings_Email.png)

### Teams Channels
![Power App - Microsoft 365 Service Health](/images/M365_App_NotificationSettings_TeamsChannels.png)

### Add Users to Teams or Email
![Power App - Microsoft 365 Service Health](/images/M365_App_NotificationSettings_Add_User.png)

### Add Teams Channels
![Power App - Microsoft 365 Service Health](/images/M365_App_NotificationSettings_Add_TeamsChannels.png)

# Installation Instructions
1. Download Solution ZIP File
2. Import Solution into environment with Dataverse
3. Configure
