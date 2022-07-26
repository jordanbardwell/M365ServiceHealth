# Overview
This is a Power Platform solution that provides Outlook and Teams adaptive card alerts for Microsoft 365 Service Health and Active issues. Adaptive card alerts can be sent to users via Outlook or Teams. Alerts can also be posted automatically to Teams channels.

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
## Licensing
Premium licensing in Power Platform is required for this solution to function since it utilizes Dataverse and other premium connectors. You will need Power Automate per user or Power Automate per flow AND either Power Apps per User, App Passes, or Pay as you go subscription.

## 1. Create Originator ID for Actionable Emails
You'll need to create an originator ID from the **[Actionable Email Developer Dashboard](https://outlook.office.com/connectors/oam/publish)**. This will allow you to send actionalable messages within your organization.

## 2. Create an App Registration in Azure AD
1. Go to [Azure Active Directory Admin Center](https://aad.portal.azure.com/)
2. Select **App Registrations**
3. Select **New Registration**. 
    1. Name the App Registration. Ex: *Microsoft 365 Service Health*
    2. Leave everything else as the default settings. Select **Register**
    3. Grant the App Registration the following **Microsoft Graph - _Application_** API Permissions:
        - ServiceHealth.ReadAll
    4. Once granted, **_Grant admin consent_**.
    5. Create a client secret and save the **secret value**.
