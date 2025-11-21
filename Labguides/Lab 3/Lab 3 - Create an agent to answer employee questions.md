# **Lab 3: Create an agent to answer employee questions about expense
policies**

**Objective:** In this lab, you will learn to use Copilot Studio to
create an agent that answers employee questions about expense policies
in a fictional corporation.

## **Exercise 1: Create an agent**

In this exercise, you will create an agent. The agent will initially
have very limited capabilities, which you’ll extend later in the
exercise by managing topics in your agent and adding knowledge source
for Generative AI responses.

### **Task 1: Create an agent**

In this task, you will create a new agent using Copilot Studio.

1.  Open a web browser, sign into **Microsoft Copilot Studio** with
    your **Office 365 admin tenant** credentials
    using +++https://copilotstudio.microsoft.com/+++
    You land on the **Home** page.

2.  View the Copilot Studio home page, which should look similar to
    this:

     ![](./media/image1.png)

3.  Ensure that you are in **Dev One** environment.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image1.png)

     **Note**: If you're unable to select the Dev One environment, navigate
     to the Power Platform Admin Center. From the left-hand menu, click
     **Manage**, then choose **Environments** > **Dev One**. Copy the
     **Environment ID**, and update the Copilot Studio link accordingly, as
     shown in the image below.

     ![](./media/image2.png)

4.  In the navigation pane on the left, select **Create** to view a page
    on which you can create a new agent. Click on the **New agent** tab.

     ![](./media/image3.png)

5.  Select the **Describe** tab and then enter the following prompt:

     **Create an agent to help employees with expense claims.**

     ![](./media/image4.png)

6.  Review the response from Copilot Studio. The chat pane should look
    similar to the following:

     ![](./media/image5.png)

7.  Continue the conversation to define your agent, which should have an
    appropriate name and tone. Enter the given prompt give the name and
    click on the **Execute** button.

    **Prompt**: Name the agent as +++Expense Helper+++

     ![](./media/image6.png)

8.  Enter the given prompt to adjust the tone and then click on the
    **Execute** button.

    **Prompt**: Use a friendly, professional tone

     ![](./media/image7.png)

9.  Ask the agent not to use any publicly accessible websites by giving
    the given prompt and then click on the **Execute** button.

     **Prompt**: Do not use any publicly accessible websites to get its
     information and avoid providing any tax advice

     **Note**: You will add a source of knowledge for your agent later.

     ![](./media/image8.png)

10. When you’re ready, select **Create** at the top right to create your
    agent. After a short while, it will be displayed like this (you can
    unpin the pane on the left to see it more clearly):

     ![](./media/image9.png)

11. In the **Test your agent** pane, enter the following prompt and then
    click on the **Execute** button.

    **Prompt**: Hello

     ![](./media/image10.png)

12. Review the response, which should be an appropriate message.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image11.png)

13. Now try the following prompt and then click on the **Execute**
    button.

     **Prompt**: Who should I contact about submitting an expense claim?

     ![](./media/image12.png)

     This time the response may be appropriate, but it’s also likely to be fairly generic.

     ![](./media/image13.png)

14. Let’s try another prompt:

     +++What's the expense limit for a hotel stay?+++

     ![](./media/image14.png)

     Again, the response may be appropriate but generic.

     ![](./media/image15.png)

15. Close the **Test your agent** pane by selecting **Test** button from
    the top right corner of the screen.

     ![](./media/image16.png)

### **Task 2: Manage topics in your agent**

You can use topics to provide explicit responses to triggers, such as
common questions or requests that you expect your users to enter.

1.  In the page for your agent, select the **Topics** tab to see its
    topics. Select the **Greeting** custom topic.

     ![](./media/image17.png)

2.  You can see the **Greeting** custom topic on the *authoring canvas*,
    which is a visual designer for creating and editing topics and looks
    similar to this:

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image18.png)

     The *Greeting* topic is triggered by an input in which one of the following phrases is present:

    - *Good afternoon*

    - *Good morning*

    - *Hello*

    - *Hey*

    - *Hi*

     The response to this trigger is to return a message to the user
     saying Hello. How can I help you today?. The inclusion of this topic
     in the agent explains the response you saw previously when testing it.

3.  Return to the **Topics** page, and in the **+ Add a topic** menu,
    select **Add from description with Copilot**.

     ![](./media/image19.png)

4.  In the **Add from description with Copilot** dialog box, name the
    new topic as +++Ask about expenses contact+++ and enter the following
    text to tell Copilot Studio what the topic should do:

     +++When the user asks who to contact about expense claims, tell them to send an email to finance@contoso.com+++

5.  Select **Create**.

     ![](./media/image20.png)

6.  If prompted, select **Allow** for **see text and images copied to
    the clipboard**.

7.  After a short wait, a new topic named **Ask about expenses
    contact** should be created and opened in the authoring canvas,
    where it should look similar to this:

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image21.png)

     The new topic should be triggered by phrases that ask about a contact
     for expenses and respond with a message telling the user to send an
     email to the appropriate address.

     **Note**: When the user asks who to contact about expense claims, tell them to send an email to finance@contoso.com

8.  Use the **Save** button (at the top right) to save the new topic in
    your agent.

     ![](./media/image22.png)

9.  Open the **Test** pane.

     ![](./media/image23.png)

10. Enter the following prompt:

     **Who should I contact about submitting an expense claim?**

     ![](./media/image24.png)

### **Task 3: Add a knowledge source for Generative AI responses**

You can add topics for all the inputs that you expect a user to enter;
but you can’t realistically expect to anticipate every question that
will be asked. Currently, your agent uses a Conversation boosting topic
to generate AI responses from a language model, but this results in
generic answers. You need to provide a source of knowledge in which the
generative AI responses can be grounded to provide more relevant
information.

1.  Return to the browser tab for Copilot Studio, and close the **Test
    your agent** pane to see the page more easily,

     ![](./media/image25.png)

2.  Select the **Knowledge** tab to see the knowledge sources defined in
    your agent (currently there should be none).

     ![](./media/image26.png)

3.  Select **+ Add knowledge**, and note the multiple types of knowledge
    source that you can add to your agent.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image27.png)

4.  In the **Upload file** section, select **Upload file** and upload
    the expense policy document from the **C:\Labfiles** folder on the
    VM.

     ![](./media/image28.png)

     **Note**: After uploading the file, you will need to wait while it is indexed; which may take 10 minutes (or longer).

5.  Select **Add to agent**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image29.png)

6.  Once the status becomes **Ready**, you can proceed to execute the
    next step.

     ![](./media/image30.png)

7.  Expand the **Test** pane and select **Start new test session**.

     ![](./media/image31.png)

8.  Then enter the following prompt:

     **What’s the expense limit for a hotel stay?**

     The response should be based on the information in the knowledge source you uploaded, and include a citation reference.

     ![](./media/image32.png)

9.  Try asking some follow-up questions, such as:

     +++What about flights?+++
    
     +++What guidelines are there for entertainment expenses?+++
    
     ![](./media/image33.png)
    
     ![](./media/image34.png)

## **Exercise 2: Publish your agent**

In this exercise, you will Publish your agent for use in a demo web
page.

### **Task 1: Publish your agent**

Now that you have a working agent, you can publish it for people to use.
The available channels through which you can deliver your agent depend
on the type of authentication you want to use to restrict access to it.
In this case, you’ll enable access for anyone and then publish the agent
for use in a demo web page.

1.  Hide the **Test your agent** pane by clicking on the **Test** icon.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image35.png)

2.  Then, at the top of the page, select the **Channels** tab and review
    the channels to which you can deploy your agent. The available
    channels depend on the authentication settings for your agent.

     ![](./media/image36.png)

3.  Select **Settings** at the top of the page.

     ![](./media/image37.png)

4.  In the **Settings** pane, on the **Security** page,
    select **Authentication**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image38.png)

5.  Then select the option for **No authentication** and **Save** the
    changes to the configuration.

     ![](./media/image39.png)

6.  Select **Save** again (confirming that you want to enable access to
    the agent for everyone).

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image40.png)

7.  Close the **Settings** pane.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image41.png)

8.  Then, view the **Channels** page.

9.  At the top of the page, select **Publish**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image42.png)

10. Then, on the **Publish** page, select **Publish**. Publishing will
    take a minute or so.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image43.png)

11. After your agent has been published, verify the **Publish
    status** on the **Channels** page.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image44.png)

12. Select the **Demo website** channel. This is an appropriate channel
    for users to test your agent.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image45.png)

13. In the **Demo website** pane, enter the following settings:

    - **Welcome message**: Ask me about Expense claims 

    - **Conversation starters**:

     "Hello"
    
     "Who should I contact with expense enquiries?"
    
     "What are the expense limits for flights?"

14. Then **Copy** the link to your agent demo website to the clipboard.

     ![](./media/image46.png)

15. Select **Save** to save the settings.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image47.png)

16. In a new browser tab, navigate to the URL you copied to open the
    demo website, which should look similar to this:

     ![](./media/image48.png)

17. Enter the message as **What are the expense limits for meals?** and
    view the response.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image49.png)

**Summary**: In this lab, you learnt to create an agent that answers
employee questions about expense policies. You learnt to extend agent
capabilities by managing topics in your agent and adding knowledge
source and then you published the agent.

