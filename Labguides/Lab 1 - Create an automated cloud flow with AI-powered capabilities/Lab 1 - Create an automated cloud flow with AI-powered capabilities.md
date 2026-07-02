# **Lab 1: Create an automated cloud flow with AI-powered capabilities**

**Objective:** In this lab, you will learn how to build an automated
cloud flow using natural language. Based on your description, Copilot
generates a flow with a trigger and actions. You will learn how to
integrate Microsoft Forms, Planner, and Teams to create an intelligent
workflow that streamlines task creation and team communication.

## **Exercise 1: Create a Microsoft Form and a plan** 

In this exercise, you will create a Microsoft Form to collect feedback
and set up a Planner plan for task management.

### **Task 1: Create a Microsoft Form**

In this task, we will create a Microsoft Form and enable response
collection. This form will be used to generate a task in Planner based
on the form response.

1.  Sign in to the Office 365 using +++https://www.office.com/+++ with
    the given Office 365 Tenant Credentials.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image1.png)

2.  Close the Pop-up window if it appears.

3.  From the left navigation pane, select **Apps > All apps**. When the
    “Welcome to Apps” pop‑up window appears, close it.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image2.png)

4.  Select **All apps**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image3.png)

5.  Select **Forms**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image4.png)

6.  Select the **Feedback** form to start with.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image5.png)

7.  Select the **Software Product Feedback** template from the list of
    templates.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image6.png)

8.  Select the **Collect responses** tab.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image7.png)

9.  Select the **Anyone can respond** option and then click the **Copy
    link** button. Copy the link to Notepad. We will use that to send a
    response while testing the flow.

     ![A screenshot of a chat AI-generated content may be incorrect.](./media/image8.png)

### **Task 2: Create a plan in the Planner**

In this task, we will create a plan within a designated team. This plan
will be used to generate a task card based on the form response.

1.  Go back to the +++https://www.office.com/+++. From the left
    navigation pane, select **Apps** and then select **Planner**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image9.png)

2.  From the bottom-left corner, select **+New plan**.

     ![A screenshot of a phone AI-generated content may be incorrect.](./media/image10.png)

3.  Select the **Simple plan** template from the list of templates.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image11.png)

4.  Select **Use template**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image12.png)

5.  In the **Name** field, enter +++My work plan+++. In the **Add to a
    group** field, select **Dev Team** from the drop-down menu and then
    click on the **Create** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image13.png)

6.  You can now see that the plan has been created.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image14.png)

## **Exercise 2: Create a cloud flow**

In this exercise, you will design an AI-assisted cloud flow that
connects Forms, Planner, and Teams and test the flow.

### **Task 1: Create a cloud flow**

In this task, we will create a flow to automatically generate a Planner
task and post a notification in a Teams channel whenever a new form
response is submitted.

1.  Log in to **Power Automate** using <https://make.powerautomate.com/>
    with your Office 365 Tenant credentials. Select the **Dev One**
    environment from the environment selector.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image15.png)

2.  From the left navigation pane, select **+Create** and then select **Describe it to design it**.

     ![](./media/image16.png)

3.  Enter the given prompt and then select the **Submit** icon.

     **Prompt** - +++When a new response is received to a Microsoft Forms survey, create a task, and then post a message on a Teams Channel+++

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image17.png)

4.  Based on the description, Copilot begins to create a
    suggested trigger and actions for your flow. Select **Keep it and
    continue**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image18.png)

5.  Review your connected apps and services. A green checkmark indicates
    that the connection is valid. Select **Create flow**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image19.png)

6.  Select the **When a new response is submitted** step.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image20.png)

7.  In the **Form Id** field, select **Software Product Feedback** from
    the drop-down menu. Collapse the **When a new response is
    submitted** pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image21.png)

8.  Select the **Get response details** step.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image22.png)

9.  In the **Form Id** field, select **Software Product Feedback** from
    the drop-down menu. Keep the **Response Id** as is in the **Response Id** field.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image23.png)

10. Collapse the **Get response details** pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image24.png)

11. Select the **Create a task** step.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image25.png)

12. Configure the parameters with the given values.

     **Group Id**: Dev Team
    
     **Plan Id**: My work plan
    
     **Title**: Enter +++**Check the response**+++
    
     ![A screenshot of a task AI-generated content may be incorrect.](./media/image26.png)

13. Collapse the **Create a task** pane.

     ![A screenshot of a task AI-generated content may be incorrect.](./media/image27.png)

14. Select the **Post message in a chat or channel** step.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image28.png)

15. Configure the parameters with the given values.

     **Post as**: Flow bot
    
     **Post in**: Channel
    
     **Team**: Dev Team
    
     **Channel**: DevChannel
    
     **Message**: Enter +++**A new task has been created based on the latest survey response.**+++
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image29.png)

16. Collapse the **Post message in a chat or channel** pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image30.png)

17. Rename the flow as **Software product feedback**.

     ![A screen shot of a software product AI-generated content may be incorrect.](./media/image31.png)

18. Select **Save draft**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image32.png)

### **Task 2: Test the flow**

In this task, we will test the flow to validate that tasks and notifications are triggered correctly.

1.  To test the flow, click the **Test** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image33.png)

2.  Select **Manually** and then click the **Publish & Test** button.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image34.png)

3.  To trigger the flow, open the form in a new browser window using the
    link saved in Notepad in your browser. Fill out the form.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image35.png)

4.  Click the **Submit** button at the end of the form.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image36.png)

5.  You can see that the flow ran successfully.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image37.png)

6.  Go back to the **Planner** and you see that the new task – **Check
    the response** has been created.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image38.png)

7.  From the **Planner** portal, select the **App launcher** and then
    select the **Teams** tab.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image39.png)

8.  From the left pane, select the DevChannel channel, and you can see
    the message.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image40.png)

**Summary**: In this lab, you learnt to create a Microsoft Form to
collect feedback, set up a Planner plan for task management, and then
build a cloud flow in Power Automate using the “Describe it to design
it” feature. You also learnt to test the flow to validate that tasks and
notifications are triggered correctly.
