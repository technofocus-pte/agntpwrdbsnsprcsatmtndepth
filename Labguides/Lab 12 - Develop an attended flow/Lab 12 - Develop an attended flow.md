# **Lab 12 - Develop an attended flow that reads orders and prompts users to select a discount**

**Objective:** The objective of this lab is to develop an **attended
Power Automate Desktop flow** that automates the process of reading
orders from an Excel file and prompts users to apply a discount based on
certain conditions. Participants will create a flow that reads data,
checks if the order amount exceeds a specific threshold, and prompts the
user to decide whether to apply a discount, with the option to enter the
discount value. The flow will then update the Excel sheet with the
applied discount.

### **Task 0: Install Microsoft Excel (If not installed on the VM)**

1.  Open the Edge browser and navigate to
    +++https://www.office.com+++ office 365 portal. Enter the admin
    tenant ID and Password in the respected field and click on
    the **Sign in** button.

     ![](./media/image1.png)
    
     ![](./media/image2.png)

2.  Click on the **Yes** button to stay signed in.

     ![](./media/image3.png)

3.  After login, click on the **Apps** from the left menu bar, click on
    the **Install apps**, and select **Microsoft 365 apps**. It will
    navigate to a different portal. If required, please sign in again.

     ![](./media/image4.png)

4.  Click on the **Install Office** button.

     ![](./media/image5.png)

5.  Navigate to the **Download** folder in VM and click on
    the **OfficeSetup.exe** and install Office.

     ![](./media/image6.png)

6.  Wait for a few minutes while the system is installing Office 365 in
    the VM.

     ![](./media/image7.png)

**Must Remember**: After the installation of Office, open the Excel app,
log in with the admin tenant password, accept all terms and conditions,
and activate the Office in the VM.

## **Exercise 1: Develop an Attended Flow**

### **Task 1: Create a Power Automate desktop flow**

1.  Open the **Power Automate Desktop app** and, if required, log in
    with the given **Office 365 tenant credentials**.

2.  Choose the **Dev one** environment and click on the **+ New**,
    then **Flow**, and start creating the new flow.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image8.png)

3.  Enter +++**Message Box Communication**+++ as the flow name and then
    click on the **Create** button.

     **Note**: Ensure that the **Power Fx** enabled toggle button is turned **off.**
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image9.png)

4.  Close the Copilot pane to maximize visibility.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image10.png)

5.  From the **Actions** pane to the left of the screen, search for the
    +++**Display select file dialog**+++ action and double-click the **Display select file dialog** action.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image11.png)

5.  Enter +++Select Excel+++ in the **Dialog Title** field, enter the location of the folder in the **Initial folder** field as +++C:\Labfiles\Orders+++, and in the File filter field, enter +++\*.xlsx+++. Select **Save** in the lower part of the dialog.

     ![A screenshot of a computer dialog box AI-generated content may be incorrect.](./media/image12.png)

6.  Before reading any data from the selected file, you must launch it
    using the **Launch Excel** action. In the **Actions** pane, search
    for the +++Launch Excel+++ action and double-click it.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image13.png)

7.  Configure the **Launch Excel** action with the following values.

    - **Launch Excel**: Select the **and open the following document**
      option from the drop-down menu.

    - **Document path**: +++**%SelectedFile%**+++

    - Select **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image14.png)

7.  To read the data from the Excel file, search for the +++**Read from
    Excel worksheet**+++ action in the **Actions** pane and double-click
    the action.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image15.png)

8.  Enter +++**%ExcelInstance%**+++ in the **Excel instance** and select **All available values from worksheet** in the **Retrieve** field. Click on the **Save** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image16.png)

8.  From the **Actions** pane, search for the +++**Get first free
    column/row from Excel worksheet**+++ action and double-click it to
    add it to the flow. It is used to retrieve the first free column and
    row in the Excel worksheet.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image17.png)

9.  Enter +++**%ExcelInstance%**+++ in the **Excel instance** and then click on the **Save** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image18.png)

9.  Search for and double-click the +++Set Variable+++ action from the
    **Actions** pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image19.png)

10. Name the variable as +++Counter+++ and enter +++1+++ into the
    **Value** field and select **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image20.png)

10. Search for and double-click the +++**Display input dialog**+++ from the **Actions** pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image21.png)

11. Configure the following fields.

    - **Input Dialog Title**: +++**Header**+++

    - **Input Dialog Message**: +++**Enter the Header**+++

    - **Default Value**: +++**Discount**+++

    - Select **Save**.

     ![](./media/image22.png)

11. Search for and double-click the +++**Write to Excel worksheet**+++
    from the **Actions** pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image23.png)

12. Configure the **Write to Excel worksheet** action with the following
    details:

    - **Excel instance**: +++%ExcelInstance%+++

    - **Value to write**: +++**%UserInput%**+++

    - **Write role**: On specific cell

    - **Column**: +++**9**+++

    - **Row**: +++**%Counter%**+++

    - Select **Save**.

     ![](./media/image24.png)

12. From the **Actions** pane, search for and double-click the +++**For each**+++ loop for action to iterate through the retrieved data.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image25.png)

13. In the **Value to iterate** field, enter +++**%ExcelData%**+++ to
    iterate the section. Then click on **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image26.png)

13. Search for and double-click the +++ **Convert text to number** +++
    from the **Actions** pane. It is used to check the value of
    the **Gross** column (column G or the sixth column in the worksheet,
    in the sheet, the name of the column is “6”).

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image27.png)

14. Configure **Text to convert** as +++**%CurrentItem[6]%**+++ and
    then click on the **Save** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image28.png)

14. Search for and double-click the +++**If**+++ action from the **Actions** pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image29.png)

15. Check whether it exceeds 100,000 and configure it as follows:

    - **First operand**: +++**%TextAsNumber%**+++

    - **Operator**: Greater than or equal to (>=)

    - **Second operand**: +++**100000**+++

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image30.png)

16. From the **Actions** pane, search for and double-click the
    +++**Display message**+++ action to have it under the **If** condition.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image31.png)

15. To provide the necessary information to the user and prompt them to
    choose **Yes** or **No**. Then click on the **Save** button. Enter
    the following details.

    - **Message Box title**: +++**Add discount**+++

    - **Message to display**:

      - +++**Product:** %CurrentItem[2]%+++

      - +++**Units**: %CurrentItem[3]%+++

      - +++**Gross:** %TextAsNumber%+++

    - **Message box button**: Yes – No

     ![A screenshot of a computer screen AI-generated content may be incorrect.](./media/image32.png)

16. Add another +++**If**+++ action under the **Display message** action
    to check which button was pressed in the previous step.

     ![](./media/image33.png)

17. Enter the following details in the respective field and then click on the **Save** button.

    - **First** **operand**: +++%ButtonPressed3%+++
    
    - **Operator:** Equal to (=)
    
    - **Second operand:** +++Yes+++

     ![A screenshot of a computer screen AI-generated content may be incorrect.](./media/image34.png)

17. Add +++**Display Input Dialog**+++ action under the second **If** action.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image35.png)

18. Enter the given parameters into the respective field, then click **Save**.

     **Input dialog title**: +++Discount Value+++
    
     **Input dialog message**: +++Enter the Discount Value+++
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image36.png)

18. Add the +++**Write to excel worksheet**+++ action below the second **If** action.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image37.png)

19. Enter the following details into it:

    - **Excel instance:** +++%ExcelInstance%+++
    
    - **Value to writer**: +++%UserInput2%+++
    
    - **Write mode:** On specific cell
    
    - **Column:** +++9+++
    
    - **Row:** +++%Counter%+++
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image38.png)

20. Under the first **If End** loop, add the action +++**Increase Variable**+++.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image39.png)

21. Add the **Variable name** as +++**%Counter%**+++. In the Increase by
    field, enter +++**1**+++ and then select **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image40.png)

21. From the top bar, select **Save** the flow for the test.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image41.png)

### **Task 2: Test the Flow**

1.  Click on the **Run** button to execute the test.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image42.png)

2.  First sheet folder will open, select the **excel** **file** from it.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image43.png)

3.  The header window will pop up, as we set the **Discount** as the
    default, and click on the **OK** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image44.png)

4.  **The Discount** window appears, which shows this product is more
    than **100000**, select **yes** or **no**. In this test, we
    select **yes** (**yes**, we give a discount on this product).

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image45.png)

5.  Then enter the **Discount Value**. For the test, we enter
    +++**10000**+++ and then click **OK**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image46.png)

6.  In the Excel sheet, the discount value is updated.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image47.png)

7.  The loop is running **continuously** for all the products.

**Summary:** In this lab, participants developed an attended Power
Automate Desktop flow that reads order data from an Excel file, checks
if the order amount exceeds a set threshold, and prompts the user to
apply a discount. The flow efficiently automates the decision-making
process by allowing users to interact with the flow through prompts and
enter discount values. This lab provides hands-on experience in
automating tasks involving Excel, user inputs, and conditional logic,
empowering participants to streamline similar business processes using
Power Automate Desktop.
