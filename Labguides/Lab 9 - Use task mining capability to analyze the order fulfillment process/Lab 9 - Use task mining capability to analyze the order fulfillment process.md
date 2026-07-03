# **Lab 9 - Use task mining capability to analyze the order fulfillment process**

**Objective:** In this lab, you will learn to utilize Power Automate
task mining capabilities to analyze and optimize the order fulfillment
process. You will also learn how to import a solution containing sample
recordings, explore task mining features, and perform process analysis
to identify bottlenecks. Additionally, the lab covers automating process
steps and using analytics to gain insights into the process efficiency.

## **Exercise 1: Get ready for task mining**

### **Task 1: Import a solution**

1.  **Sign in** to Power Automate using
    +++https://make.powerautomate.com/+++ with your Office 365
    tenant credentials.

2.  Select your environment – **Dev One**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image1.png)

3.  On the navigation pane to the left, select **Solutions**, and then
    in the toolbar at the top, select **Import solution**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image2.png)

4.  Select **Browse**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image3.png)

5.  Select the **Processmining.zip** file from **C:\LabFiles** and open
    it.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image4.png)

6.  Select **Next**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image5.png)

7.  Select **Import** and wait for the solution to import.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image6.png)

8.  Wait for the solution to import.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image7.png)

## **Exercise 2: Explore the task mining capability**

### **Task 1: View sample recordings**

1.  Once you've successfully imported the .zip file, in the navigation
    pane to the left, select **Process mining** and then select
    the **Invoice submission process**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image8.png)

2.  If you are navigated to the **Analytics** tab, then go back one
    step. Go back to the **Invoice submission process** by selecting it
    from the breadcrumbs at the top of the page.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image9.png)

3.  You can see some of the existing recordings under the **Recordings**
    section.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image10.png)

### **Task 2: Explore the features**

You'll see the following features:

- **New recording**: Create a new recording.

- **Analytics**: See the process map and insights

- **Analyze**: Analyze a process.

- **Create activity names**: Create activity names for your process.

- **Delete process**: Delete your process.

**Note**: Zoom in or out on the screen to make all buttons visible.

![A screenshot of a computer AI-generated content may be incorrect.](./media/image11.png)

### **Task 3: Analyze a process**

When you analyze a process, the process mining capability analyzes
existing recordings to identify any bottlenecks within the business
process.

1.  Select **Analyze**.

     **Note:** The analysis will take a few minutes to complete. During
     this process, a status message is displayed under the **New
     recording** button.
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image12.png)

2.  If you run into an error during the analysis stage,
    select **Analyze** to trigger this action again.

3.  Once it's done, you see the **Process analysis status** change
    to **Analyzed**. Select **Analytics** to see the process map and
    insights.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image13.png)
    
     **Note:** This step may take a couple of minutes to complete after the analysis has been performed.

### **Task 4: Analytics page layout**

This section explains what you can do on the **Analytics** screen.

1.  Once it's done, you see the **Process analysis status** change
    to **Analyzed**. Select **Analytics** to see the process map and
    insights.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image14.png)

2.  You will see a screen similar to the following image.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image15.png)

3.  Initially, you will be on the **Process** tab. This tab gives
    in-depth information about the analyzed process, including the
    process map, time analytics for each variant, and each recording
    author.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image16.png)

4.  Look at the top analytics data. The average process time is 1.47
    minutes out of five recordings.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image17.png)

5.  Analyze other time-based metrics dashboards.

    - **Activity by average time in sec**: Notice that **Enter invoice
      details** and **Download invoice** are taking the most time.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image18.png)

    - **Recording by average time in min**: Notice that some people
      (**Preston Morales** and **Shakti Menon**) are taking more time than
      others.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image19.png)

6.  Select the **Legend** option.

     ![](./media/image20.png)

7.  The legend option gives additional information about the report,
    helping them to better understand the visualizations and data
    presented.

     ![](./media/image21.png)

8.  Select the **Application** tab.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image22.png)

9.  The **Application** tab gives information about the apps used in
    recordings. This includes what apps were used by authors, how often
    they were used, and what the transitions were between them. This
    report explains which connectors should be used when implementing
    automation for the process, and where to potentially use desktop
    flows, as there’s no existing connector.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image23.png)

10. Go back to the process map by selecting **Process**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image24.png)

### **Task 5: Automate activities**

In this task, you will use the Automate activities feature, which helps
you identify automation opportunities and guides you through automating
your processes using Microsoft Power Automate.

1.  Start to create a flow for automation by selecting **Automate
    activities** at the top.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image25.png)

2.  The tab opens in the browser and shows the flow designer. The
    recommended actions that match the activities from the process map
    automatically appear on the right panel. For example, several email
    connectors are suggested for you to use in order to automate
    the **Download invoice attachment from email** activity.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image26.png)

3.  Select **Office 365 Outlook** connector.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image27.png)

4.  Close the **Automate activities** and **Send feedback** panel.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image28.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image29.png)

5.  Before creating this automation process, first complete the
    pre-requisite required for this activity. On the Power Automate
    portal, click on the **App launcher** and then select
    **SharePoint**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image30.png)

6.  Select the **Contoso** site.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image31.png)

7.  Select the **Documents** tab.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image32.png)

8.  Select **Upload** and then select **Files**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image33.png)

9.  Upload the **Invoice** Excel from the **C:\Labfiles** folder of the
    VM.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image34.png)

10. Select the **Send an email (V2)** action.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image35.png)

11. In the **To** field, enter **MOD** and then select **MOD
    Administrator** from the suggestions.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image36.png)

12. Enter +++**Invoice**+++ in the **Subject** field.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image37.png)

13. Select **+** **icon** > **Add an action** to add a new step.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image38.png)

14. Search for and select **Get file content using path**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image39.png)

15. Select the **Contoso** site address from the drop-down menu.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image40.png)

16. To select the file path, select the **Folder** icon > **Shared
    Documents** > **Invoice.xlsx**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image41.png)

17. Go back to the Send an email (V2) step. Select **Show advanced**
    option.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image42.png)

18. In the **Attachments Name – 1** field, enter +++**Invoice**+++. In
    the Attachment Content field, select **File Content** from the dynamic content.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image43.png)

19. Select **Automate activities** from the toolbar.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image44.png)

20. Select the **Microsoft Teams** connector from the **Notify Team of
    submission**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image45.png)

21. Close the **Automate activities** pane for better visibility.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image46.png)

22. Select **Post message in a chat or channel** action.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image47.png)

23. Select the following options from the drop-down menu of each field.

     Post as – Flow bot
    
     Post in – Channel
    
     Team – Dev
    
     Channel – DevChannel
    
     Message – Enter +++Please check invoice+++
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image48.png)

24. Select **Save** to save the flow.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image49.png)

25. Select **Test** to test the flow.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image50.png)

26. In the **Test Flow** window that appears on the right side of the
    screen, select **Manually** and then select **Test**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image51.png)

27. Once you see the green check mark next to the apps, which shows you
    have signed in successfully, then select **Continue**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image52.png)

28. Select **Run flow**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image53.png)

29. Select **Done**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image54.png)

30. Click on the **App launcher** and then select **Outlook**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image55.png)

31. You will see an email with the attachment.

     ![A screenshot of a chat AI-generated content may be incorrect.](./media/image56.png)

32. Click on the **App launcher** and then select **Teams**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image57.png)

33. Go to the **DevChannel**. You will see the message from the bot.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image58.png)

**Summary:** In this lab, you have learnt to utilize Power Automate task
mining capabilities to analyze and optimize the order fulfillment
process. By importing a pre-built solution with sample recordings, they
explored key features of task mining, including process analysis,
identifying bottlenecks, and generating automation recommendations. You
also learnt how to assess process efficiency through detailed analytics
on time spent across various tasks and applications. The lab highlighted
how task mining can streamline business processes by identifying
automation opportunities, ultimately improving operational efficiency
and reducing manual workloads in the order fulfillment process.
