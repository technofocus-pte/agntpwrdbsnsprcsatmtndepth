# **Lab 0: Set up lab environment**

**Objective:** In this lab, you will acquire Power Apps trial license
and will create a team in Microsoft Teams. You will create a security
group and assigned a Bot author role to MOD Administrator.

## **Exercise 1: Assign Power Apps trial license**

1.  Open a web browser on your VM and go to
    !!https://powerapps.microsoft.com/en-us/free/!!.

     ![](./media/image1.png)

2.  Select **Start free**.

     ![A person with his arms crossed Description automatically generated](./media/image2.png)

3.  Enter your **Office 365 admin credentials**, check the checkbox to
    **accept the agreement** and click on **Start free**.

     ![](./media/image3.png)

4.  Enter **password of your Office 365 tenant id** and then select
    **Sign in**.

     ![](./media/image4.png)

5.  Select **Yes** on **Stay signed in?** pop-up window.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image5.png)

6.  Keep the **United States** as your **country/region** and then click
    on the **Get started** button.

     ![](./media/image6.png)

7.  You can now see **Home page of Power Apps** and the developer
    environment – **Dev One** which is created for you.

     ![](./media/image7.png)

8.  Open the new tab and go to **Power Platform admin center** by
    navigating to !!https://admin.powerplatform.microsoft.com!! and if
    required, sign in using your given Office 365 admin tenant
    credentials.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image8.png)

9.  From the left navigation pane, select **Manage** > **Environments**
    and then you can see, **Dev One** is your Dataverse environment.

     ![](./media/image9.png)

## **Exercise 2: Create a team in Microsoft Teams**

1.  Sign into the Microsoft Teams
    using !!https://teams.microsoft.com/!! with
    your Office 365 tenant credentials.

2.  On **Get to know Teams**, select **Get Started**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image10.png)

3.  Close the window which asks for scanning QR code.

     ![A screenshot of a qr code AI-generated content may be incorrect.](./media/image11.png)

4.  On the left side of the app, Select **Chat**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image12.png)

5.  Select **New items** from above your list of chats and channels.
    Select **New team**. 

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image13.png)

6.  Enter the **Team name** as !!Test Team!!. In **Name the first channel**
    field enter !!TestChannel!! and click on **Private**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image14.png)

7.  Select **Org-wide**.

    ![](./media/image15.png)

8.  Select **Create**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image16.png)

9.  You can now see the **Test** team has been created.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image17.png)

## **Exercise 3: Create a Security group and assign Bot author role** **to MOD Administrator**

    In this exercise, you will create a security group and assign Bot author role to MOD Administrator to grant the              necessary publishing rights.

1.  Open a web browser on your VM and go to the Azure portal using
    !!https://portal.azure.com/!!. Sign in with the given **Office 365
    admin credentials.** You can see the image shown below in your portal. Select **Next** in the **Let’s keep your account      secure** window.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image3.a.png)

2.  In your mobile, install the **Microsoft Authenticator** App and then come back to **Microsoft Azure portal**.                **Microsoft Authenticator – Install Microsoft Authenticator** window, click on the **Next** button.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image3.1.png)

3.  In **Microsoft Authenticator – Set up your account** window, click on the **Next** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image3.2.png)

4.  **Scan the QR code** using the **Authenticator app** installed in your mobile phone and click on the Next button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image3.3.png)

5.  Enter the number in your mobile authenticator app and select **Yes**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image3.4.png)

6. Click on the **Done** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image3.5.png)
   
4.  On the Microsoft Azure portal, in the search bar, enter !!Microsoft Entra!! and select **Microsoft Entra ID** from the       suggestions.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image18.png)

5.  From the left navigation pane, expand **Manage** and then select
    **Groups**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image19.png)

6.  Select **New group**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image20.png)

7.  On the **New Group** page, provide the following information.

     Group type: Security

     Name: !!Agentgrp!!

     ![](./media/image21.png)


8.  Then to select owners, click on the **no owners selected**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image21.png)

9.  **Check** the **checkbox** of **MOD Administrator** and then click
    on the **Select** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image22.png)

10.  To select members, click on the **no members selected**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image23.png)

11.  **Check** the **checkbox** of **MOD Administrator** and then click
    on the **Select** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image24.png)

12.  Select **Create**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image25.png)

13. Navigate to Power Platform admin center. From the left navigation
    pane, select **Manage** tab. Then select **Tenant settings**. In the
    search box, enter !!Copilot Studio!! and then select **Copilot
    Studio authors**.

     ![](./media/image26.png)

14. Click on the **Edit** icon (pencil) next to the **None** opiton.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image27.png)

15. Select **Agentgrp** and then click on the **Done** button.

     ![A white screen with text AI-generated content may be incorrect.](./media/image28.png)

16. Select **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image29.png)

17. From the left navigation pane, select **Manage** > **Environments**
    and then click on the **Dev One** environment.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image30.png)

18. In the **Access** section, click on the **See all** below the
    **Users** option.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image31.png)

19. Select **MOD Administrator.**

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image32.png)

20. Select **Manage roles**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image33.png)

21. Seelct **Bot author** role and then click on the **Save** button.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image34.png)

22. Select **Save** agin to confirm the selection.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image35.png)

23. Close the window.

     ![](./media/image36.png)

**Summary**: In this lab, you acquired Power Apps trial license and
created a team in Microsoft Teams. You also created a security group and
assigned a Bot author role to MOD Administrator.









