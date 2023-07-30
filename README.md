<p align="center">
<img src="https://icon-library.com/images/active-directory-icon/active-directory-icon-2.jpg" alt="Active Directory Logo"/>
</p>
<h1>Active Directory</h1>
This tutorial outlines the proper utilization of Microsoft Active Directory. Active Directory is a core tool for system administrators who need to manage Windows machines. Active Directory allows you to manage users, groups, machines, and the policies that apply to all of them in a centralized fashion. In this tutorial, you'll interact with Active Directory, use it to add users and groups, edit users memberships as well as create a new group policy object (GPO).<br />
<h2>Environments and Technologies Used</h2>

- Windows Virtual Machine
- Qwiklabs
- Microsoft Active Directory

<h2>Operating Systems Used </h2>

- Windows 10</b>
<h2>Managing Users and Groups<h2>
 Open the Active Directory Administrative Center (ADAC). You can find it by typing "active" into the Windows start menu.
<p><img alt="" src="https://cdn.qwiklabs.com/3RaKcfhSZ2kffGXVHZqQb4eohABAU4IWptWYcEj%2FdpM%3D" style="height:674px; width:391px" /></p>

The Active Directory Administrative Center allows you to manage your Active Directory installation, by configuring users, groups, computers, and more. Feel free to browse around the resources that already exist in the directory.
<p><a href="https://cdn.qwiklabs.com/Aswh6JeCCxyeti2JxCQViH69XEAkVU2Sy5Q3Vqcnjd4%3D"><img alt="" src="https://cdn.qwiklabs.com/Aswh6JeCCxyeti2JxCQViH69XEAkVU2Sy5Q3Vqcnjd4%3D" /></a></p>
For this lab, we want to create a new user called Alex. To do that, first click on the example (local) entry. This is the entry for the domain that your account can manage. Then scroll down and double click on the Users entry to see the list of users and groups that currently exist.
<h2>Adding users<h2>
To create a new user, take a look at the tasks list on the right. Under the Users section, there's a New menu entry, which opens a submenu to select what's the type of entity that you want to create. In this case, we want to create a new user, so click User.
<p><img alt="" src="https://cdn.qwiklabs.com/tTfpvE7P%2BtZe%2BGkjUtlr2qv0pW7W8ApzdvFCUuco7iA%3D" /></p>
This will open a new window that lets you fill in a number of fields related to the new user. There are a lot of fields available, but only a couple are mandatory (indicated with the red star). You can leave the rest empty. The user that we are creating is called Alex, with their username being also alex.
<p><img alt="" src="https://cdn.qwiklabs.com/bvbG097amSkvVvEVXkhVoMcGC%2BHhqoAwI1OHrFA2qpA%3D" /></p>
Once you've entered the necessary data, click the OK button to have the user created.

If you click on the newly created account, you will see that where it displays the name of the user, the system says Alex (Disabled).
<p><img alt="" src="https://cdn.qwiklabs.com/NvZU4ck4JlxgsXF8DrMMuNOOPpvK6dENRyZtI4c4d6E%3D" /></p>
What happens if you right click on the entry and try to Enable it?

<p><img alt="" src="https://cdn.qwiklabs.com/jbVCyj1Qb42DM6L%2B%2Bqp0c8OOamHjHNns1B78WFNCG5s%3D" /></p>
The system will not enable an account that doesn't have a good password. In this case, the password is empty because we haven't set it. Obviously, an empty password is not a good password.

You can set a password using the Reset password menu option. By having the User must change password at next logon option selected, we ensure that the user will change their password when they log in. The goal of this is that after they've logged in once, the system administrator will not know their new password.
<p><img alt="" src="https://cdn.qwiklabs.com/J23LwU%2FL6gcHBVUqsRvyF55YXC8tlckokRW4fVLWMgg%3D" /></p>
Once you've set a good password, you can retry enabling the account. This time it should work.
<h2>Adding groups<h2>
Let's now add a new group. If you browse through the existing groups, you will see that there's a group called Developers and a group called Java Developers. We now want to add an additional group, called Python Developers. Add the new group to the Developers group, then add the account we just created for Alex to the Python Developers group.

To create a new group, use the same menu that you used for creating a new user, but this time select the new Group option.
<p><img alt="" src="https://cdn.qwiklabs.com/IeFrSwAKItUp51sL7mINY7ZhTiST4UDrko5O78hmHDk%3D" /></p>
This will open a similar window to the one that we saw before, but this time it requires the data for the Group rather than the user.
<p><img alt="" src="https://cdn.qwiklabs.com/39AoKzRbX8pSdmNTSLGEPQgE0VFQl7UeNRPvIFVYJ2o%3D" /></p>
We are creating a group called Python Developers and that's the only data that is mandatory. You can also add additional information in the Description and Notes, if you want. Once you are done, click OK to have the group created.

<h2>Adding entities to groups<h2>
We have a Python Developers group, now we want to add it to the Developers group that already exists. We can do this by scrolling down to the new entry and then right clicking on the entry in the list and selecting the Add to another group entry.
<p><img alt="" src="https://cdn.qwiklabs.com/bzP5OxNZlbClqDaezTA5se2tyjppyhO1g8z9YgsT954%3D" /></p>
This will open a small window where we need to enter the name of the group. In this case, the group is called Developers.
<p><img alt="" src="https://cdn.qwiklabs.com/RihxM2IPXHzolrw0CXTFnuwadzHk6PxQudNlt2RXVZU%3D" /></p>
You can use the Check Names button to verify that you have entered the name correctly. If you have, it will underline the text. If the name is incorrect, it will show a window saying "Name Not Found."

Clicking the OK button will add the Python Developers group to the Developers group. We now want to do the same for adding Alex to Python Developers. But we'll follow a different path.

In this case, we will double click the Python Developers entry in the list, which will open up an editing window for the group.

<p><img alt="" src="https://cdn.qwiklabs.com/Xa%2BWhAbDbMY8QSWgFSUl7jL0sxPLUii%2BoGJk1xMCyeM%3D" /></p>
You can scroll down until you find the Members section of this window, or you can click on the Members link on the left. This section allows us to manually add or remove members from the group.
<p><img alt="" src="https://cdn.qwiklabs.com/9rG77%2FhtdxQE0IXpGT00Y51iaXtZuOIWe%2F2Rczk1fkQ%3D" /></p>
In this case, what we want to do is to add Alex to the group, so click the Add button, enter Alex in the text field and then OK for the addition and OK for saving the changes. We've successfully added a new member, Alex, into the Group!

<h2>Editing memberships<h2>
Finally, there's an existing user called Alosha that has switched from programming in Java to programming in Python, we want to remove this user from the Java Developers group and add them to the Python Developers group.

To do this, look for the user Alosha in the list and double click on the entry. This will open the properties of the user that you will be able to edit. There's a lot of configuration to each user, click on the section on the left called Member Of.
<p><img alt="" src="https://cdn.qwiklabs.com/HHf84kzC3PWRFrqPbwQsowRxP2dA0zdQeSIbbEQSh7Y%3D" /></p>
We can see that Alosha is a member of the Domain Users group (all users of the domain are members of this group) and of the Java Developers group. You can select the Java Developers entry and click the Remove button to remove that group.

The click the Add button to add a new membership.
<p><img alt="" src="https://cdn.qwiklabs.com/1HsIwFZeWl8IfFPyAXP5pX0yhSsIZs0pgiN2JhCNjFA%3D" /></p>
This will pop-up a small window where you need to enter the name of the group that you want to add, in this case Python Developers. Once you are done, click OK in the Select Groups window and then OK in the editing user window.

With that, we've created users and groups and we've added and removed group memberships using Active Directory. Let's now look into how to manage group policies.

<h2>Managing Group Policies<h2>
To manage group policies, we need to use the Group Policy Management application. You can find it by typing group into the Windows start menu.
<p><img alt="" src="https://cdn.qwiklabs.com/Hqz20zOhw8GkfS4SXaatmlq2eeUDMphFEQKYRwqNz0U%3D" /></p>
This application allows you to set policies that will manage the way machines in your domain behave. You can apply these policies to the whole domain or to separate Organizational Units (OUs).

In our case, we want to add a new policy to the Developers OU that already exists in the domain. To do that, expand the tree until you reach the example.com domain tree and find the Developers OU inside it.
<p><img alt="" src="https://cdn.qwiklabs.com/l18ast0sbOAKorzO6C%2Fjnnp7T3haAdvAkvFIcvfpnGY%3D" /></p>
To create a new policy, right click on the entry and select the first menu entry: Create a GPO in this domain and Link it here.

When you click this option, you will be prompted to set a name for the policy and once you do, the policy will get added to the OU.
<p><img alt="" src="https://cdn.qwiklabs.com/Dntkfx4pJpeVq4new0mWfH5GkWl35uG7J27aEle9t%2Fs%3D" /></p>
We want to set a default wallpaper for the machines in the Developers OU, so we will call our policy "New Wallpaper"

Once created, we want to edit the policy, to do this, right-click on the entry and click on the first menu entry: Edit.
<p><img alt="" src="https://cdn.qwiklabs.com/FoiATMg73822pAHCG1yhPD4yiulAw%2BpqXRXHD5qiSMw%3D" /></p>
Note: You may get a warning message about what linking policies means. That's ok, you can just accept the warning and move on.

This will open a new application: the Group Policy Management Editor. This application allows you to navigate and configure all settings that can be set in a group policy.

As we want to set the wallpaper, we need to navigate to this setting by going to: User Configuration > Policies > Administrative Templates > Desktop > Desktop
<p><img alt="" src="https://cdn.qwiklabs.com/ytG8fJihU6H9L8WbKq8I6KV%2B%2F45f%2FOPsXtzcS6ZFE5I%3D" /></p>
This opens a list of possible settings that we can configure, including the Desktop Wallpaper. To set the wallpaper to a specific value, double-click on the Desktop Wallpaper entry.
<p><img alt="" src="https://cdn.qwiklabs.com/PiWUn99iQ6pMJbPFGrbDVtd4ZNiUe2wxZhA5vCuKwWA%3D" /></p>
The window that opens allows you to set the value of the wallpaper. To do that, first click on the Enabled button and then enter a path for the wallpaper. The path could be a local path in the machine or a network path on a server that shares files.

For this lab, simply enter C:\Qwiklabs\wallpaper.jpg in the section Wallpaper Name.

Once you click OK, the group policy is created and contains the values we want. To verify this, go back to the Group Policy Management application and click the Settings tab of the new policy.

Note: This may show a warning that the application needs to be allowed to generate web content. You will need to Add the application as a trusted website in order to view its contents.
<p><img alt="" src="https://cdn.qwiklabs.com/othjw%2BpQDJhbv29EvHa7pYONszFydvRwS8rji77k89Y%3D" /></p>
By clicking the show links in the webpage, you can see that the policy has been defined and that the only setting being modified is the Desktop Wallpaper, which is set to the value we set above.

<h2>Conclusion<h2>

You've now seen how to manage users, groups and group policies using Active Directory. There's a lot more to learn about AD, but these skills are the building blocks for administering a fleet of Windows computers.



