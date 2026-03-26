**Lab 2 - Build an Inventory Management App**

**Objective:** In this lab, you will learn to create a functional
inventory management application using Microsoft Power Apps and Copilot.
Participants will learn to set up their Dataverse environment, design
app screens, manage data, and automate inventory restocking workflows
with Power Automate.

**Exercise 1: Build an Inventory Management App**

**Task 1: Create an inventory management app using Copilot.**

1.  Open a browser and go to +++\*\* sign in with office 365 admin
    tenant account.

2.  Click on the environment in the top right corner and select **your
    developer** environment – **Dev One**.

> ![](./media/image1.png)

3.  From the left navigation menu, click on **Create** and then select
    **Start with Copilot**.

> ![](./media/image2.png)

4.  Enter the prompt below and click on the **Generate** button.

> +++**Build a candy inventory management app**+++
>
> ![](./media/image3.png)

5.  The copilot generates the tables as shown in the image below.

> ![](./media/image4.png)

6.  Select the **Supplier** table, then select **View data,** and
    explore the data.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image5.png)
>
> ![](./media/image6.png)

7.  In the Copilot pane, enter the given prompt and then select the
    **send** icon.

> **Prompt**: +++Add a Supplier email column to the Supplier table.+++
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image7.png)

8.  You can see the column added by Copilot.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image8.png)

9.  Select the **Inventory** table and observe the available columns.

> ![](./media/image9.png)

10. Enter the given prompt in the text box and click the **send** icon.
    This column is required to notify when the quantity falls below the
    reorder point.

> +++Add reorder point column to Inventory table+++
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image10.png)

11. Check if the new column has been added to the table by Copilot.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image11.png)

12. Add a **candyInStock** column with the data type set to **Number**.
    If the quantity is less than the reorder point, the **Quantity**
    column will automatically be updated using **candyInStock**.

> +++Add a candyInStock column to the Inventory table with the whole
> number data type. The records should be in whole numbers.+++
>
> ![](./media/image12.png)
>
> **Note**: After executing the above prompt, if the **Reorder Point**
> column throws a data validation error, then manually change the sample
> values to match the Number data type.

1.  Click on the Record Point column drop-down and select **Edit
    column**.

> ![](./media/image13.png)

2.  Click on the data type field and select **Number** as the data type.

> ![](./media/image14.png)

3.  Click on the update button.

> ![](./media/image15.png)

4.  Manually change the record value.

> ![](./media/image16.png)

13. The table has been updated with the **Reorder Point** column and
    **candyInStock** column. 

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image17.png)

14. Close the **Copilot** pane.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image18.png)

15. Click on the **Save and open app** button.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image19.png)

16. In the **Done working?** window, click **Save and open app**, then
    wait for the app to be created.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image20.png)

17. In the **welcome** window, select **Skip**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image21.png)

18. The app gets created and should look like the image below.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image22.png)

19. Click the **Save** button, enter the name **Candy Inventory
    Management App**, and then click **Save** again.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image23.png)

**Exercise 2: Create a Power Automate flow to restock the inventory.**

**Task 1: Create a Power Platform flow to trigger restock email**

1.  Log in to **Power Automate** using
    +++<https://make.powerautomate.com/>+++ with your Office 365 Tenant
    credentials. Select the **Dev One** environment from the environment
    selector.

> ![](./media/image24.png)

2.  Copy the following prompt and paste it in the Copilot field and then
    select **Generate**.

> **Prompt:** +++Create a candy restock flow when a row is added or
> modified in the Dataverse table. Add a condition to check if the
> quantity is less than the reorder points. If it is less then take an
> approval to update the row+++
>
> ![](./media/image25.png)

3.  Based on the description, Copilot begins to create a
    suggested trigger and actions for your flow. Select **Keep it and
    continue**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image26.png)

4.  Review your connected apps and services. A green checkmark indicates
    that the connection is valid. Select **Create flow**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image27.png)

5.  Select the **When a row is added or modified** step.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image28.png)

6.  Ensure that the **Change Type** is **Added or Modified**. If not,
    then select it from the drop-down menu.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image29.png)

7.  From the **Table Name** dropdown menu, search for and
    select **Inventories**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image30.png)

8.  Remove the default selection in the **Scope** field and select
    **Organization** from the drop-down menu.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image31.png)

9.  Collapse the **When a row is added, modified or deleted** panel
    using collapse icon on top right corner of the panel.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image32.png)

10. Select the **Condition** step.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image33.png)

11. Observe that Copilot has already added values.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image34.png)

12. But we don’t want these values, i.e., body/quantity. To correct
    that, follow the upcoming steps.

13. Select the **Choose a value** box, remove the default selection, and
    select the dynamic content icon. 

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image35.png)

14. Search for the +++ Quantity+++ column and select it. 

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image36.png)

15. Similarly, remove the second default value and select the dynamic
    content icon.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image37.png)

16. Search for the +++**Reorder points**+++ column and select it. 

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image38.png)

17. Close the **Condition** pane.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image39.png)

18. Expand the **Condition** node.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image40.png)

19. Select the** Start and wait for an approval **action from the flow.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image41.png)

20. From the **Approval Type** dropdown menu, select **Approve/Reject -
    First to respond**.

> After you select the **Approval Type**, more parameters are now
> available.
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image42.png)

21. Under the **Title** field, enter +++**Approve to Restock**+++ - and
    click on the dynamic content icon.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image43.png)

22. Search for +++**Candy Name**+++ and select it. 

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image44.png)

23. In the **Assigned to** field, enter +++MOD+++ and select MOD
    Administrator credentials from the suggestion.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image45.png)

24. In the **Details** field, enter the given text: Select
    Candy(Type)\>from the dynamic content.

> +++Hi Sir,+++
>
> \<Candy(Type)\> +++is out of stock - for customers to place an order.
> Please approve to restock.+++
>
> +++Thanks+++
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image46.png)

25. Close the **Start and wait for an approval **pane.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image47.png)

26. Select the **Condition** step.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image48.png)

27. Select the **Choose a value** box, select the dynamic content icon. 

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image49.png)

28. Select the **Outcome** listed under the **Start and wait for an
    Approval** action.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image50.png)

29. Select the condition as **is equal to** and enter the value
    as **Approve**. Close the **Condition** pane.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image51.png)

30. Expand another **Condition** step and select the **Update a row**
    step.

> ![](./media/image52.png)

31. Remove the default selection for the **Table name** field.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image53.png)

32. Select **Inventories** table from the drop-down menu.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image54.png)

33. Remove the default selection, select the **Row Id** field and then
    select the dynamic content icon. 

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image55.png)

34. Search for a unique identifier column from the Inventories table and
    select it. In this case, it is **Inventory**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image56.png)

35. Click the **Advanced Parameters** drop-down and select
    the **Quantity** column. 

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image57.png)

36. Click inside the **Quantity** field and select the **Function**
    icon.

> ![](./media/image58.png)

37. Enter the below function (you type in your app) and collapse the
    action.

> **Note:** The below function does not work for you as your column
> schema name will be different. Go to the table --\> column, and copy
> the schema name.
>
> +++add(triggerBody()?\['cr6cd_Quantity'\],triggerBody()?\['cr6cd_candyInStock'\])+++
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image59.png)

38. Close the **Update a row** pane.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image60.png)

39. Rename the flow - **Candy Restock Flow**.

> ![A screenshot of a search box AI-generated content may be
> incorrect.](./media/image61.png)

40. Save the flow by selecting the **Save** button in the upper-right
    corner of the screen.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image62.png)

**Task 2: Test the restock flow**

1.  Switch back to the **Power Apps** tab or open it
    using +++https://make.powerapps.com/+++. From the left pane, select
    Apps and then open the **Candy Inventory Management App**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image63.png)

2.  Select the **Inventories** screen.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image64.png)

3.  Select **+New.**

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image65.png)

4.  Enter the **Quantity** value **less than the reorder
    points** and **commit** changes. Enter **Inventory 3** as an
    **Inventory**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image66.png)

5.  Switch back to the **Power Automate** tab. Select the **App
    launcher** from the top-left corner.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image67.png)

6.  You should have received an email to restock. Review the email, then
    click **Approve** and **Submit**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image68.png)

7.  Switch back to the **Power Automate** tab. From the left pane,
    select **My flows** \> **Candy Restock Flow**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image69.png)

8.  The flow is successful now. 

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image70.png)

**Summary**: In this lab, you have learnt to build an inventory
management app with the help of Copilot and implement a Power Automate
flow to trigger restock requests based on inventory levels.
