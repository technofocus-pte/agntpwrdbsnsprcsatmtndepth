---
lab:
  title: 'Lab 8: Process ingestion and process analytics with Copilot in Process Mining'
  description: In this lab you will learn to ingest the data and get the process analytics using Copilot in Process Mining.
  duration: 15 minutes
  level: 100
  islab: true
---

# **Lab 8: Process ingestion and process analytics with Copilot in Process Mining**

## **Exercise 1 - Process ingestion with Copilot in Process Mining**

1.  Navigate to the **Power Automate** portal
    using **https://make.powerautomate.com/**. Click on the environment
    selector and select the **Dev One** environment.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image1.png)

2.  From the left navigation, select **Process mining** and then
    select **Start here** under **Create new process**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image2.png)

3.  Keep the Process type – **Case ID process mining**, Data source –
    Dataflow, enter a **Process contact** as the Process name for your
    process name, and then select **Continue**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image3.png)

7.  If you are asked to **choose where to export**, then select **Power
    BI embedded** from the **Choose your destination** drop-down and
    then select **Continue**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image4.png)

8.  Under **Connect to your data**, choose **Text/CSV**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image5.png)

8.  Under the **Connection settings** area, select **Upload file** and
    then click **Browse.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image6.png)

9.  Open the **Grocery_Contacts.csv** file from **C:\LabFiles** in your
    lab VM. After uploading the file, if you see that a connection is
    created automatically, as shown in the first screenshot below, then
    go to the next step. If a connection is not created, then scroll
    down and select **Sign in** as shown in the second screenshot below,
    and sign in with your admin tenant credentials.

     **Note:** Ensure that you don’t select ‘Ask a chatbot’ while selecting
     the ‘Next’ button.
    
    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image7.png)
    
    ![Screenshot](./media/image8.png)

10. Once the file is uploaded, select **Next**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image9.png)

11. Select **Next** on the **Preview file data** page.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image10.png)

12. Select **Next** on the **Transform your data** page.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image11.png)

13. On the **Map your data** page, for the attributes below, map the
    column of attribute type correctly to set up your process map. Then,
    select **Save and analyze**.

     **contactid**: CaseID
    
     **genderCode**: Activity
    
     **birthdate**: Event Start
    
     **Note**: Case ID, Activity, and Event start are required.
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image12.png)

14. Wait for the report to be prepared.

    &nbsp;

15. Once the report is prepared, you will be able to explore the report.
    Navigate through the **Summary**, **Map**, and **Variant DNA** tabs.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image13.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image14.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image15.png)

## **Exercise 2 - Process analytics with Copilot in Process Mining**

1.  In process map view, if the Copilot pane is not open, then
    select **Copilot** on the command bar to the right. The Copilot pane
    opens.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image16.png)

2.  Copilot offers several prepared suggestions to easily get you
    started on engaging with your data.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image17.png)

3.  From the provided suggestions, select **Summarize my process**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image18.png)

4.  Copilot responds to your query.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image19.png)

5.  If available, it also provides subsequent prepared suggestions.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image20.png)

6.  (Optional) You can continue in conversation with Copilot by
    selecting subsequent suggestions. Alternatively, you can ask your
    own questions at any time using the text field in the bottom part of
    the Copilot pane.
