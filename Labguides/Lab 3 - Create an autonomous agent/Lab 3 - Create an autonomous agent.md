# **Lab 3: Create an autonomous agent**

**Objective**: In this lab, you will learn to create an agent
called Friendly Tutor to help users learn about Copilot Studio using
knowledge from the official Copilot Studio documentation. You will learn
to add knowledge to your agent and test content changes in real time.
You will also learn to enable multilingual support in the agent by
adding French and German as a secondary language to ensure the agent can
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
    using +++https://go.microsoft.com/fwlink/?LinkId=2107702+++.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image1.png)

2.  Fill in the following required information and then select **Get
    Started**.

     **Country or Region** – United States
    
     **Job title** – Your job title
    
     **Business phone number** – Your phone number
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image2.png)

3.  Under the **Confirmation details** step, select **Get Started**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image3.png)

4.  Select **United States** as your country/region and then
    select **Get** **Started**.

     ![](./media/image4.png)

5.  Select the **Dev One** environment from the environment selector.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image5.png)
    
     **Note**: If you're unable to select the **Dev One** environment as
     shown in the image below, then follow the steps below.
    
     ![image](./media/image6.png)
    
     Open the Power Platform Admin Center using
     +++<https://admin.powerplatform.microsoft.com/+++. From the left-hand
     menu, select **Manage**, then choose **Environments** \> **Dev One**.
     Copy the **Environment ID**, and update the Copilot Studio link
     accordingly, as shown in the image below.
    
     ![image](./media/image7.png)
    
     Navigate back to the Copilot Studio tab and open
     +++<https://copilotstudio.microsoft.com/environments>**< EnvironmentID >**/home+++ (Replacing **< EnvironmentID >** with the value fetched above)
    
     ![](./media/image8.png)

6.  On the **Welcome to Copilot Studio** pop-up, select **Skip.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image9.png)

7.  Enter a given prompt of what you want your agent to do: +++Help
    users learn how to create agents with Copilot Studio.+++ 

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image10.png)

8.  The **Overview** page for your agent appears.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image11.png)

9.  In the **Details** section, select **Edit**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image12.png)

10. Rename your agent +++Friendly Tutor+++ then select **Save.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image13.png)

11. In the **Instruction** section, select **Edit**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image14.png)

12. Specify the desired conversation style and tone your agent should
    use, for example, enter the given prompt - +++**Friendly Tutor should talk to users like a kind, patient teacher**+++ and then select **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image15.png)

13. In the **Knowledge** section, select **Add knowledge**.

     ![A screenshot of a web browser AI-generated content may be incorrect.](./media/image16.png)

14. In the **Add knowledge** window, select **Public websites**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image17.png)

15. In **Add public websites**,
    enter +++https://learn.microsoft.com/microsoft-copilot-studio+++, select **Add**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image18.png)

16. Select **Add to agent**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image19.png)
    
     **Note:** During the creation experience, your agent might need a few
     moments before it can start using its knowledge sources.

17. The **Overview** page for your agent appears. Now you can
    start testing and improving your agent.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image20.png)

### **Task 2: Test changes to your agent**

The best way to improve your agent? Test it. Make some changes. Test it
again. Repeat.

1.  Start by testing how your agent currently responds in the test chat.
    In the **Test you agent** pane, which is opened on the right side of
    the screen, ask your agent a question. For example, enter **How do I
    add a knowledge source?** and select the **Send** icon.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image21.png)

2.  Notice the tone of your agent. In this example, the agent's
    instructions are to talk to users like a kind, patient teacher. What
    if you give your agent different instructions?

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image22.png)

3.  Go to the **Overview** page.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image23.png)

### **Task 3: Change your agent's introduction**

Help your agent make a great first impression with a new introductory
message. This message lets users know what your agent does and
encourages them to interact with your agent.

1.  In the **Test your agent** chat, click on the **Start new test
    session** icon at the top of the panel to restart the conversation.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image24.png)

2.  In the **Test your agent** chat, select your agent's introductory
    message. Select the **Message** box, then select the ellipsis (…)
    next to the message ‘Hello, I am a bot’.

     ![A screenshot of a chat AI-generated content may be incorrect.](./media/image25.png)

3.  Replace the default message with your own by using the message given
    below:

     +++**Hello, I'm here to help you learn how to use Microsoft Copilot Studio. You can ask me all about agents: "What is an agent?" "How do I make an agent?" "How do agents work?"**+++
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image26.png)

4.  Select **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image27.png)

5.  To test this change, click on the **Start new test session** icon at
    the top of the panel to restart the conversation in the **Test your agent** chat panel.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image28.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image29.png)

## **Exercise 2: Enable Multilingual Support and Publish Agent**

In this exercise, you will enable multilingual support for your agent by
adding French and German as secondary languages. You will download and
translate a localization file, upload the translated file, and create a
custom topic that detects the user's language and sets it dynamically.
This ensures the agent can respond appropriately in multiple languages.

### **Task 1: Add Secondary Language and Upload Localization File**

1.  From the top navigation bar, click on **Settings** to open the
    configuration options for the agent.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image30.png)

2.  Within the **Settings** menu, locate and click on
    the **Languages** section from the left side pane. Here, you will
    see the current primary language configuration for the agent.
    The **Primary language** option should already be set
    to **English**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image31.png)

3.  Click on the **+ Add language** button to begin adding a new
    language. This will allow your agent to support multilingual
    conversations.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image32.png)

4.  In the language picker, search for **French (France).** Once
    located, check the box next to it and click **Add** to include it as
    a supported language.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image33.png)

5.  After French has been added, click the **Upload** button. This will
    allow you to manage translations for the agent's content in the
    newly added language.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image34.png)

6.  Select **Browse**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image35.png)

7.  Locate the **localization_fr.json** file in
    your **C:\Labfiles** folder on the VM and click **Open**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image36.png)
    
     **Note**: You can download the current language structure by
     selecting **Download localization file (JSON format)** and then
     translating it into the required language. In this lab, you are using
     a pre-translated localization_fr.json file, which is available in
     the **C:\Labfiles** folder.
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image37.png)

8.  Select **Upload translation updates**. When prompted again, click on
    the **Upload localization** button to confirm and apply the
    translated content to the agent.

     ![A screenshot of a computer screen AI-generated content may be incorrect.](./media/image38.png)
    
     ![A screenshot of a computer screen AI-generated content may be incorrect.](./media/image39.png)

9.  Once the upload is successful, click on the **Close** button to exit
    the language management section.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image40.png)

### **Task 2: Add Secondary Language (German) and Upload Localization File**

1.  Click on the **+ Add language** to add German to the agent.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image41.png)

2.  Enter **German** in the search field, select the check box next to
    the **German** language, and then click on the **Add** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image42.png)

3.  After adding language, click on the **Upload** button to add
    localization.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image43.png)

4.  Click **Browse**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image44.png)

5.  Locate the **localization_translated_de.js** file in your Downloads
    folder, and click **Open**.

     ![](./media/image45.png)

6.  Click **Upload translation updates**. When prompted again,
    click **Upload localization** to confirm and apply the translated
    content to the agent.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image46.png)
    
     ![A screenshot of a computer screen AI-generated content may be incorrect.](./media/image47.png)

7.  Once the upload is successful, click on the **Close** button to exit
    the language management section.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image48.png)

8.  Close the **Settings** pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image49.png)

### **Task 3: Create a Topic to Detect Language and Set User Preference**

1.  Select **Topics** from the top menu bar. Select **+ Add a topic** to
    create a new topic. Choose **From blank** to start with a blank
    template.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image50.png)

2.  In the new topic canvas, at the top of the screen, enter the name +++**Translator**+++.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image51.png)

3.  In the canvas, you'll see a **Trigger node**. In
    the **Describe** section, enter the following phrases to trigger
    this topic:

     +++This topic detects when a user is speaking a non-English language,
     such as French or German, and then switches to that language to
     provide answers in the correct language.+++
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image52.png)

4.  Click on the **(+) Add icon** under the **Trigger** node.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image53.png)

5.  Click on the **Add a tool** option and then select **New Prompt** to
    create a new prompt flow.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image54.png)

6.  On the prompt screen, rename the tool (from the top-left)
    as **Detect language** to represent its functionality.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image55.png)

7.  In the **Instructions** pane, enter the given text: +++**Determine which language this message is written in:**+++

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image56.png)

9.  At the bottom of the instructions panel, click on the **Add
    content** button and then select **Text**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image57.png)

10. For the **Name** field, enter: +++**Message**+++, for the **Sample
    Data** field, enter: +++**Message from the user**+++, and then
    click **Close** once done.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image58.png)

11. In the **Model response** pane, change the output format from
    **Text** to **JSON**, so the response returns structured language
    data.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image59.png)

12. Click on the **Test** button. The response should include a property
    showing the detected language, e.g., "language": "English".

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image60.png)

13. Click **Save** to add the prompt as a node on the topic canvas.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image61.png)

14. On the **Prompt node**, select **3 dots** in the **Enter or select a
    value** field to select a variable.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image62.png)

15. Select the **System** variable **Activity.Text** as the input
    source.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image63.png)

16. Click on the **Output** field and then choose **Create new.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image64.png)

17. Click on the **Var1** variable and rename the variable
    as **DetectedLanguage** and close the **Variable properties** pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image65.png)

18. Under the **Prompt** node, click on the **+ icon** and choose **Add
    a condition** node.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image66.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image67.png)

19. Click on the **Select a variable** field and on the first condition
    line, choose the variable DetectedLanguage.structuredOutput.language

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image68.png)

20. In the **Enter or select a value field**, enter **French** to set
    the value to **French**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image69.png)

21. Under the French condition, click on the **+ icon**, go
    to **Variable management**, and choose **Set a variable value**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image70.png)

22. Click on the **Select a variable** field, navigate to
    the **System** variable and select **User.Language**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image71.png)

23. For value, click on the value field and select **French**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image72.png)

24. Click on the **+** Icon under the prompt tool and select **Add a
    condition** trigger.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image73.png)

25. On the second condition line, choose the
    variable **DetectedLanguage.structuredOutput.language**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image74.png)

26. Enter +++German+++ to set the value to **German**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image75.png)

27. Under the German condition, select the + icon, go to **Variable
    management**, and choose **Set a variable value**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image76.png)

28. For variable, click on the select variable, navigate
    to **System** variable and select **User.Language**. Close the pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image77.png)

29. For value, click on the value field and select **German.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image78.png)

30. Under the **All other conditions** node, click on the **+** **Icon**
    add select **Variable management** > **Set a variable** node.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image79.png)

31. For variable, click on the **Select a variable** field, navigate
    to **System** variable, and select **User.Language**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image80.png)

32. For value, click on the value field and select **English.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image81.png)

33. Under the **French, German, and English** variable node, there is
    a **+** node option that can add a node under all of them. Click on
    the **+** icon.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image82.png)

34. Navigate to **Advanced** and then select the **Generative Answer
    node**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image83.png)

35. Click on the **Input** ellipsis icon, navigate to the
    **System** tab, and select **Activity.Text** variable.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image84.png)

36. Click on the **Edit** option under data source.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image85.png)

37. Turn on the **Search only selected sources** option. Select
    the **Name** check box it will select all the data knowledge
    sources.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image86.png)

38. Scroll select the **Customize** check box and then set the
    customization to **Medium**. Close the pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image87.png)

39. Click the **Save** button at the top-right corner to complete the
    topic configuration.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image88.png)

### **Task 4: Test the Agent**

Verify that the agent responds accurately to user input in both English
and French using test prompts in the built-in test chat window.

1.  Open the **Test your agent** panel from the right side of the
    Copilot Studio interface if it is not already open.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image89.png)

2.  In the message field, enter the following English prompt and click
    on the Execute button. Observe the agent's response and verify that
    it replies in English.

     **Prompt:** +++How do I add a knowledge source?+++
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image90.png)

3.  Now, enter the following **French** prompt in the test field and
    click on **Execute**. Observe the response to confirm that the agent
    replies appropriately in French, based on the uploaded localization
    content.

     **Prompt:** +++Comment ajouter une source de connaissances?+++
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image91.png)

**Summary**: In this lab, you learnt to create an agent by adding
knowledge to your agent and testing content changes in real time. You
also learnt to enable multilingual support in the agent. You uploaded
the translated localization file and created a custom topic that detects
the user's language and sets it dynamically.
