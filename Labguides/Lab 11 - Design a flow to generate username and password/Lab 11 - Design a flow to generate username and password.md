# **Lab 11 - Design a flow to generate a username and password​**

**Objective:** The objective of this lab is to create and test a Power
Automate Desktop flow that generates a username and a random password
based on user input. By completing this lab, participants will learn how
to design and automate the flow using Power Automate Desktop actions,
including handling text manipulation and generating random text.

## **Exercise 1: Create a Power Automate Desktop Flow**

1.  Navigate to +++https://make.powerautomate.com/+++ and if
    required, sign in with your Office 365 tenant credentials.

2.  From the top left corner, select **+ New** > **Flow**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image1.png)

3.  On the **Create a flow** screen, enter the **Flow name** - +++**Generate Username and Password**+++ then select **Create**.

     ![A screenshot of a computer screen AI-generated content may be incorrect.](./media/image2.png)

4.  Close the Copilot pane to maximize visibility.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image3.png)

5.  From the **Actions** pane to the left of the screen, search for the
    +++**Display input dialog**+++ action and double-click the **Display
    input dialog** action to select.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image4.png)

6.  Set the **Input dialog title** property to +++**Name Input**+++ and
    the **Input dialog message** property to +++**Please enter your
    first and last name (for example, Adele Vance)**+++. This action
    displays a message that prompts the user for input. Click on
    the **Save** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image5.png)

7.  From the **Actions** pane to the left of the screen, search for the
    +++**Split text**+++ action and double-click the action to select.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image6.png)

8.  In the **Text to split** field of the Split text action,
    enter +++**%UserInput%**+++ and then click on **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image7.png)

9.  From the **Actions** pane, search for the +++**Change text case**+++
    action and double-click the **Change text case** action to select.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image8.png)

10. In the **Text to convert** field, enter +++**%TextList\[0\]%**+++.
    With the index of a list type variable, we provided the first item
    of the list, which is the first name.

     ![A close-up of a computer screen AI-generated content may be incorrect.](./media/image9.png)

11. Set the **Convert to** as **Lower case** and then click on
    the **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image10.png)

12. From the **Actions** pane, search for the +++**Change text case**+++
    action and double-click the **Change text case** action to select.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image11.png)

13. In the **Text to convert** field, enter +++**%TextList\[1\]%**+++.
    With the index of a list type variable, we provided the first item
    of the list, which is the first name.

     ![A close-up of a computer screen AI-generated content may be incorrect.](./media/image12.png)

14. Set the **Convert to property** to **Lower case** and then
    click **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image13.png)

15. From the **Actions** pane, search for the +++**Get subtext**+++
    action and double-click the **Get subtext** action to select.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image14.png)

16. In the **Original text** field, enter +++**%TextWithNewCase%**+++.
    In the **Start index** section, select **Character position**. Set
    **Character position** to +++**0**+++.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image15.png)

17. In the **Length** section, select **Number of chars** from the
    drop-down menu. Set the number of chars value to +++**1**+++. This
    setting gets the first character of the text string.

18. Select **Save** in the lower part of the dialog.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image16.png)

19. To generate a random password, search for the +++**Create random
    text**+++ action from the left search bar, double-click the action
    to add in the flow.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image17.png)

20. The action’s properties can be left at their default values. Then
    select **Save.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image18.png)

21. From the **Actions** pane, search for the +++**Display message**+++
    action and double-click the action to select.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image19.png)

22. In the **Message box title** field, enter +++**Username &
    Password**+++.

     ![A screenshot of a login box AI-generated content may be incorrect.](./media/image20.png)

23. In the **Message to display** field, enter the following content:

     +++Hello, %UserInput%, your username is: %SubText%%TextWithNewCase2%
     Your temporary password is: %RandomText%+++

21. The username (first letter of first name, combined with family name)
    is displayed, and the result of the **Generate random text** action
    shows as the user’s password. Click on the **save** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image21.png)

22. The **completed flow** should look like the following figure.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image22.png)

## **Exercise 2: Test the flow**

1.  Click on the **Run** button to test the flow.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image23.png)

2.  Enter the **First and Last Name – Peter Johnson**, for testing
    purposes, and click on the **Ok** Button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image24.png)

3.  The **Final output** of the test case looks like the one below.
    Select **Ok**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image25.png)

4.  Click the **Save draft** button to save the flow.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image26.png)

## **Exercise 3: Create a flow with Copilot**

In this exercise, you will create the flow with the help of Copilot. You
will describe in natural language what you want to achieve. Here, you
are building the flow using Copilot on the home page.

1.  Go to the **Home** page of the Power Automate Desktop app.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image27.png)

2.  To create a flow from the home page, type the given prompt in
    Copilot’s chat area and then select the **submit** icon.

     **Prompt** – +++Create a Desktop flow to generate a username and a
     random password based on user input (for example, *Adele Vance*). The
     username should be constructed by taking the first letter of the first
     name and the entire last name, all in lowercase+++
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image28.png)

3.  Once you submit your prompt, Copilot processes it and launches the
    designer with the newly generated flow.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image29.png)

4.  Close the Copilot pane to maximize visibility.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image30.png)

5.  Review the flow.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image31.png)

6.  Click on the **Run** button to test the flow.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image32.png)

7.  Enter the **First and Last Name – Peter Johnson** for testing
    purposes,- and click on the **Ok** Button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image33.png)

8.  The **Final output** of the test case looks like the one below.
    Select **Ok**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image34.png)

9.  Click the **Save draft** button to save the flow.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image35.png)

**Summary:** In this lab, participants successfully designed and tested
a Power Automate Desktop flow that generates a username and random
password based on user input. By utilizing text manipulation actions,
such as splitting, changing case, and generating random text,
participants gained practical experience in automating user-specific
tasks. The flow demonstrates how to dynamically create a username and
password using basic Power Automate Desktop features. This lab lays the
foundation for building more complex automation flows in future tasks.
