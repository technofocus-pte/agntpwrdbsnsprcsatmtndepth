# **Lab 6: Create and enhance Safe Travels agent and implement Multi agent orchestration**

**Objective:** Agent templates are designed to help you get started with
a custom agent. You are responsible for assessing all safety and legal
implications of using an agent template and customizing it as
appropriate for your business.

In this lab, you will learn to create an agent from the Safe Travels
template and how that agent can be enhanced to suit the needs of
specific customers. In the process of doing that, you will learn the
concepts of Agent Flow creation and Multi agent orchestration in Copilot
Studio.

## **Exercise 1: Create Safe Travels agent from template**

### **Task 1: Create Safe Travels agent from template**

In this task, you will create the agent in Copilot Studio using the Safe
Travels agent template.

1.  Sign into **Microsoft Copilot Studio** with your **Office 365 admin
    tenant** credentials
    using +++https://copilotstudio.microsoft.com/+++
    You land on the **Home** page.

2.  Ensure that you are in **Dev One** environment.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image1.png)

     [!Alert] **Important:**  If the Copilot Studio and does not show up
     the option to select **Environment** as in the below screenshot, then
     follow the below steps.

    ![image](./media/image2.png)

     Open +++https://admin.powerplatform.microsoft.com/+++.
     Select **Manage** -> **Environments** **-> Dev One** and select the
     value of the **Environment ID**.

     ![image](./media/image3.png)

     Navigate back to the Copilot Studio tab and open
     +++https://copilotstudio.microsoft.com/environments/**<
     EnvironmentID>**+++ (Replacing **<EnvironmentID>** with the
     value fetched above)

3.  Select **+ Create** from the left pane to create a new agent.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image4.png)

4.  Under **Start with an agent template**, select **Safe Travels**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image5.png)

5.  The Safe Travels template creates a new agent that is designed to
    provide employees of a company with travel assistance. 

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image6.png)

6.  Browse through the set-up page. Under **Knowledge**, you can find
    that **US Travel Website** is already added as a Knowledge source.
    It can be edited if needed. Here, we are using the same website.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image7.png)

7.  Select **Create** to create the Safe Travels agent. We are not
    changing anything here and using the template as such. At any point,
    the agent can be upgraded as per the user requirements.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image8.png)

8.  The **agent** gets **created** and opens up automatically showing up
    the **Overview** page.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image9.png)

9.  In the **Test** pane, enter +++How to apply for passport?+++ and hit
    **Send**.

    The Test pane is open by default. If not, click on the Test icon on top
    right.
    
    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image10.png)

10. You can see that the agent provides information on how to apply for
    the passport from its knowledge source.

    ![A screenshot of a phone AI-generated content may be incorrect.](./media/image11.png)

### **Task 2: Publish the agent to Teams and Microsoft 365 Copilot**

In this task, you will publish the agent created in Copilot Studio to
the Microsoft Teams and Microsoft 365 Copilot channel.

1.  Open the **App launcher** from the top-left corner of the screen.
    Select **Teams**.

     ![](./media/image12.png)

2.  Back in the Copilot Studio, select **Publish** from the top right of
    the agent page.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image13.png)

3.  Select **Publish** in the confirmation dialog.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image14.png)

4.  Select **Channels** from the top navigation bar.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image15.png)

5.  Select **Teams and Microsoft 365 Copilot** from the list of
    available channels.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image16.png)

6.  Select **Add channel**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image17.png)

7.  Click on the **See agent in Teams** option add the agent to the
    Teams.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image18.png)

8.  If the screens below appears, select **Cancel** and then select
    **Use the web app instead**.

    ![](./media/image19.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image20.png)

9.  This opens up the agent in the Microsoft Teams. Select **Add** to
    add the agent.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image21.png)

10. Once added, you will get an option to open the agent. Select
    **Open**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image22.png)

11. Test the agent from Teams. Enter the given prompt – **Hi**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image23.png)

12. Enter the given prompt – **How can I apply for passport?** and click
    on the **send** icon.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image24.png)

13. Back in the Copilot Studio, close the Teams and Microsoft 365
    Copilot channel window.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image25.png)

## **Exercise 2 – Enhance the Safe Travels agent** 

### **Task 1: Test the existing Safe Travels agent**

In this task, we will test the **Safe Travels** agent to see how it
responds when asked about travel approval.

1.  Open the **Copilot Studio** at
    +++https://copilotstudio.microsoft.com+++ from a browser. Ensure
    that you are in the **Dev One** environment. From the left
    navigation pane, select **Agents** tab and open the **Safe Travels**
    agent.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image26.png)

2.  Select the **Test** icon to test the agent.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image27.png)

3.  Enter +++Need travel approval+++ in the Test window and click on the
    **send** icon.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image28.png)

4.  You can see that the agent responds with a generalized instruction
    set to be followed to get the travel approval.

    ![A screenshot of a travel approval AI-generated content may be incorrect.](./media/image29.png)

### **Task 2 – Enhance the agent with company specific Knowledge assets**

In this task, we will add knowledge asset - **Travel Policy** specific
to the company Contoso.

1.  From the Overview page of the agent, scroll down and select **+ Add
    knowledge**

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image30.png)

2.  Click on **select to browse** option.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image31.png)

3.  From **C:\Labfiles** folder, select **Travel Policy.docx** and click
    **Open**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image32.png)

4.  Click **Add** to the add the file.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image33.png)

     ![A screenshot of a computer error AI-generated content may be incorrect.](./media/image34.png)

5.  Ensure that the file is added. Wait till the status changes from
    **In progress** to **Ready** before proceeding to the next step.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image35.png)

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image36.png)

### **Task 3 – Create a Team and Channel in Microsoft Teams**

In this task, we will create a team and a channel in MS Teams to which
the travel approval request will be sent.

1.  Sign into the Microsoft Teams
    using +++https://teams.microsoft.com/+++ with
    your Office 365 tenant credentials.

2.  Open Microsoft Teams and select **See all your teams** option from
    the left pane.

    ![A screenshot of a chat AI-generated content may be incorrect.](./media/image37.png)

3.  Select **Create team** to create a new team.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image38.png)

4.  Enter the Team name as +++**HR Team**+++ and First channel name as
    +++**Travel Approval Channel**+++ and select **Create**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image39.png)

5.  Select **Skip** in the Add members to HR Team dialog.

    ![A screenshot of a email AI-generated content may be incorrect.](./media/image40.png)

6.  Now, the Team and Channel creation is completed.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image41.png)

### **Task 4 – Create an Agent flow**

In this task, we will create a new Agent flow to post the travel request
to the Teams channel

1.  Select **Flows** from the left pane.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image42.png)

2.  Select **+New agent flow** to create a new flow.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image43.png)

3.  Select **When an agent calls the flow** under **AI capabilities**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image44.png)

4.  Select **+ Add an input**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image45.png)

5.  Select **Number** as the type of user input.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image46.png)

6.  Name the input as +++**Employee ID**+++. Then select **+ Add an
    input**.

    ![](./media/image47.png)

7.  Now, select a **Text** input and name it as +++**Purpose**+++.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image48.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image49.png)

8.  Select **+ icon** to **add an action** below the trigger node.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image50.png)

9.  Search for +++**Teams**+++ and click on **See more** under the Teams
    group of actions.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image51.png)

10. Select **Post message in a chat or channel**.

    ![](./media/image52.png)

11. Select **Sign in** and **login** using your credentials.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image53.png)

    ![A screenshot of a computer error AI-generated content may be incorrect.](./media/image54.png)

12. Select the below details

    Post as – Select **User**
    
    Post in – Select **Channel**
    
    Team – Select **HR Team**
    
    Channel – Select **Travel Approval Channel**
    
    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image55.png)

13. In the Message field, enter the following

    \`\`\`
    
     Travel Request from
    
     Employee ID - <Employee ID>
    
     Purpose - <Purpose>
    
     \`\`\`
    
     Replace **\<Employee ID\>** and **\<Purpose\>** with the dynamic
     content variables, **Employee ID** and **Purpose** as in the below
     screenshots.
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image56.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image57.png)

14. The Parameters tab will now look like below.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image58.png)

15. Add another **action** after the Post message node.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image59.png)

16. Select **Respond to the agent** under **AI capabilities**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image60.png)

17. Select **Add an output**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image61.png)

18. Select **Text** the type of output.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image62.png)

19. Name it as +++Output+++ and enter the value as +++Request
    submitted+++.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image63.png)

20. Click on **Save draft** to save the flow.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image64.png)

21. Once the flow is saved, select **Publish**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image65.png)

22. Ensure that the flow has been published.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image66.png)

23. Click on the **Overview** tab of the agent flow.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image67.png)

24. Select **Edit** and name the flow as +++Request Travel Approval
    Flow+++ in the **Details** pane. Select **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image68.png)

### **Task 5 – Add the Agent flow as a tool to the agent**

In this task, we will add the created Agent flow to the agent Safe
Travels in order to leverage the flow functionality.

1.  From the left pane, select **Agents**.

    ![](./media/image69.png)

2.  Select the **Safe Travels** agent.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image70.png)

3.  Scroll down in the Overview page and select **Add tool**.

    ![A screenshot of a web page AI-generated content may be incorrect.](./media/image71.png)

4.  Select the **Flow** tab and then select created **Request Travel
    Approval Flow**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image72.png)

5.  Select **Add and configure**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image73.png)

6.  Select **Add to agent**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image74.png)

7.  Once added, you can see the flow under **Tools** tab.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image75.png)

8.  Select **Overview** tab, the flow will get listed under **Tools**
    section.

    ![A screenshot of a search engine AI-generated content may be incorrect.](./media/image76.png)

### **Task 6 – Create Topic**

In this task, we will create a Topic to use the created travel approval
flow.

1.  Select **Topics** from the top menu.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image77.png)

2.  Select **+ Add a topic** -> **Add from description with Copilot**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image78.png)

3.  Enter the below details and then select **Create**.

    **Name** - +++Travel Approval+++
    
    **Create a topic to** - +++This topic should get the Employee ID
    (Number) and Purpose of travel (Text) details from the user and invoke
    the Tool "Request Travel Approval Flow"+++
    
    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image79.png)

4.  The **Topic** gets created as below.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image80.png)
    
    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image81.png)

5.  See if the Flow is invoked. In this case, only a Message node
    stating that the flow is invoked is added. In such a case,
    **delete** such **Message** node and click on **Add a node** icon
    after the node where the Purpose is requested from the user.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image82.png)
    
    ![](./media/image83.png)

6.  Select **Add a tool** -> **Request Travel Approval Flow.**

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image84.png)

7.  For the flow variable **Employee ID,** click on the 3 dots **(…)**
    in the **Enter or select a value field** and add the variable
    **EmployeeID.**

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image85.png)
    
    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image86.png)

8.  Similarly add the **Purpose of travel** input.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image87.png)

9.  Select **+icon** to add a new node and then select **Send a
    message** node.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image88.png)

10. Click on the **{x}** icon to add a variable.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image89.png)

11. Add the **Output** Variable to it as in the screenshots below.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image90.png)

12. Select **Save.**

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image91.png)

13. Select **Publish** to publish the agent.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image92.png)

14. Select **Publish** in the confirmation dialog box.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image93.png)

15. Select the **Test** icon and enter +++Travel Approval+++ and
    **send** from the test pane.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image94.png)

16. Converse by giving the below details to the agent

     Employee ID – +++1234+++
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image95.png)

17. Enter the Purpose of travel - +++Client meeting for finalizing
    proposal of XYZ project+++ and click on the **send** icon.

    ![A screenshot of a chat AI-generated content may be incorrect.](./media/image96.png)

18. Select **Allow**.

    ![A screenshot of a chat AI-generated content may be incorrect.](./media/image97.png)

19. You will get a **Request submitted** message from the agent.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image98.png)

20. Open the **Teams Channel** and you will see the details posted there
    for the Travel approval.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image99.png)

### **Task 7 – Create Leave Management agent** 

In this task, we will build a Leave management agent which can be used
to learn about the leaves, leave balance for employees and so on.

1.  From the Copilot Studio Home page, select **Agents** -\> **+ New
    agent**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image100.png)

2.  Select **Configure** tab.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image101.png)

3.  In the configuration page, enter the below details and select
    **Create**.

    - Name - +++Leave Manager Agent+++

    - Description - +++This agent is to track the leaves of all the
      employees, their leave balance and leave history to approve or
      reject any new leave requests.+++

    - Instructions - +++Track the leaves of employees. Track their leave
      balance. Apply/Reject leaves based on their balance.+++

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image102.png)

4.  Once the agent gets created, scroll down in the **Overview** page
    and select **Add knowledge** under the **Knowledge** section.

    ![](./media/image103.png)

5.  Click on **select to browse**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image104.png)

6.  Select the file **Leave balance Tracker** from **C:\Labfiles** and
    click **Open**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image105.png)

7.  Select **Add to agent** to add the tracker to the agent.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image106.png)

8.  The file gets added. Wait until the status is Ready before
    proceeding to the next step.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image107.png)

9.  Select **Topics** from the top navigation bar.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image108.png)

10. Select **+ Add a topic** -> **Add from description with Copilot**
    from the Topics tab.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image109.png)

11. Enter the below details and click on **Create**.

    - Name - +++Leave Balance Checker+++
    
    - Create a topic to - +++Get the Employee ID from the user and check and
      reply with the leave balance based on the tracker added as knowledge
      source+++
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image110.png)

12. Check if the topic has the node to get the Employee ID and then
    click **Save**. Here, we have a node for getting the Employee ID and
    a Message node stating that the balance is being retrieved.

     Check the topic once and remove other nodes that have got created apart from the above ones.
    
     Then **Save** the topic.
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image111.png)

13. Send a message +++Check Leave balance+++ from the **Test** pane.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image112.png)

14. Enter +++1234+++ for Employee ID.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image113.png)

15. Check the response from the agent. This is retrieved from the
    knowledge asset added to the agent.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image114.png)

16. Select **Publish** and wait till the agent is published.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image115.png)

17. Select **Publish** again.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image116.png)

## **Exercise 3 - Implement Multi agent orchestration in Copilot Studio**

Rather than relying on a single agent to do everything—or managing
disconnected agents in silos—organizations can now build multi-agent
systems in Copilot Studio (preview), where agents delegate tasks to one
another. This includes those built with the Microsoft 365 agent builder,
Microsoft Azure AI Agents Service, and Microsoft Fabric. These agents
can now all work together to achieve a shared goal: completing complex,
business-critical tasks that span systems, teams, and workflows.

In this exercise, we will add the Leave management agent to the Safe
Travels agent which can be used to learn about the leaves when planning
to travel.

1.  Select **Agents** tab and then select the **Safe Travels** agent.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image117.png)

2.  We will first test this agent to see what information it can give on
    leaves. From the **Test** pane, enter +++Check Leave balance+++ and
    select **send** icon.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image118.png)

3.  You can see that the agent responds with a generalized information
    on how to check the leave balance. It also refers to the Travel
    Policy document while doing this.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image119.png)

4.  Select the **Agents** tab from the top menu.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image120.png)

5.  Select **+ Add**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image121.png)

6.  On the **Choose how you want to extend your agent** window, select
    **Leave Manager Agent** from the list. It can be added only if it is
    published. Please wait if it is in the process of publishing.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image122.png)

7.  Select **Add agent** to add this agent to **Safe Travels**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image123.png)

8.  To trigger the flow, you need to enable **generative
    orchestration**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image124.png)

9.  To enable **generative orchestration**, select **Settings**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image125.png)

10. In the **Orchestration** section, select **Yes - Responses will be
    dynamic, using available tools and knowledge as appropriate** for
    **Use generative AI orchestration for your agent's responses?** Then
    select **Save.**

    ![](./media/image126.png)

11. Close the **Settings**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image127.png)

12. Now you can see that **Trigger** is updated as **By agent**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image128.png)

13. Wait for few minutes after the agent is added and then click on
    **Publish**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image129.png)
    
     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image130.png)

14. Wait for few more minutes after the agent is published and then
    enter +++Check Leave balance for 1234+++ in the **Test** pane of the
    **Safe Travels agent**.

15. You can see that the **Leave Manager** agent is accessed
    automatically and the agent replies to the question from the **Leave
    Manager agent’s topic**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image131.png)

**Summary:** In this lab, you learnt how to enhance an agent created
from a template to suit the individual needs. You have also learnt to
implement Multi agent orchestration in the Copilot Studio.


