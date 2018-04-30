---
title: Installing Kurukshetra
tags: [introduction]
sidebar: mydoc_sidebar
permalink: install.html
summary: Once the environment is set, let's install kurukshetra
---

Once the environment is set, we can go ahead and install kurukshetra just like a CMS installation. Installing kurukshetra is as simple as moving the downloaded files into webroot:

```bash
# Clone the github repo and move all the files into Web root
git clone https://github.com/a0xnirudh/kurukshetra.git
cd kurukshetra
cp -r * /var/www/html/

# Appropriate permissions to the files
chmod 755 -R /var/www/html

# Make Apache the owner of **uploads** directory
chown www-data /var/www/html/challenges/uploads
```

Visit `http://localhost` or `http://127.0.0.1` to navigate into installation (will auto redirect into /installation/).

{% include warning.html content="
The project files must be on the webroot or else location redirection's will fail to work and hence project won't work properly.
"%}

While visiting, since it's the first time (installation is not yet done), it will redirect to `/installation/index.php`, where we should enter the MySQL db credentials (user should have the permission to create database) and click on validate to see if the credentials are correct.

{% include image.html file="install.png" alt="Installing kurukshetra" caption="Installing and configuring kurukshetra" %}

Click next and enter the Google OAuth **Client ID** and **Client secret** and make sure the redirect URL is set to the path `http://your-domain.com/login/index.php` in the OAuth settings. As of now the framework only supports Google OAuth based login.


{% include important.html content="
The first logged in user immediately after the installation is automatically given the **Admin** privileges. Please make sure to login first with a valid account immediately once installation is over.
"%}

Once the installation is done correctly, you can visit `http://127.0.0.1` which will give the login page to the user (only Google login is supported as of now).