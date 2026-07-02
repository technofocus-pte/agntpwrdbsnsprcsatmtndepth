# **Lab 5: Create an agent and agent flow for a healthcare organization**

**Objective**: In this lab, you will learn to create an agent that helps
with patient diagnosis of various pains. The scenario used here is - A
healthcare organization provides multiple levels of care and services to
its patients. It wants to use Microsoft Copilot Studio to build an agent
that helps with patient diagnosis of various pains. The agent captures
the given information: Patient age, Patient gender, and Primary
symptoms. The agent summarizes this information into a text string. The
agent then sends this string to a generative service to check symptoms
and provide a potential diagnosis. You use an agent flow to summarize
the information for better consumption.

## **Exercise 1: Create an agent**

In this exercise, create an agent that captures this information and
provides a potential diagnosis.

**Task 1: Create a healthcare agent**

1.  Sign in to **Microsoft Copilot Studio** with your **Office 365 admin
    tenant** credentials using +++https://copilotstudio.microsoft.com/+++.

2.  Select the **Dev One** environment from the environment selector.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image1.png)
    
     **Note**: If you're unable to select the **Dev One** environment as
     shown in the image below, then follow the steps below.
    
     ![image](./media/image2.png)
    
     Open the Power Platform Admin Center using
     +++https://admin.powerplatform.microsoft.com/+++. From the left-hand
     menu, select **Manage**, then choose **Environments** > **Dev One**.
     Copy the **Environment ID**, and update the Copilot Studio link
     accordingly, as shown in the image below.
    
     ![image](./media/image3.png)
    
     Navigate back to the Copilot Studio tab and open
     +++https://copilotstudio.microsoft.com/environments/**< EnvironmentID
     >**/home+++ (Replacing **< EnvironmentID >** with the value fetched above)
    
     ![](./media/image4.png)

3.  On the **Welcome to Copilot Studio** pop-up, select **Skip.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image5.png)

4.  On the left pane, select **Agents** and then select **+Create blank
    agent**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image6.png)

5.  The **Overview** page for your agent appears.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image7.png)

6.  In the **Details** section, select **Edit**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image8.png)

7.  Rename the agent as **Symptom Checker** and then select **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image9.png)

8.  Select the **Topics** tab.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image10.png)

9.  Select **Add a Topic**. On the menu that appears, select **From
    blank**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image11.png)

10. Change the name of the topic from **Untitled** to **Check
    Symptoms**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image12.png)

11. Under **describe what the topic does**, enter: +++**This topic
    captures symptoms that a patient is experiencing and provides a
    potential diagnosis. It can answer questions like "I want to check
    my symptoms."**+++

     ![A screenshot of a computer screen AI-generated content may be incorrect.](./media/image13.png)

12. Select the **Add node** button,

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image14.png)

13. Select **Send a message** node.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image15.png)

14. In the **Message** box, enter: +++**I'm happy to help you. I just need to capture more details.**+++

     ![](./media/image16.png)

15. Select the **Add node** button, and then select **Ask a Question**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image17.png)

16. For the question text, enter: +++**How old are you?**+++

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image18.png)

17. Select the arrow next to **Multiple Choice Options**. On
    the **Choose information to identify** pane, select **Age**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image19.png)

18. Under **Save user response as**, select **Var1**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image20.png)

19. Change the variable name to +++**Age**+++. Close the **Variable
    properties** pane.

     ![Screens screenshot of a computer screen AI-generated content may be incorrect.](./media/image21.png)

20. Select the **Add node** button, and then select **Ask a Question**.

     ![](./media/image22.png)

21. For the question text, enter: +++**What was your gender at
    birth?**+++

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image23.png)

22. Select the arrow next to **Multiple Choice Options**. On
    the **Choose information to identify** pane, select the **User's
    entire response**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image24.png)

23. Under **Save user response as**, select **Var1**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image25.png)

24. Change the variable name to **Gender**. Close the **Variable
    properties** pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image26.png)

25. Select the **Add node** button, and then select **Ask a Question**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image27.png)

26. For the question text, enter: +++**Describe to me the symptoms that
    you're having.**+++

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image28.png)

27. Select the arrow next to **Multiple Choice Options**. On
    the **Choose information to identify** pane, select the **User's
    entire response**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image29.png)

28. Under **Save user response as**, select **Var1**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image30.png)

29. Change the variable name to **Symptom**. Close the **Variable
    properties** pane.

    ![A screenshot of a computer screen AI-generated content may be incorrect.](./media/image31.png)

30. Select the **Save** button and leave the **Topics** tab open.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image32.png)

31. Select the **Add node** icon. Select **Add a tool** and then select
    **New Agent flow**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image33.png)

## **Exercise 2: Create an agent flow**

### **Task 1: Specify and configure an event to start the flow**

 First, select the trigger (event) that starts the flow. In this case,
 an agent triggers the agent flow. This setup enables you to call the
 flow in different topics.

1.  After selecting the **New Agent flow** tool in the topic, you will
    be navigated to the **Designer** tab of the Agent flow. You can see
    there are two nodes added already. One is **When an agent calls the
    flow**, and the other is **Respond to the agent.**

     ![](./media/image34.png)

2.  Select **When an agent calls the flow**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image35.png)

3.  Select **Add an Input**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image36.png)

4.  Select **Number**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image37.png)

5.  Change the name from **Number** to +++**Patient Age**+++.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image38.png)

6.  Select **Add an Input** again.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image39.png)

7.  Select **Text**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image40.png)

8.  Change the name from **Input** to +++**Patient Gender**+++.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image41.png)

9.  Select **Add an Input** one last time.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image42.png)

10. Select **Text**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image43.png)

11. Change the name from **Input** to +++**Primary Symptom**+++.

     ![A screenshot of a computer screen AI-generated content may be incorrect.](./media/image44.png)

**Task 2: Specify an action**

1.  Under the **When an agent calls the flow** trigger, select **Insert
    the action(+)**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image45.png)

2.  On the **Add an action** pane, search for and select **Run a
    prompt**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image46.png)

3.  On the **Run a prompt** pane, set the **Prompt** box to **AI
    Summarize**. Select it from the drop-down menu.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image47.png)

4.  In the input text, select **Dynamic value** (lightning bolt).

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image48.png)

5.  Under **When an agent calls the flow**, select the following dynamic
    values one by one:

    - **Patient Age**

    - **Patient Gender**

    - **Primary Symptom**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image49.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image50.png)

6.  Select **Respond to the agent**.

     **Note**: If the action is not automatically added to the flow, then
     under the **Run a Prompt** step, select **Insert a new step (+)**.
    
     ![](./media/image51.png)

7.  Select **Add an output**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image52.png)

8.  Select **Text**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image53.png)

9.  Set the name of the output to +++**Summarized**+++ having **Text**
    data type.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image54.png)

10. In the **Enter a value to respond with** box, select **Dynamic
    value** (lighting bolt).

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image55.png)

11. Search for and select **Body**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image56.png)

12. Select **Save draft**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image57.png)

13. Select the **Overview** tab.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image58.png)

14. In the **Details** section, select **Edit**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image59.png)

15. Change the name from **untitled** to +++**Summarize Symptoms**+++.
    Select the **Save** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image60.png)

16. Switch back to the **Designer** tab.

     ![](./media/image61.png)

17. Select **Publish**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image62.png)

**Task 3: Add a flow to the topic**

1.  Select the **Agents** from the left pane and then click on the
    **System Checker** agent to open it.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image63.png)

2.  Select the **Topics** tab.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image64.png)

3.  Select the **Check Symptom** topic.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image65.png)

4.  Below the last node in the topic, select the **Add node** button.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image66.png)

5.  Select **Add a tool** node and then select the **Summarize
    Symptoms** agent flow that you created earlier.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image67.png)

6.  Configure the action as follows and then close the **Select a
    variable** pane.

     **Patient Age (Number)**: Select the **Age** variable that you created earlier.
    
     **Patient Gender (String):** Select the **Gender** variable that you created earlier.
    
     **Primary Symptom (String):** Select the **Symptoms** variable that you created earlier.
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image68.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image69.png)

7.  Select the **Add node** button. On the menu that appears,
    select **Send a message**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image70.png)

8.  Select the **Insert variable {x}** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image71.png)

9.  Select **Summarized text**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image72.png)

10. Select the **Save** button.

     ![](./media/image73.png)

## **Exercise 3: Test the agent**

**Task 1: Test your agent**

1.  Ensure that your **Test your agent** pane is open. If not, select
    the **Test** icon from the upper left corner of the screen.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image74.png)

2.  In the **Ask a question or describe what you need** box, enter the
    following text: **I have some symptoms that I want checked.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image75.png)

3.  Enter an **Age** value, and then select the **Enter** key.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image76.png)

4.  Enter a **Gender** value, and then select the **Enter** key.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image77.png)

5.  When you're asked for your symptom, enter the following
    text: +++**I'm experiencing severe, sharp pain in my hands. The pain
    has been getting worse and is pretty much all the time.**+++ Select
    the **Enter** key.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image78.png)

6.  Observe the response from the agent.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image79.png)

**Summary**: In this lab, you created an agent that captures the
information from the patient and provides a potential diagnosis.  You
also built an agent flow that uses a patient's age, gender, and symptoms
to create a summary for a Copilot Studio agent.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image80.png)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image81.png)

![A screenshot of a computer error AI-generated content may be
incorrect.](./media/image82.png)
