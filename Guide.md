# Youtrack - Beginner Guideline


## Table of contents
- [Table of contents](#table-of-contents)
- [Project](#1-project)
    - [Create a Project](#11-create-a-project)
    - [Team](#12-team)
    - [Roles](#13-roles)
    - [Time Tracking](#14-time-tracking)
- [Agile Board](#2-agile-board)
    - [Overview](#21-overview)
    - [Sprints](#22-sprints)
    - [New Swimlane](#23-new-swimlane)
    - [Cards](#24-cards)
    - [Board Time Tracking](#25-board-time-tracking)
    - [Board Settings](#26-board-settings)
- [More Workflows](#3-more-workflows) 
   - [Create Workflow](#31-create-a-workflow)
    - [Auto Comment](#32-example-auto-comment)
    - [Auto Card](#33-example-auto-card)
- [Report and Dashboard](#3-report-and-dashboard)
    - [Create a Report](#31-create-a-report)
    - [Dashboard Overview](#32-dashboard-overview)
- [Supporting Information](#4-supporting-information)
    - [GitHub Integration](#41-github-integration)
    - [Enable Registration on your YouTrack Server](#42-enable-registration-on-your-youtrack-server)

## 1. Project

### 1.1 Create a Project
If you want to create a project you go to: projects -> create project.
![alt text](/pics/CreateProject.png)
Now you can name your project, give it an ID, choose the project type and give it a description.

### 1.2 Team
The first important step is to invite the people you want to work with on your project. To do this, you need to go to the project settings. You can find it when you click on your project in the projects tab.

Now you see the project settings on the right
![alt text](/pics/1.2Team2.png)
Now, click on "Team." After that, you’ll see a button called "Add members." Click it to add new people to your team. But remember, you can only add people who are already registered on the YouTrack server. When you add someone, they automatically get the role of a developer.

### 1.3 Roles
Each project has different roles. Like I said before, when you add people, they get the developer role automatically. If you want to change their role, go back to the project settings and click on "Access." Here, you can see all your team members and their roles. To change someone's role, click "Grant role" and choose a new role for the person or group.
![alt text](/pics/3.Roles1.png)
If you want to know more about the roles you can go to the administration settings of the youtrack server. Here you go to Access Management -> Roles.
![alt text](/pics/3.Roles3.png)

Here you see a list of all the roles available on the YouTrack server and what each role can do. If you are the owner of the server, you can also add new roles to the server.

### 1.4 Time Tracking
Before you go to the Agile board(s) of your project, I suggest turning on time tracking. This feature helps you automatically track how long a task or card is in progress. To enable time tracking, go to the project settings again and select "Time Tracking." Then, set the options like shown in the picture.
![alt text](/pics/1.4TimeTracking1.png)
After that you go to workflow 
![alt text](/pics/workflow1.png)
and click on "Attach workflows". Then you search for the "In Progress Work Timer".
![alt text](/pics/1.4TimeTracking2.png)
If you have never set up this work flow before you will get a "requires setup" notification next to the "In Progress Work Timer". On the right half you see a detailed view with 2 Rules. Simply click on Apply fixes to use time tracking.
![alt text](/pics/1.4TimeTracking3.png)


## 2. Agile Board

### 2.1 Overview
Here you see a quick overview over an agile board
![alt text](/pics/2.1Overview.png)
not my edit<br>

### 2.2 Sprints
Whenever you're working on your project, you're in a sprint. Sprints usually last between 1 to 4 weeks. To make a new sprint, click on the current sprint, then click "New Sprint."
![alt text](/pics/2.2Sprint.png)
Now, you can name the sprint, set a goal, and choose how long it will last. When you create the sprint, it will be automatically selected, and you can either start it right away or plan all the sprints before the project starts.

### 2.3 New Swimlane
If you click on "New Swimlane" in the bottom right corner of the page, you can create a new swimlane. A window will open with different settings for the swimlane.

Now you can see the Estimation and Time Spent fields. These fields wouldn't be there if we didn't set up time tracking.

### 2.4 Cards

To create a new card you simply click "new card" in a swimlane and it will create a card in the swimlane.
![alt text](/pics/2.3NewSwimlane.png)


### 2.5 Board Time Tracking
Now we can use time tracking. When you drag and drop a card into the "In Progress" state, a timer will start. If you move it to another column (like Open, To Verify, or Done), the timer will automatically stop, and the time will be added to that card.

You can click on the card to see its history, which shows you which team member worked on the task and for how long. It even has a little circle that shows if you’re within the estimation you set before or if the task is overdue.
![alt text](/pics/2.5BoardTimeTracking.png)

### 2.6 Board Settings
You can configure some things on your board by going to the board settings. You can find this in the picture at [Overview](#21-overview). Here, you'll see general settings, but I won’t cover those because there's nothing to set up. However, if you're interested, you can take a quick look.
The important settings are under "Columns and Swimlanes." Here, you can add an extra column if you need it.
If you add a new type, you can create swimlanes for other types, like Bug or Epic.


So the last thing is the chart settings. To see the changes you do here, just check the Board (Sprint) diagram like [Overview](#21-overview). So now you see the chart and the chart settings. It should look like this:
![alt text]![alt text](/pics/2.6BoardSetting2.png)
Here you can choose the type, the calculation and the issue filter. This is a really minimalistic chart. To get better ones we will create a report in the next big point.

## 3. More Workflows

### 3.1 Create a Workflow
In YouTrack you can save time by automating tasks and processes that you do often. This means you don’t have to do the same work over and over again.

First, go to your account settings. After that, select Workflow.

![alt text](/pics/workflow1.png)

You can write down your new Workflows in the JavaScript Editor. Or you can just use the Workflow Constructor. 

![alt text](/pics/workflow2.png)


### 3.2 Example auto comment
You can set up YouTrack to write an automatic comment every time you open an issue.
![alt text](/pics/workflow_autocomment.png)

### 3.3 Example auto card

Imagine you have to work on a very similar task every week. Instead of creating a new card each time, you can have one automatically generated for you.

With this workflow, a new "Write Blog Post" card will be created in the backlog as soon as your current "Write a Blog Post" card is in the final state.
![alt text](/pics/workflow_autoblogpost.png)


## 4. Report and Dashboard

### 4.1 Create a Report
To create a report, just click on "Reports." You’ll see different types of reports you can choose from. For example, you can select a burndown chart as one of the options.
![alt text](/pics/3.1CreateReport.png)
The most important setting is the "Original Estimation Field." It is best to choose Issue Count and Story Points for a good report. You can also pick "Estimation," but you need to set the second "Original Estimation Field" to "Time Spent." If you don’t do this, you can leave the second field empty.
![alt text](https://i.imgur.com/4MvnXu4.png "Burndown example")
(not my picture)<br>
In the top right, you can manually recalculate your report and change the settings. On the y-axis, you will see the "Original Estimation Field," and on the x-axis, you will see the timeline. 


### 4.2 Dashboard Overview

Here, you can see a small overview of an example dashboard. You can add widgets if you want and share your dashboard with other users or groups. You can also switch to a list view of a project, where you can see every user story and its subtasks in a clear format.
![alt text](/pics/3.2Dashboard.png)
Here is a picture of the list view.
![alt text](/pics/3.2.1List.png)


## 5. Supporting Information
### 5.1 GitHub Integration
You can connect your GitHub repository to the project to make commits in YouTrack. Just go to the project settings and click on VCS.
![alt text](/pics/4.1VSCIntegration.png)
Now on "New VCS integration..." button you can link your GitHub repository. So after that you can do a commit if you double click on a card and then click add commit.
![alt text](/pics/4.1VSCIntegration2.png)

### 5.2 Enable Registration on your YouTrack Server
To do this go the admin settings on the server and click on Access Management -> Auth Modules.
![alt text](/pics/4.2Enable%20Registration.png)
Then there should be the "Hub" Auth Module. Simply click on it and enable the registration. Thats it.
