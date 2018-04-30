---
title: Managing Users
sidebar: mydoc_sidebar
permalink: manage_users.html
summary: New admins can be added by already existing administrators from the kurukshetra dashboard. Admins can also disable existing users and prevent them from logging in back to the framework.
---

Administrators has the ability to manage users by adding more administrators (existing users can be made admins from the dashboard) or by also disabling login to the framework by blacklisting the email address.

### Adding Administrators

Once logged in as **admin**, visit `/admin/users.php` to list all the users who has logged in (atleast once) into kurukshetra.

{% include image.html file="user_management.png" alt="managing users in kurukshetra" caption="Managing users in kurukshetra" max-width=850%}
 
 Simply click on the tickbox next to each user to make them an admin.
 
{% include important.html content="
While adding new administrators, be very careful. An administrator can also remove admin privileges from other administrators (making them a normal user) or even block them from logging into the framework again."%}
 
 
### Disable users
 
Once logged in as **admin**, visit `/admin/users.php` to list all the users who has logged in (atleast once) into kurukshetra. You can disable a user login by simply unchecking the checkbox named **Enable?** and the framework will disable that account login until its re-enabled manually by an admin.
 
{% include tip.html content="
By default, a new user logging into the framework is automatically enabled. To disable a user, an administrator has to manually disable the user login from the dashboard."%}