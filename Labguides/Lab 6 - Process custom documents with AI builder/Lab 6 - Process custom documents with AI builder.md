# **Lab 6 - Process custom documents with AI builder**

**Objective:** In this lab, you will learn how to create an AI model
using AI Builder in Power Automate. The model will be trained to extract
custom information, such as invoice numbers, customer IDs, total
amounts, and due dates, from documents like invoices. You will learn how
to sign into AI Builder, choose document types, define fields to
extract, upload documents for training, and finally, integrate the
trained model with Power Automate and Power Apps.

## **Exercise 1: Create your first model**

### **Task 1: Sign in to AI Builder**

1.  Navigate to the Power Automate with the help of
    +++https://make.powerautomate.com/+++ and if asked, sign in using
    the Office 365 admin tenant account.

2.  Select the environment - **Dev one** from the top bar.

     ![](./media/image1.png)

3.  Navigate to the left pane and select **AI Hub**, then click on **AI
    Models.** If you don't see AI Hub, click on **More** to locate it.

     ![](./media/image2.png)

4.  Choose the **Extract custom information from documents** option.

     ![](./media/image3.png)

5.  Scroll down and select **Create custom model** to proceed.

     ![](./media/image4.png)

### **Task 2: Choose document type**

1.  When choosing the document type, you have three options:

    - **Fixed template documents:** This option is ideal when, for a
      given layout, the fields, tables, checkboxes, and other items can
      be found in similar places. You can teach this model to extract
      data from structured documents that have different layouts. This
      model has a quick training time.

    - **General documents:** This option is ideal for any kind of
      documents, especially when there is no set structure or when the
      format is complex. You can teach this model to extract data from
      structured or unstructured documents that have different layouts.
      This model is powerful but has a long training time.

    - **Invoices:** Invoice documents are standard account payable
      forms. This model type comes with standard fields, and you can
      teach this model to extract additional custom data or update the
      standard data.

2.  Select **Fixed template documents** and click **Next**.

     ![](./media/image5.png)

### **Task 3: Choose information to extract**

Define the fields and tables you want your model to extract. We'll
extract the following fields:

- Invoice number

- Customer ID

- Total amount

- Due date

1.  Click **+** **Add** and select **Text** **field**, then
    click **Next**.

     ![](./media/image6.png)
    
     ![](./media/image7.png)

2.  Enter the text field name as +++**Invoice Number**+++ and
    select **Done**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image8.png)

3.  Repeat this by selecting the **Text** **field**, name it as
    +++**Customer ID**+++, and select **Done**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image9.png)

4.  Click **+ Add** and select the **Number field**, then click
    **Next**.

     ![](./media/image10.png)
    
     ![](./media/image11.png)

5.  Enter the number field name as +++**Total amount**+++ and
    select **Done**.

     ![](./media/image12.png)

6.  Click **+ Add** and select **Date** **field**. Select **Next**.

     ![](./media/image13.png)

     ![](./media/image14.png)

7.  Enter the date field name as +++**Due Date**+++ and select **Done**.

     ![](./media/image15.png)

8.  To extract table details from the invoice, we will create a table
    named Items with columns Description and Item total. To do so,
    click **+ Add** and select **Table**.

     ![](./media/image16.png)

9.  Select **Table** and click **Next**.

     ![](./media/image17.png)

10. Define the table name as +++**Items**+++.

11. Select **Column1**, click on **Edit column** and rename it to
    +++**Description**+++, then click **Confirm**.

     ![](./media/image18.png)
    
     ![](./media/image19.png)

12. Click **+ New column**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image20.png)

13. Enter the column name as +++**Item total**+++, then select **Add**.
    Finally, click **Done**.

     ![](./media/image21.png)

14. Click **Next** to proceed to the next step in your model.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image22.png)

### **Task 4: Define collections and upload documents**

Define collections and upload documents. A collection groups documents
with the same layout. Create a collection for each unique layout your
model needs to process. Since there are two invoice providers using
different templates, we'll create two collections.

1.  Select the **New collection** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image23.png)

2.  You've now created a space to add a collection called **Collection
    1**. Rename the first collection to **Adatum**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image24.png)

3.  Add a second **New collection.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image25.png)

4.  Rename the second collection to +++Contoso+++.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image26.png)

5.  Click on the **Adatum** collection. A panel appears on the right
    side of your screen, prompting you to add documents. Select **Add
    documents** to continue.

     ![](./media/image27.png)

6.  From the **Select source** window, select **My device**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image28.png)

7.  For **Adatum**, find the five documents that are available
    in **C:\LabFiles\Adatum\Train** folder. Then select **Open**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image29.png)

8.  An **Upload documents** pop-up window appears. Select the **Upload 5
    documents** button to continue. Select **Done** to close the pop-up.

     ![](./media/image30.png)
    
     ![](./media/image31.png)

9.  Click on the **Contoso** collection. A panel appears on the right
    side of your screen, prompting you to add documents. Select **Add
    documents** to continue.

     ![](./media/image32.png)

10. From the **Select source**, select **My device**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image33.png)

11. For **Contoso**, find the five documents that are available in
    **C:\LabFiles\Contoso\Train** folder. Then select **Open**.

12. An **Upload documents** pop-up window appears. Select the **Upload 5
    documents** button to continue. Select **Done** to close the pop-up.

     ![](./media/image34.png)

     ![](./media/image35.png)

13. Once you've uploaded the sample documents to both collections,
    select **Next** to continue.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image36.png)

### **Task 5: Tag documents**

Start teaching your AI model how to extract the fields and tables by
tagging the sample documents you've uploaded. As you tag the expected
fields in each document, a check will appear over that document, and the
red dot at the top corner will disappear.

1.  Select the **Contoso** collection from the right panel to begin
    tagging.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image37.png)

2.  **Tag Fields:**

    - Start by tagging fields like **Invoice Number,** **Due date, and
      Total amount.**

    - Draw a rectangle around each field in the document, then select
      the corresponding field name.

    - Resize your selection if needed. Hovering over words will show
      light blue boxes, indicating where you can draw rectangles.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image38.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image39.png)
    
     ![A screenshot of a computer screen AI-generated content may be incorrect.](./media/image40.png)

3.  Go to **Customer ID** in the **Contoso** collection, select the
    ellipsis **(…)** next to the field on the right panel, and
    choose **Not available in the document**.

     ![A screenshot of a computer screen AI-generated content may be incorrect.](./media/image41.png)

4.  **Tag Tables:**

    - Draw a rectangle around the table you want to tag and select the
      table name.

    - Draw rows by left-clicking between row separators.

    - Draw columns by pressing Ctrl + left-click (or ⌘ left-click on
      macOS).

    - Assign the headers by selecting the header column and mapping it
      to the desired one.

    - If you've tagged the table's header, select Ignore first row to
      prevent it from being extracted as content.

     ![A screenshot of a computer screen AI-generated content may be incorrect.](./media/image42.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image43.png)
    
     ![A screenshot of a computer screen AI-generated content may be incorrect.](./media/image44.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image45.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image46.png)
    
     ![A screenshot of a computer screen AI-generated content may be incorrect.](./media/image47.png)

5.  Tag all five documents with the same process. Once you've tagged a
    document, move to the next one using the navigation arrows at the
    top right of the document preview.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image48.png)

6.  Now select the **Adatum** Collection.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image49.png)

7.  **Tag Fields:**

    - Start by tagging fields like **Invoice Number, Customer ID and
      Total amount.**

    - Draw a rectangle around each field in the document, then select
      the corresponding field name.

    - Resize your selection if needed. Hovering over words will show
      light blue boxes, indicating where you can draw rectangles.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image50.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image51.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image52.png)

8.  Select the three dots next to the **Due Date** field and
    select **Not available in collection.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image53.png)

9.  **Tag Tables:**

    - Draw a rectangle around the table you want to tag and select the
      table name.

    - Draw rows by left-clicking between row separators.

    - Draw columns by pressing Ctrl + left-click (or ⌘ left-click on
      macOS).

    - Assign the headers by selecting the header column and mapping it
      to the desired one.

    - If you've tagged the table's header, select Ignore first row to
      prevent it from being extracted as content.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image54.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image55.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image56.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image57.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image58.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image59.png)

10. Tag all five documents with the same process. Once you've tagged a
    document, move to the next step using the navigation arrows at the
    top right of the document preview.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image60.png)

### **Task 6: Model summary and train**

1.  Select the **Next** button at the bottom of the screen.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image61.png)

2.  Review the **Model summary**. Under Information to extract you'll
    see that Customer ID and Due Date only appeared in five examples out
    of **10**, whereas everything else appeared in all 10 examples.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image62.png)

3.  If everything looks acceptable, select **Train**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image63.png)

4.  Click on the **Go to model** button while training.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image64.png)

## **Exercise 2: Use your model**

### **Task 1: Quick test**

1.  After your model completes training, click on the model name to view
    important details about your newly trained model on a details page.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image65.png)

2.  To see your model in action, select **Quick test**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image66.png)

3.  Select **Upload from my device**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image67.png)

4.  Drag and drop or upload an image from your device -
    C:\Labfiles\Contoso\Test to test. From the previous sample data, use
    the files from the **Test** folder that we didn’t use for training.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image68.png)

5.  You can now view the detected fields that you chose and the
    associated confidence scores for retrieving the individual fields
    compared to the trained model. Click on the **Close** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image69.png)

### **Task 2: Publish your model**

1.  Your model can't be used until you publish it. If you're satisfied
    with your model, select **Publish** to make it available for use.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image70.png)

### **Task 3: Use your model in Power Apps**

Now that your model is published, you can use your Document processing
model in a canvas app. A special component is available for you to add
that analyzes any image and extracts the text based on your trained
Document processing mode.

1.  Select **Use model**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image71.png)

2.  Select the **Build intelligent apps** option to begin the canvas app
    creation experience.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image72.png)

3.  You will be navigated to the Power Apps portal. Select **Skip** on
    the welcome window. Select **Got it** on the **This is a premium
    component window**, if it appears.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image73.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image74.png)

4.  Within your canvas app, a **Form processor component** is
    automatically added and linked to your published Document processing
    model.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image75.png)

5.  Next, we select which field from the invoice to display.
    Select **Insert** and then add a **Text label** component.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image76.png)

6.  With the label selected, make sure that the **Text** property is
    selected in the top left-hand corner. In the formula bar,
    write +++FormProcessor1.Fields+++. This code gives you access to the
    other properties from the model as well. For this exercise, we
    choose **Invoice Number**. The result looks similar to this image.

     ![](./media/image77.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image78.png)
    
     **Note**: Notice how 'Invoice Number' is in single quotes in the
     previous image. This is because when the Invoice Number column was
     created, the column name was created with a space in between the
     words. If your columns weren't created with spaces, you don't need the
     single quotes, and your code may look like this image instead.
    
     ![](./media/image79.png)

7.  Place the label below the form.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image80.png)

8.  Next, we add a gallery so we can see the data from the items of the
    invoice. Select **Insert** and then **Vertical Gallery**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image81.png)

9.  In the **Items** property of the gallery,
    enter: +++FormProcessor1.Tables.Items+++

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image82.png)

10. Place the vertical gallery below the label.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image83.png)

11. Select **Play** on the upper right of the Power Apps studio to
    preview the app.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image84.png)

12. Select **Analyze** and then select the image that you used to quick
    test previously.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image85.png)

13. A preview of your document shows the **Invoice Number** and the
    items from the invoice.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image86.png)

**Summary:** In this lab, you learnt how to build and train a custom AI
model capable of extracting specific data fields from documents. You
learnt how to test the model with real-world data, integrate it into
automated workflows within Power Automate, and use it within a canvas
app in Power Apps. In this lab, you learnt how AI models can be used to
automate document processing and streamline business tasks, providing
practical experience in leveraging AI Builder for intelligent
automation.
