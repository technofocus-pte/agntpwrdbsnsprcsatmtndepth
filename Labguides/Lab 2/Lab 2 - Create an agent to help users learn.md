# **Lab 2: Create an agent to help users learn about Copilot Studio**

**Objective**: In this lab, you will learn to create an agent
called Friendly Tutor to help users learn about Copilot Studio using
knowledge from the official Copilot Studio documentation. You will learn
to add knowledge to your agent and test content changes in real time.
You will also learn to enable multilingual support in agent by adding
French and German as a secondary language to ensure the agent can
respond appropriately in multiple languages.

## **Exercise 1: Create and improve your agent** 

In this exercise, you will create an agent, add knowledge to it and test
it. You will also change your agent's introduction.

### **Task 1: Create an agent**

In this task, you will create an agent called Friendly Tutor to help
users learn about Copilot Studio using knowledge from the official
Copilot Studio documentation.

1.  Sign into **Microsoft Copilot Studio** with your **Office 365 admin
    tenant** credentials
    using !!https://copilotstudio.microsoft.com/!!
    You land on the **Home** page.

2.  Ensure that you are in **Dev One** environment.

    ![](./media/image1.png)

3.  Select **Agents** from the left navigation pane and then select **+ New agent**.

4.  A page appears with two panes where you can set up your agent on the
    left-hand side, and test it on the right-hand side. The left-hand
    pane has two tabs: **Describe** and **Configure**. Here, you will be
    using **Describe** tab which is selected already.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image3.png)

5.  For this example, tell Copilot you want to name your agent "Friendly
    Tutor." To do so enter the given prompt - !!Name the agent as Friendly Tutor!! and then click on the **Send** icon.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image4.png)

6.  Notice the new name appears in the test pane. The maximum length for
    the name is 30 characters.

     ![A screenshot of a chat AI-generated content may be incorrect.](./media/image5.png)

7.  Note that, you can refine the Copilot generated instructions for your agent
    but keep them simple for now. Just make sure you include information
    about what your agent helps users do. Notice the suggested prompts
    in the test pane are automatically updated, following your changes.
    The instructions can have up to 8,000 characters. In this case, we are going with the above prompt.

8.  Specify the desired conversation style and tone your agent should
    use, for example, enter the given prompt - !!Friendly Tutor should talk to users like a kind, patient teacher!! and then     click on the **Send** icon.

     ![](./media/image6.png)

9.  Add knowledge to your agent, if desired. For Friendly Tutor, tell
    Copilot you want to !!Use https://learn.microsoft.com/microsoft-copilot-studio as a knowledge source!!

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image7.png)

     **Note:** During the creation experience, your agent might need a few moments before it can start using its knowledge        sources.

10. Select **Create**.

     ![A screenshot of a chat AI-generated content may be incorrect.](./media/image8.png)

11. The **Overview** page for your agent appears. Now you can start testing and improving your agent. 

     ![](./media/image9.png)

### **Task 2: Test changes to your agent**

The best way to improve your agent? Test it. Make some changes. Test it
again. Repeat.

1.  Start by testing how your agent currently responds in the test chat.
    In the **Test you agent** pane, which is opened on right side of the
    screen, ask your agent a question. For example, enter !!How do I add a knowledge source?!! and select **Send** icon.

     ![](./media/image10.png)

2.  Notice the tone of your agent. In this example, the agent's
    instructions are to talk to users like a kind, patient
    teacher. What if you give your agent different instructions?

     ![](./media/image11.png)

3.  Go to the **Overview** page.

     ![](./media/image12.png)

4.  Update the instructions for your agent to use a different tone by
    selecting **Edit** button in the **Instructions** field.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image13.png)

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image14.png)

5.  Edit/replace sentence specifying the tone by the given sentence -
    !!Talk to users like Jane Austen!! and then click **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image15.png)

6.  Test your agent's new instructions with any question. Enter !!How do I add a knowledge source?!! and select **Send** icon.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image16.png)

7.  Notice how the response has changed.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image17.png)

### **Task 3: Change your agent's introduction**

Help your agent make a great first impression with a new introductory
message. This message lets users know what your agent does and
encourages them to interact with your agent.

1.  In the **Test your agent** chat, select your agent's introductory
    message. Click on the **New test session** icon at the top of the
    panel to restart the conversation.

     ![](./media/image18.png)

2.  Select the **Message** box then select the ellipsis (…) next to the
    message ‘Hello I am bot’.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image19.png)

3.  Replace the default message with your own by the message given
    below:

     !!Hello, I'm here to help you learn how to use Microsoft Copilot Studio. You can ask me all about agents: "What is an        agent?" "How do I make an agent?" "How do agents work?"!!

     ![](./media/image20.png)

4.  Select **Save**.

     ![](./media/image21.png)

5.  To test this change, click on the **New test session** icon at the
    top of the panel to restart the conversation in the **Test your
    agent** chat panel.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image18.png)

## **Exercise 2: Enable Multilingual Support and Publish Agent**

In this exercise, you will enable multilingual support in their agent by
adding French and German as a secondary language. you will download and
translate a localization file, upload the translated file, and create a
custom topic that detects the user's language and sets it dynamically.
This ensures the agent can respond appropriately in multiple languages.

### **Task 1: Add Secondary Language and Upload Localization File**

1.  From the top navigation bar, click on **Settings** to open the configuration options for the agent.

    ![](./media/image22.png)

2.  Within the **Settings** menu, locate and click on
    the **Languages** section from the left side pane. Here, you will
    see the current primary language configuration for the agent.
    The **Primary language** option should already be set
    to **English**.

     ![](./media/image23.png)

3.  Click on the **+ Add language** button to begin adding a new
    language. This will allow your agent to support multilingual
    conversations.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image24.png)

4.  In the language picker, search for **French (France)**. Once
    located, check the box next to it and click **Add** to include it as
    a supported language.

     ![](./media/image25.png)

5.  After French has been added, click the **Upload** button. This will
    allow you to manage translations for the agent's content in the
    newly added language.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image26.png)

6.  Click **Browse**.

     ![](./media/image27.png)

7.  Locate the localization_fr.json file in your **C:\Labfiles** folder
    on the VM and click **Open**.

     ![](./media/image28.png)

     **Note**: You can download the current language structure by
     selecting **Download localization file (JSON format)** and then
     translate it in the required language. In this lab you are using a
     pre-translated localization_fr.json file which is available in
     the **C:\Labfiles** folder.

     ![](./media/image29.png)

8.  Select **Upload translation updates**. When prompted again, click on
    the **Upload localization** button to confirm and apply the
    translated content to the agent.

    ![](./media/image30.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image31.png)

9.  Once the upload is successful, click on the **Close** button to exit
    the language management section.

     ![](./media/image32.png)

### **Task 2: Add Secondary Language (German) and Upload Localization File**

1.  Click on the **+ Add language** to add German language to the agent.

     ![](./media/image33.png)

2.  Enter **German** in the search field, select check box next to the
    **German** language and then click on the **Add** button.

     ![](./media/image34.png)

3.  After adding language click on the **Upload** button to add
    localization.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image35.png)

4.  Click **Browse**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image36.png)

5. Locate the localization_translated_de.js file in your Downloads
    folder, and click **Open**.

     ![](./media/image37.png)

6. Click **Upload translation updates**. When prompted again,
    click **Upload localization** to confirm and apply the translated
    content to the agent.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image38.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image39.png)

7. Once the upload is successful, click on the **Close** button to exit
    the language management section.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image40.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image41.png)

### **Task 3: Create a Topic to Detect Language and Set User Preference**

1.  Select **Agents** from the left navigation pane. Click on the **Friendly Tutor** agent to open it.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image42.png)

2.  Select **Topics** from top menu bar. Select **+ Add a topic** to
    create a new topic. Choose **From blank** to start with a blank
    template.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image43.png)

3.  In the new topic canvas, at the top of the screen, enter the
    name **Translator.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image44.png)

4.  In the canvas, you'll see a **Trigger node**. In
    the **Describe** section, enter the following phrases to trigger
    this topic:

    !!Can you translate this?, Translate for me, I need a translation, Help me translate, Translate this sentence, Translate     this text, Can you help me with translation?!!

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image45.png)

5.  Click on the **(+) Add icon under Trigger node**.

     ![A screenshot of a chat AI-generated content may be incorrect.](./media/image46.png)

6.  Click on the **Add a tool** and then select **New Prompt** to create
    new prompt flow.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image47.png)

7.  On the prompt screen, rename the tool (from the top-left)
    as **Detect language** to represent its functionality.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image48.png)

8.  In the **Instructions** pane, enter the following text !!Determine which language this message is written in:!!

   ![A screenshot of a computer AI-generated content may be incorrect.](./media/image49.png)

9.  At the bottom of the instructions panel, click on the  **Add
    content** button and then select **Text**.

   ![A screenshot of a computer AI-generated content may be incorrect.](./media/image50.png)

10. For **Name**, enter: !!Message!!, for **Sample Data**, enter: !!Message from the user!! and then click **Close** once done.

   ![A screenshot of a computer AI-generated content may be incorrect.](./media/image51.png)

11. In the **Model response** pane, change the output format
    to **JSON**, so the response returns structured language data.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image52.png)

12. Click on the **Test** button. The response should include a property
    showing the detected language, e.g., "language": "English".

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image53.png)

13. Click **Save** to add the prompt as a node on the topic canvas.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image54.png)

14. On the **Prompt node**, click on the **Input** button.

     ![](./media/image55.png)

15. Select the **System** variable **Activity.Text** as the input
    source.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image56.png)

16. Click on the **Output** field and then choose **Create new.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image57.png)

17. Click on the **Var1** variable and rename the variable
    as **DetectedLanguage** and close the **Variable properties** pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image58.png)

18. Under the Prompt node, click on the **+ icon** and choose **Add a
    condition** node.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image59.png)

19. Click on the **Select a variable** field and on the first condition
    line, choose the variable DetectedLanguage.structuredOutput.language

     ![](./media/image60.png)

20. In the **Enter or select a value field**, enter !!**French**!! to set
    the value to **French**.

     ![](./media/image61.png)

21. Under the French condition, click on the **+ icon**, go
    to **Variable management**, and choose **Set a variable value**.

     ![](./media/image62.png)

22. Click on the **Select a variable** field, navigate to the **System**
    variable and select **User.Language**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image63.png)

23. For value, click on the value field and select **French**.

     ![](./media/image64.png)

24. Click on the **+** Icon under prompt tool and the select **Add a
    condition** trigger.

     ![](./media/image65.png)

25. On the second condition line, choose the variable
    **DetectedLanguage.structuredOutput.language**.

     ![](./media/image66.png)

26. Enter !!**German**!! to set the value to **German**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image67.png)

27. Under the German condition, click **+**, go to **Variable
    management**, and choose **Set a variable value**.

     ![](./media/image68.png)

28. For variable, click on the select variable, navigate to **System**
    variable and select **User.Language**.

     ![](./media/image69.png)

29. For value, click on the value field and select **German.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image70.png)

30. Under **All other conditions**, click on the + Icon add select
    **Variable management** > **Set a variable** node.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image71.png)

31. For variable, click on the **Select a variable** field, navigate to
    **System** variable and select **User.Language**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image72.png)

32. For value, click on the value field and select **English.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image73.png)

33. Under the **French, German and English** variable node, there is
    a **+** node option which can add node under all of them. Click on
    the **+** icon.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image74.png)

34. Navigate to **Advanced** and then select **Generative Answer node**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image75.png)

35. Click on the **Input** ellipsis icon, navigate to **System** tab and
    select **Activity.Text** variable.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image76.png)

36. Click on the **Edit** option under data source.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image77.png)

37. Turn on **Search only selected sources** option. Select
    the **Name** check box it will select all the data knowledge source.

     ![](./media/image78.png)

38. Scroll select the **Customize** check box and then set the
    customization as **Medium**.

     ![](./media/image79.png)

39. Click the **Save** button at the top-right corner to complete the
    topic configuration.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image80.png)

### **Task 4: Publish the agent**

1.  From the top right corner, click on the **Publish** button.

     ![](./media/image81.png)

2.  Then again, select **Publish** for confirmation.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image82.png)

### **Task 5: Test the Agent**

Verify that the agent responds accurately to user input in both English
and French using test prompts in the built-in test chat window.

1.  Open the **Test your agent** panel from the right side of the Copilot
    Studio interface if it not already opened.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image83.png)

2.  In the message field, enter the following English prompt and click
    on the Execute button. Observe the agent's response and verify that
    it replies in English.

    **Prompt:** !!How do I add a knowledge source?!!

    ![](./media/image84.png)

3.  Now, enter the following **French** prompt in the test field and
    click on **Execute**. Observe the response to confirm that the agent
    replies appropriately in French, based on the uploaded localization
    content.

    **Prompt:** !!Comment ajouter une source de connaissances?!!

    ![](./media/image85.png)

 **Summary**: In this lab you learnt to create an agent by adding
 knowledge to your agent and testing content changes in real time. You
 also learnt to enable multilingual support in the agent. You uploaded
 the translated localization file and created a custom topic that
 detects the user's language and sets it dynamically.







