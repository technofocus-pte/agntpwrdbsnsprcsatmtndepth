# **Lab 4: Create an automated cloud flow**

**Objective**: In this lab, you will learn how to create an automated
cloud flow in Microsoft Power Automate that streamlines vacation request
approvals. In this lab you will also learn to build a SharePoint list
for requests approval and configure actions such as profile retrieval,
approval workflow, conditional logic, email notifications, and item
updates.

## **Exercise 1: Create a SharePoint list**

### **Task 1: Create a SharePoint list**

Before you create the flow, create a SharePoint Online list. Later, you
will use this list to request approval for vacations.

1.  Sign in to office 365 using !!https://www.office.com/!! with your 365 Tenant
    Credentials.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image1.png)

2.  Close the Pop-up window.

     ![A white background with blue and purple text AI-generated content may be incorrect.](./media/imagee1.2.png)

3.  From the left navigation pane, select **Apps**. Close the pop-up
    window that says **Welcome to Apps**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/imagee1.3.png)

4.  Select **SharePoint**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/imagee1.4.png)

5.  Close the pop-up window.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/imagee1.5.png)

6.  Select **+Create site**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/imagee1.6.png)

7.  Select **Communication site**.

     ![](./media/image7.png)

8.  Select **Blank** template.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image8.png)

9.  Select **Use template**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image9.png)

10. Give a name to your site as !!Contoso!! and then select **Next**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image10.png)

11. Keep the language as **English** and then select **Create site**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image11.png)

12. Select **+New** and then select **List**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image12.png)

13. Select **List** under **How would you like to start?**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image13.png)

14. Enter the details and click on **Create**.

    - Name – !!Vacation!!

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image17.png)

15. For a better visibility, close the **New steps** pane which is opened on the right side on the screen.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image20.png)

16. Select **Add Column** and select **Date and time** then click on
    **Next**. (Note that **‘Title’** column is already present in the
    list, so we will start adding remaining columns.)

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image21.png)

17. Enter **Start Date** as Name in the create a column dialog that
    appears on the right pane and then click on **Save.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image22.png)

18. Simillarally create the following columns in your SharePoint Online list. The list after adding all the columns looks        like the image below.

    Column and its type:
     
    Title: Single line of text (already present in the list)
    
    Start Date: Date and Time
    
    End Date: Date and Time
    
    Comments: Text (Single line of text)
    
    Approved: Yes/No
    
    Manager Comments: Text (Single line of text)

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image23.png)

## **Exercise 2: Create an approval workflow**

In this exercise, you will configure triggers, add profile and approval
actions, apply conditional logic, and sett up email notifications and
SharePoint updates for approved or rejected requests.

### **Task 1: Create an automated cloud flow**

1.  Log in to **Power Automate** using !!https://make.powerautomate.com/!!
    with your office 365 Tenant credentials.

2.  Select **Dev One** environment from the environment selector.

    ![](./media/image26.png)

3.  Select **+Create** > **Automated cloud flow**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image27.png)

### **Task 2: Add a trigger**

1.  Give your flow a name - !!Approval Workflow!!.

2.  Under **Choose your flow's trigger**, select **When an item is
    created - SharePoint**, and then select **Create**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image28.png)

3.  On the designer window, close the **Copilot** pane for a better
    visibility.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image29.png)

4.  Select **When an item is created** card, select the **Site Address
    from dropdown.**

     **Note:** Refresh the page if you don’t see your site under the drop-down menu.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image30.png)

5.  Select **List Name** for the SharePoint list that you created
    earlier - **Vacation** and then close the pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image31.png)

### **Task 3: Add a profile action**

1.  Select **+icon** to add **new step**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image32.png)

2.  Type !!profile!! into the **Choose an operation** search box. Find,
    and then select the **Get my profile (V2)** action.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image33.png)

3.  Select **Sign in** and sign in with your Office 365 tenant
    credentials.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image34.png)

4.  From the drop-down menu of the **Advanced parameters**, mark the checkbox
    of **Select fields**.

     ![](./media/image35.png)

5.  Click in the plain area and then select enter !!aboutMe!! in the
    **Select fields** and then close the pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image36.png)

6.  Click on the **Save** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image37.png)

### **Task 4: Add an approval action**

1.  Select **+ icon** to add **new step** under **Get my profile(V2)** step.

     ![](./media/image38.png)

2.  Type !!approval!! into the **Choose an action** search box. Select
    the **Start and wait for an approval** action. 

    **Note**: If asked to create a new connection then select **Create new**.

     ![](./media/image39.png)

3.  Configure the **Start and wait for an approval** as below.

    - **Approval type** – Approve/Reject – First to respond

    - **Title** - !!Vacation Request for!! < CreatedByDisplayName > (Select Created by DisplayName from Dynamic Content)

     ![](./media/image40.png)

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image41.png)

    - For **Assigned To** field, select **Created By Email** from Dynamic content. To do so,
      select **Settings** menu in the **Assigned To** field, select **Use
      dynamic content** and then select **Created By Email.**

     ![](./media/image42.png)

     ![](./media/image43.png)

    - Details - <CreatedByDisplayName> !!wants to go on vacation from!! <StartDate> to <EndDate> 

      Select CreatedByDisplayName, StartDate and EndDate from dynamic content.

     **Note:** The **Approval type**, **Title** and **Assigned To** fields
     are required. You can use **Markdown** to format
     the **Details** field.

     ![](./media/image44.png)

     **Note:** This action sends the approval request to the email address in the **Assigned To** box.

### **Task 5: Add a condition**

1.  Select **+ icon** to add **New step** and then enter !!Condition!!
    in the search box select **Condition** in the list of actions.

     ![](./media/image45.png)

2.  On the **Condition** card, select **Choose a value** on the left. A
    list of dynamic values display. Select enter **Responses Approver
    response** in the search box and select it from the list of dynamic
    values.

     ![](./media/image46.png)

3.  In the **Condition** step, select the **Choose a value** box on the
    right and then enter !!Approve!! into the box.

     ![](./media/image47.png)

     **Note:** The valid responses to the **Approvals - Start an
     approval** action are "Approve" and "Reject". These responses are
     case-sensitive.

4.  Close the **Condition** card.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image48.png)

### **Task 6: Add an email action for approvals**

Follow these steps to send an email if the vacation request is approved:

1.  Select **+ icon** to **add an action** under the **True** branch of
    the condition.

     ![](./media/image49.png)

2.  Enter **send email** into the search box on the **Choose an
    action** card. Select the **Send an email (V2)** action from Office 365 Outlook. If asked, select **Sign in**. 

     ![](./media/image50.png)

3.  Configure the email card to suit your needs.

     **Note: To**, **Subject**, and **Body** are required.

     This card is a template for the email that is sent when the status of
     the vacation request changes.
    
     In the **Body** box on the **Send an email (V2)** card, use
     the **Comments** token from the **Approvals - Start an approval** action.

    - **To** - Select <CreatedByEmail> from dynamic content. Select
      **Settings** icon for the To field, select **Use dynamic content** and
      then select **Created By Email** from dynamic content.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image51.png)

    - **Subject** – Enter !!Your vacation request has been approved!!.

    - **Body** – Enter !!Your vacation has been approved by!! <ResponsesApproverName> (from dynamic content)

      Enter !!Approver Comments!! – Select **Responses Comments** from dynamic content.

     ![](./media/image52.png)

### **Task 7: Add an update action for approved requests**

1.  Under the **Send an email (V2)** step, select **+ icon** to **Add an
    action** in the **True** branch.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image53.png)

2.  Enter **Update item** in the search box on the **Add an
    action** card and then select the **Update item** action under
    **SharePoint.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image54.png)

3.  Configure the **Update item** with the Vacation Requests details.

    - **Site Address** – Select **Contoso site address** from the drop-down list

    - **List Name** – Select **Vacation** from the drop-down list

    - **Id** - Select <**ID**> from Dynamic content

    - Select **Show all** in the **Advanced parameters** field

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image55.png)

    - Title – Select <**Title**> from the Dynamic content listed under **When an item is created**.

    - Start Date - Select <**Start Date**> from the Dynamic content listed under **When an item is created**.

    - End Date - Select <**End Date**> from the Dynamic content listed under **When an item is created**.

    - Manager Comments - Select <**Responses Comments**> from the Dynamic
      content listed under **Start and wait for an approva**l.

     **Note: Site Address**, **List Name**, **Id**, and **Title** are required.

     ![](./media/image56.png)

### **Task 8: Add an email action for rejections**

1.  Select **+ icon** to **add an action** under the **False** branch.

     ![](./media/image57.png)

2.  Enter **Send email** into the search box of the **Choose an
    action** card, select **Office 365 Outlook** to filter the actions,
    and then select the **Send an email (V2) - Office 365
    Outlook** action.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image58.png)

3.  Configure the email as below.

    - To – Select <CreatedByEmail> from the Dynamic content. To do
      so, select **Settings** icon for the To field, select **Use
      dynamic content** and then select **Created By Email** from
      dynamic content.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image59.png)

     ![](./media/image60.png)

    - Subject – !!Sorry - Your vacation request was not approved!!

    - Body - Seelct <**Responses Comments**> from the Dynamic content

    - Close the pane.

     This card represents the template for the email that's sent when the
     status of a vacation request changes.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image61.png)

### **Task 9: Add update action for rejected requests**

1.  Under the **Send an email (V2)** step, select **+ icon** to **Add an
    action** in the **False** branch.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image62.png)

2.  Enter **update item** into the search box on the **Choose an
    action** card, and then select the **Update item -
    SharePoint** action.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image63.png)

3.  Configure the card as below.

    - Site Address – **Contoso site address** from the drop-down list

    - List Name – Select **Vacation** from the drop-down list

    - Id - <**ID**> (Select from Dynamic content under **When an item is created**)

    - Select **Show all** in the **Advanced parameters** field

     ![](./media/image64.png)

    - Title - <**Title**> (Select from Dynamic content under **When an item is created**)

    - Manager Comments - <**Manager Comments**> from Dynamic content

     **Note: Site Address**, **List Name**, **Id**, and **Title** are required.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image65.png)

1.  Select **Save** to save the work we've done.

     Your flow should now look like this.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image66.png)

     Now that we've created the flow, it's time to test it!

## **Exercise 3: Test the flow**

 In this exercise, you will test the automated vacation approval
 workflow by submitting a test request, monitoring the flow execution,
 and verifying approval notifications across Power Automate, Outlook.

### **Task 1: Request an approval to test your flow**

1.  To create a vacation request in the SharePoint Online list you
    created earlier, follow the steps given below.

2.  On the **Contoso** site, select **Vacation** list from the
    horizontal navigation menu and then select **+Add new item.**

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image23.png)

3.  Enter the following details and click on **Save.**

    - **Title** - !!Vacation Request!!
    
    - **Start Date** – Select December 15 
    
    - **End Date** – Select December 16
    
    - **Comments** – !!Travelling to my hometown!!

     ![](./media/image67.png)

     After you save this request, the flow triggers, and then, creates a request in the approvals center.

4.  Open the **Power Automate** portal. If you are on the designer
    window then select **Back**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image68.png)

4.  Under the history pane, you can see the status as **Running**. **Refresh** the page if you dont see the status as running. 

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image69.png)

5.  Select the **App launcher** from the top left corner of the Power
    Automate portal. Select **Outlook**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image70.png)

6.  You can see an email received by Power Automate approval. Click on
    the **Approve dropdown**, write comment as **Approved** and select
    **Submit**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image71.png)

7.  The Approver either Approves or Rejects the vacation and a requestor
    (in this case MOD Admin only) receives an email.

  The Approver has approved the vacation with the comments “Approved”.

8.  Check the status under Power Automate - > **My flows** ->
    **Approval WorkFlow**.

    ![](./media/image72.png)

9.  You can check the status of Approval in Microsoft Teams. Go to
    Microsoft Teams using !!https://teams.microsoft.com/!! (If required,
    sign in with your Office 365 tenant credentials). Select **(…)More
    added apps** > **Approvals**.

    ![](./media/image73.png)

### **Task 2: Cancel an approval request**

 Sometimes you might want to cancel an approval request that you've
 sent. Possibly you made a mistake in the request, or it’s no longer
 relevant. In either case, the person who sent the request can cancel
 it by following these steps:

1.  Enter the details in the **Vacation** list.

2.  Select the approval flow from the run History.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image74.png)

3.  Select **Cancel** in the side pane.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image75.png)

    ![](./media/image76.png)

     **Tip:** You can always select the **History** tab to view the
     approval requests that you've cancelled.

     ![](./media/image77.png)

     ![](./media/image78.png)

     **Note:** The cancel feature is supported on the **Create an approval (v2)** action.

 **Summary:** In this lab you learnt to automate a vacation approval
 process using Power Automate and SharePoint. You learnt to build an
 automated cloud flow triggered when a new item is added to the list,
 to add different actions and conditional logic and verified approval
 outcomes in Power Automate and Outlook.





