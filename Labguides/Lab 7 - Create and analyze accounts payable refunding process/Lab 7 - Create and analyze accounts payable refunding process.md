# **Lab 7 - Create and analyze accounts payable refunding process**

**Objective:** In this lab, you will learn to create and analyze an
accounts payable refund process using Power Automate Process Mining
capabilities. You will also learn to import data from a CSV file, create
a new process, and utilize the Process Mining desktop app to analyze key
performance indicators (KPIs) and other metrics to gain insights into
the efficiency and performance of the accounts payable refund process.

## **Exercise 1: Create a process and import data**

### **Task 1: Create a process**

1.  Go to +++https://make.powerautomate.com/+++. If asked, sign in with
    your Office 365 tenant credentials. Select your environment – **Dev
    One**.

     ![](./media/image1.png)

2.  On the navigation pane to the left, select **Process mining**.

     ![](./media/image2.png)

3.  In the **Create new process** section, select **Start here**.

     ![](./media/image3.png)

4.  In the **New process** screen, Select Case ID process mining as the
    Process type, select **Dataflow** as the Data source, enter the
    process name **AP Refunds**, and then select **Continue**.

     ![](./media/image4.png)

5.  If you are asked to **choose where to export**, then select **Power
    BI embedded** from the **Choose your destination** drop-down and
    then select **Continue**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image5.png)

### **Task 2: Import data**

1.  In the **Choose a data source** screen, select **Text/CSV**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image6.png)

2.  Under the **Connection settings** heading, select **Upload file**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image7.png)

3.  Select **Browse**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image8.png)

4.  Find and select **SampleData_AP_Refunds_Financial_EventLog.csv**.
    Location: **C:\Lab Files**

5.  Select **Open**.

6.  If you're asked to authenticate, select **Sign in** and follow the
    prompts. (Configure Pop-up blocker to allow.)

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image9.png)

7.  Select **Next**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image10.png)

8.  Preview file data and select **Next**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image11.png)

9.  When you see the Power Query, which allows you to transform your
    data, select **Next**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image12.png)

10. Match the **Attribute Name** from the sample data to the **Attribute
    Type** as mentioned in the next step.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image13.png)

11. In this sample, the data attributes you’ll change
    are **InvoiceValue**, **Resource**, **StartTimestamp**, **EndTimestamp**, **CaseId**,
    and **ActivityName** as follows.

     **InvoiceValue** – Financial per case (first event)
    
     **Resource** – Resource
    
     **StartTimestamp** – Event Start
    
     **EndTimestamp** – Event End
    
     **CaseId** – Case ID
    
     **ActivityName** – Activity
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image14.png)

12. When you're **finished**, the attribute mapping should look like the
    following screenshot.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image15.png)

13. Select **Save and analyze**. The analysis might take a few minutes
    to run.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image16.png)

14. When the **analysis process is complete**, you’ll see a process map
    and a dashboard with other insights about your process. On the
    dashboard, you can view many metrics that will help you **analyze
    your process.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image17.png)

## **Exercise 2: Analyze a process**

### **Task 1: Analyze a process**

Let’s take the analysis of our process beyond KPIs. We'll use the Power
Automate Process Mining desktop app, where you can edit and analyze your
processes created in the process mining capability.

1.  From the top bar, click on the **Download Process Mining app**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image18.png)

2.  Double-click on the **PowerAutomateProcessMining** App installer
    file in the **Downloads** folder of the VM.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image19.png)

3.  Click on the **Install** button.

     ![](./media/image20.png)

4.  After installing the **Process Mining** app, it will launch
    automatically. If it does not, open the app manually. Once launched,
    select **English** as the language and click **Next Step**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image21.png)

5.  Select the check box to agree to the **Terms of Use**, and then
    click **Next Step**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image22.png)

6.  Select the **Apply and Mine** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image23.png)

7.  Enter your admin tenant Id and click on the **Sign In** button.

     ![A screenshot of a computer login AI-generated content may be incorrect.](./media/image24.png)

8.  Then enter your admin tenant password and click on **Sign in**.

     ![A screenshot of a login box AI-generated content may be incorrect.](./media/image25.png)

9.  If pop up appears saying ‘Stay signed in to all your apps’ then
    select **No, sign in to this app only**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image26.png)

10. On the Power Automate Process Mining app toolbar, select the
    environment – **Dev** **One** from the top right.

     ![](./media/image27.png)
    
     **Note**: If you get an application error, keep trying by selecting **Retry**.
    
     ![A computer screen shot of a blue and white application error AI-generated content may be incorrect.](./media/image28.png)

11. Search for the process that you created with the process mining
    capability in Power Automate (**AP Refunds**).

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image29.png)

12. Select **Default** to display the default view. You’re ready to use
    the advanced capabilities of the Process Mining desktop app.

     ![](./media/image30.png)
    
     **Note 1**: If you get an error - '**Loading process model failed**',
     then close the **Process Mining** app and **reopen** it from
     the **Start** menu of the VM.
    
     **Note 2:** If it shows an error message related to **Model size is
     too large for your PC configuration** and gives Yes and No options for
     execution, select **Yes**.
    
     ![](./media/image31.png)

13. You can see the process map now.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image32.png)

14. On the **Customize** panel toolbar, select **Frequency** (the first
    icon), and then select **Case count** in the **Metric** dropdown
    menu.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image33.png)
    
     The process map displays the number of cases of the process that
     include the activity specified at each node.

15. On the **Customize** panel, select the **Performance** (clock icon),
    and then select **Mean duration** from the dropdown menu.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image34.png)
    
     Notice that the **Refund with special voucher** step has a long mean
     duration compared to other steps.
    
     ![A diagram of a customer service AI-generated content may be incorrect.](./media/image35.png)

16. On the **Customize** panel, select **Finance** (the piece of paper
    icon), and then select **Mean** from the **Metric** dropdown menu.

     ![](./media/image36.png)
    
     Notice that the same **Refund with Special Voucher** step involves
     only $631.11 in invoice value, which is less than half of most of the
     other steps.
    
     ![A white sign with black text AI-generated content may be incorrect.](./media/image37.png)

17. Select **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image38.png)

**Summary:** In this lab, you created and analyzed an accounts payable
refund process using Power Automate Process Mining capabilities. By
importing CSV data, they constructed a detailed process map and
dashboard, allowing them to examine key performance indicators (KPIs)
and process metrics. Through the Power Automate Process Mining desktop
app, participants performed deeper analysis, identifying inefficiencies
such as long durations and lower invoice values in specific steps. This
lab demonstrated how Process Mining can help organizations optimize
financial workflows, improve efficiency, and streamline accounts payable
operations.
