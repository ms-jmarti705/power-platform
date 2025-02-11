---
title: "Create a team template and add to an entity form  | MicrosoftDocs"
description: Create a team template and add to an entity form
author: paulliew
ms.subservice: admin
ms.author: paulliew
ms.reviewer: sericks
ms.custom: "admin-security"

ms.component: pa-admin
ms.topic: conceptual
ms.date: 08/22/2023
search.audienceType: 
  - admin
---
# Create a team template to control access rights for automatically created teams

<!-- legacy procedure -->

A team template can be used for the entities that are enabled for automatically created access teams. In the team template, you have to specify the entity type and the access rights on the entity record. For example, you can create a team template for an account entity and specify the Read, Write, and Share access rights on the account record that the team members are granted when the team is automatically created. After you create a team template, you have to customize the entity main form to include the new team template. After you publish customizations, the access team template is added in all record forms for the specified entity in a form of a list. For example, you created a team template called “Sales team” for the account entity. On all account record forms you’ll see the list called “Sales team”. You can add or remove team members using this list.  

To learn more about creating, using, and adding access teams to a solution, watch the following video.
> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW18Hte] 

    
## Enable an entity for access teams  

Make sure you have the System Administrator or System Customizer security role or equivalent permissions.

Check your security role:
- Follow the steps in [View your user profile](/powerapps/user/view-your-user-profile).
- Don’t have the correct permissions? Contact your system administrator.

1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) as an admin (Dynamics 365 admin, Microsoft 365 Global admin, or Microsoft Power Platform admin).

2. Select an environment and go to **Settings** > **Templates** > **Access team templates**.

3. On the command bar, select **More Commands** (...).

4. Select **Customize Entity**. 

5. In the navigation pane, expand **Entities**, and then choose the entity you want to use in the team template.  

6. On the **Entity Definition** form, in the **Communication & Collaboration** section, select the **Access Teams** checkbox.  

7. On the **Actions** toolbar, select **Save**.  
  

## Create a team template  
  
1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) as an admin (Dynamics 365 admin, Microsoft 365 Global admin, or Microsoft Power Platform admin).

2. Select an environment and go to **Settings** > **Templates** > **Access team templates**.
  
3. On the **Actions** toolbar, choose **+New**, complete the required fields, and then choose **Save**.  

> [!NOTE]
> You can create two access team templates per entity.

## Add a team template to the entity form   
  
1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) as an admin (Dynamics 365 admin, Microsoft 365 Global admin, or Microsoft Power Platform admin).

2. Select an environment and go to **Settings** > **Templates** > **Access team templates**.

3. On the command bar, select **More Commands** (...).

4. Select **Customize Entity**.  

5. In the navigation pane, expand **Entities**, expand the entity you want to use in the team template, and then select **Forms**.  

6. In **System Forms**, select **Active Forms** > **Main** form. 

7. On the **Main** form, open the **Insert** tab.  

8. On the ribbon, choose **Sub-Grid**.  
  
    The **Set Properties** dialog box appears.  
  
9. In **Set Properties**, complete the required fields, and then select the **Display label on the Form** check box. 

10. In the **Records** drop-down list, select **All Record Types**.  

11. In the **Entity** drop-down list, select **Users**.  

12. In the **Default View** drop-down list, select **Associated Record Team Members**.  

13. In the **Team Template** drop-down list, select the desired template and choose **Set**.  
  
     The team template you selected now appears on the **Main** form.  
  
14. On the **Actions** toolbar, select **Save**, and then select **Publish**.  

## Add a team template to a solution   

You can add your team template as a component to a [solution](/power-apps/maker/data-platform/solutions-overview).

1. [Create a solution](/power-apps/maker/data-platform/create-solution).

   Add Team template.
   
1. Select **Add existing** on the action bar.
1. Select **More** and **Other**, and then select **Team template**.
1. Select your Team template and select **Add**.

   Add the table where your Team template was added.

1. Select **Add existing** on the action bar.
1. Select **Table**.
1. Select the table where the Team template was added. Select **Next**.
1. Select the **Include table metadata** option.
1. Select **Add**.

> [!NOTE]
> For custom tables, you will need to select the **Include all objects** option.

   Add the form where the Team template was added.

1. Double-click the table where the updated form resides.
1. Click the **Forms** link under the **Data experiences** section.
1. Click the **Add existing form** option on the Action bar.
1. Select the form where the Team template was added.
1. Click **Add**.
1. [Publish your customizations](/power-apps/maker/data-platform/create-solution#publish-changes).

## Export your team template
You can now export your team template and import it into a different environment.

1. [Export your team template solution](/power-apps/maker/data-platform/export-solutions).
1. Download the solution .zip file.
1. [Import your team template .zip file solution](/power-apps/maker/data-platform/import-update-export-solutions).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
