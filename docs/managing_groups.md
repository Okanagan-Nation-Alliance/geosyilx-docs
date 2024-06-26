## Managing Groups

### Creating Groups

In GeoNode is possible to create new groups with set of permissions which will be inherited by all the group members.
The creation of a Group can be done both on the GeoNode UI and on the Admin Panel.

The Create Groups link of About menu in the navigation bar allows administrators to reach the Group Creation Page.

"Placeholder for the screenshot"

Fill out all the required fields in the resulting form and click Create to create the group. The Group Details Page will open.


As already mentioned above, groups can also be created from the Django-based Admin Interface of GeoNode.
The Groups link of the AUTHENTICATION AND AUTHORIZATION section allows to manage basic Django groups which only care about permissions.
To create a GeoNode group you should take a look at the GROUPS section.

Types of Groups

In GeoNode users can be grouped through a Group Profile, an enhanced Django group which can be enriched with some further information such as a description, a logo, an email address, some keywords, etc. It also possible to define some Group Categories based on which those group profiles can be divided and filtered.

A new Group Profile can be created as follow:

- click on the Group Profile + Add button

- fill out all the required fields (see the picture below), Group Profiles can be explicitly related to group categories

- click on Save to perform the creation, the new created group profile will be visible in the Group Profiles List

Group Categories

Group Profiles can also be related to Group Categories which represents common topics between groups. In order to add a new Group Category follow these steps:

- click on the Group Categories + Add group category button

- fill out the creation form (type name and description)

### Modifying Groups
Through the Groups link of About menu in the navigation bar, administrators can reach the Groups List Page.

For each group some summary information (such as the title, the description, the number of members and managers) are displayed near the Group Logo.

Administrators can manage a group from the Group Profile Details Page which is reachable by clicking on the title of the group.


As shown in the picture above, all information about the group are available on that page:

- the group Title;

- the Last Editing Date which shows a timestamp corresponding to the last editing of the group properties;

- the Keywords associated with the group;

- Permissions on the group (Public, Public(invite-only), Private);

- Members who join the group;

- Managers who manage the group.


The Edit Group Details link opens the Group Profile Form through which the following properties can be changed:

- Title.

- Logo.

- Description.

- Email, to contact one or all group members.

- Keywords, a comma-separated list of keywords.

- Access, which regulates permissions:

    - Public: any registered user can view and join a public group.

    - Public (invite-only): only invited users can join, any registered user can view the group.

    - Private: only invited users can join the group, registered users cannot see any details about the group, including membership.

- Categories, the group categories the group belongs to.

Manage Group Members.

   the Delete this Group, click on it to delete the Group Profile. GeoNode requires you to confirm this action.

   the Group Activities drives you to the Group Activities Page where you can see all datasets, maps and documents associated with the group. There is also a Comments tab which shows comments on those resources.

   The Manage Group Members link opens the Group Members Page which shows Group Members and Group Managers. Managers can edit group details, can delete the group, can see the group activities and can manage memberships. Other Members can only see the group activities.
   In Public Groups, users can join the group without any approval. Other types of groups require the user to be invited by the group managers.
   Only group managers can Add new members. In the picture below, you can see the manager can search for users by typing their names into the User Identifiers search bar. Once found, he can add them to the group by clicking the Add Group Members button. The Assign manager role flag implies that all the users found will become managers of the group.

If you want to change the role of group members after adding them, you can use the “promote” button to make a member into a manager, and the “demote” button to make a manager into a regular member.


**Group based advanced data workflow**

By default GeoNode is configured to make every resource suddenly available to everyone, i.e. publicly accessible even from anonymous/non-logged in users.

It is actually possible to change few configuration settings in order to allow GeoNode to enable an advanced publication workflow.

With the advanced workflow enabled, your resources won’t be automatically published (i.e. made visible and accessible for all, contributors or simple users).

For now, your item is only visible by yourself, the manager of the group to which the resource is linked (this information is filled in the metadata), the members of this group, and the GeoNode Administrators.

Before being published, the resource will follow a two-stage review process, which is described below:


pLACEHOLDER FOR SCREENSHOT



How to enable the advanced workflow

You have to tweak the GeoNode settings accordingly.

Please see the details of the following GeoNode Settings:

- `RESOURCE_PUBLISHING`

- `ADMIN_MODERATE_UPLOADS`

- `GROUP_PRIVATE_RESOURCES`

Summarizing, when all the options above of the Advanced Workflow are enabled, upon a new upload we will have:

- The “unpublished” resources will be hidden to anonymous users only. The registered users will be still able to access the resources (if they have the rights to do that, of course).

- The “unpublished” resources will remain hidden to users if the permission (see Admin Guide section: ‘Manage Permissions’) will be explicitly removed

- During the upload, whenever the advanced workflow is enabled, the owner’s Groups are automatically allowed to access the resource, even if the “anonymous” flag has been disabled. Those permissions can be removed later on

- During the upload, “managers” of the owner’s Groups associated to the resource, are always allowed to edit the resource, the same as they are admin for that resource

- “managers” of the owner’s Groups associated to the resource are allowed to “publish” also the resources, not only to “approve” them



Change the owner rights in case of advanced workflow is on

After switching ADMIN_MODERATE_UPLOADS to True and resource is approved owner is no longer able to modify it. He will see new button on the resource detail page: Request change. After clicking this, view with short form is shown. On this view user can write short message why he want to modify the resource.

This message will be sent through messaging and email system to administrators:

After administrator unapprove the resource owner is again able to modify it.
The group Manager approval

Here, the role of the Manager of the group to which your dataset, document or map is linked is to check that the uploaded item is correct. Particularly, in the case of a dataset or a map, it consists of checking that the chosen cartographic representation and the style are fitting but also that the discretization is appropriate.

The Manager must also check that the metadata are properly completed and that the mandatory information (Title, Abstract, Edition, Keywords, Category, Group, Region) are filled.

If needed, the Manager can contact the contributor responsible of the dataset, document or map in order to report potential comments or request clarifications.

Members of the group can also take part in the reviewing process and give some potential inputs to the responsible of the dataset, document or map.

When the Manager considers that the resource is ready to be published, he should approve it. To do so, the Manager goes to the resource detail page, then opens the Edit Metadata. In the Settings tab, the manager checks the Approved box, and then updates the metadata and saves the changes:

Following this approval, the GeoNode Administrators receive a notification informing them that an item is now waiting for publication
The publication by the GeoNode Administrator

Prior to the public release of an approved resource, the Administrator of the platform performs a final validation of the item and its metadata, notably to check that it is in line with license policies.

If needed, the GeoNode Administrator can contact the Manager who has approved the resource, as well as its responsible.

Once the resource is validated, the item is made public by the Administrator. It can now be viewed, accessed, and downloaded in accordance with the Permissions set by the responsible contributor.
Promotion, Demotion and Removal of Group Members

If the owner is a group Manager, They have permissions to edit, approve, and publish the resource.

When a group member is promoted to a manager role, they gain permissions to edit, approve and publish the resource.

When a group manager is demoted to a member role, they lose edit permissions of the resource and only remain with view and download permissions.

When a member is removed from the group, they can nolonger access the unpublished resource anymore.
Manage profiles using the admin panel

So far GeoNode implements two distinct roles, that can be assigned to resources such as datasets, maps or documents:

- party who authored the resource

- party who can be contacted for acquiring knowledge about or acquisition of the resource

These two profiles can be set in the GeoNode interface by accessing the metadata page and setting the Point of Contact and Metadata Author fields respectively.

Is possible for an administrator to add new roles if needed, by clicking on the Add contact role button in the Base -> Contact Roles section:



Clicking on the People section (see figure) will open a web for with some personal information plus a section called Users.



Is important that this last section is not modified here unless the administrator is very confident in that operation.




