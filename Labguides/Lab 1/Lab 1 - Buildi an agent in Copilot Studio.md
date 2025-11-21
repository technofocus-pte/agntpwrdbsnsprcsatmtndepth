# **Lab 1: Build an agent in Microsoft Copilot Studio with the new AI capabilities**

**Objective**: In this lab, you will learn to create an agent to collect
user’s information and summarize the details using an Adaptive card.

## **Exercise 1: Create an agent**

In this exercise, you will create a Real Estate Booking Service agent to
collect a user's full name, email, address of the property, and date and
time of the showing.

1.  Sign into **Microsoft Copilot Studio** with your **Office 365 admin
    tenant** credentials
    using +++https://go.microsoft.com/fwlink/?LinkId=2107702+++

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image1.png)

2.  Fill up the following required information and then select **Get
    Started**.

     **Country or Region** – United States

     **Job title** – Your job title

     **Business phone number** – Your phone number

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image2.png)

3.  Under Confirmation details step, select **Get Started**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image3.png)

4.  Select **United States** as your country/region and then
    select **Get Started**.

     ![](./media/image4.png)

5.  Select **Dev One** environment from environment selector.

     ![A screenshot of a chat AI-generated content may be incorrect.](./media/image5.png)

     **Note**: If you're unable to select the **Dev One** environment as shown in the image below then follow the steps            below.

     ![image](./media/image6.png)

     Open the Power Platform Admin Center using +++https://admin.powerplatform.microsoft.com/+++. From the left-hand
     menu, select **Manage**, then choose **Environments** > **Dev One**. Copy the **Environment ID**, and update the             Copilot Studio link accordingly, as shown in the image below.

     ![image](./media/image7.png)

     Navigate back to the Copilot Studio tab and open +++https://copilotstudio.microsoft.com/environments/>**\<
     EnvironmentID>**/home+++ (Replacing **< EnvironmentID >** with the value fetched above)

     ![](./media/image8.png)

6.  On the **Welcome to Copilot Studio** pop-up, select **Skip.**

     ![](./media/image9.png)

7.  Select **+ Create** from the left navigation menu and then
    select **New agent**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image10.png)

8.  A page appears with two panes where you can set up your agent on the
    left-hand side and test it on the right-hand side. The left-hand
    pane has two tabs: **Describe** and **Configure**. Select
    **Configure**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image11.png)

9.  Name your agent as +++**Real Estate Booking Service**+++.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image12.png)

10. In the **Description** text box, enter **Create bookings for real
    estate properties.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image13.png)

11. In the **Instructions** text box, enter +++**Speak courteously and
    mimic the behavior of a real estate agent.**+++

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image14.png)

12. Select **Create**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image15.png)

13. To improve visibility, close the **Test your agent** pane.

     ![](./media/image16.png)

14. With your agent created, select **Topics** from the above horizontal
    pallet.

     ![](./media/image17.png)

15. Select the **+ Add a topic** dropdown menu. Select **Add from
    description with Copilot**.

     ![](./media/image18.png)

16. A new window appears asking you to **Name your topic** and provide a
    description in the **Create a topic to...** space.

17. In the **Name your topic** field, enter the following text:

     +++**Book a Real Estate Showing**+++

18. In the Create a topic to... field, enter the following text:

     +++**Collect a user's full name, email, address of the property, and date and time of the showing**+++

     Select **Create**.

     ![](./media/image19.png)

     A new topic displays with the generated trigger phrases.

     ![](./media/image20.png)

     **Note:** Remember, your generated content might appear differently than what's shown in this lab.

     Multiple question nodes, entity selection, and variable naming should also display.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image21.png)

19. Look for and then select the **What is your email
    address?** question node.

     ![](./media/image22.png)

20. Select the **’What is your email address'** message field.

     ![](./media/image23.png)

21. Enter [**Thank you**](urn:gd:lg:a:send-vm-keys) in the message box
    and then select **{X}** icon to insert variable.

    ![](./media/image24.png)

22. Select **Name** or **FullName** variable.

    ![](./media/image25.png)

    ![A screenshot of a computer AI-generated content may beincorrect.](./media/image26.png)

23. Select **Save**.

     ![](./media/image27.png)

## **Exercise 2: Add nodes with natural language**

In this exercise, you will add an Adaptive card property to your agent
which helps you to summarize the entered information and to prompt the
user if the details are correct.

1.  Make sure that no node is selected by clicking in the empty space
    around the nodes.

2.  In the **Edit with Copilot** panel, in the **What do you want to
    do?** field, enter the following text:

     +++Summarize the information collected in an adaptive card+++

3.  Select **Update**.

     ![](./media/image28.png)

4.  A message node with an Adaptive Card is added to the end of the
    topic.

     ![](./media/image29.png)

5.  Select the **Adaptive Card**. The Adaptive Card properties should
    appear on the right of the screen.

     ![](./media/image30.png)

6.  Opening the Adaptive Card properties closes the **Edit with
    Copilot** panel; therefore, you need to select the **Copilot** icon
    to reopen it.

     ![](./media/image31.png)

7.  Make sure that no node is selected by clicking in the empty space
    around the nodes.

8.  In the **What do you want to do?** field, enter the following text:

     +++Add a new multiple choice question to prompt the user if the details are correct with two options Yes or No+++

9.  Select **Update**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image32.png)

10. A new question node is added to the end of the topic with options
    for the user to select.

     ![](./media/image33.png)

11. Select **Save**.

     ![](./media/image34.png)

12. Close the **Edit with Copilot**.

     ![](./media/image35.png)

13. On right side of the screen, you can see the **Test your
    agent** pane is already opened. If not, click on **Test**.

     ![](./media/image36.png)

14. When the **Conversation Start** message appears, your agent will
    start a conversation. In response, enter a trigger phrase for the
    topic that you've created:

     +++I want to book a real estate showing+++

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image37.png)

     The agent responds with the "**What is your full name?**" question, as shown in the following image.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image38.png)

15. Enter the rest of the information:

     Full name: +++Brooke Gray+++
    
     Email address: +++abc@example.com+++ 
    
     Address: +++555 Oak Lane, Denver, CO80203+++ 
    
     Date and Time: +++25/12/2025 10:00 AM+++
    
     ![](./media/image39.png)

16. You can see that copilot has generated the adaptive card.

     ![](./media/image40.png)

17. Select **Yes** or **No** for the question **Are these details
    correct?**

     ![](./media/image41.png)

 **Summary**: In this lab, you created a Real Estate Booking Service agent which helps you to collect user’s information.         You have used an Adaptive card to summarize information collected from the user and to enhance the conversation              experience.

