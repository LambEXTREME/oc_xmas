# :christmas_tree: ownCloud Xmas
Add a christmas sprinkle to your ownCloud installations

Latest release: 0.0.4. [Changelog](https://github.com/tomneedham/oc_xmas/blob/master/CHANGELOG.md).
## :battery: Features
 - Snowflakes! :snowflake::snowflake::snowflake:
 
## :wrench: Usage
1. Install and enable the app. This gives you snowflakes everywhere by default
2. You can selectively disable snowflakes:

 - `occ config:app:set xmas showOnLogin --value=false` Disables snow flakes on the login
 - `occ config:app:set xmas showOnFiles --value=false` Disables snow fakes on the files app
 - `occ config:app:set xmas showOnPublicShare --value=false` Disables snow flakes on the public share page
3. Enjoy!
 
## :bulb: Roadmap / Ideas
 - Folder icons should be presents :gift: [see issue #8](https://github.com/tomneedham/oc_xmas/issues/8)
 - Configurable appear / disappear snowflakes timers :alarm_clock: [see issue #9](https://github.com/tomneedham/oc_xmas/issues/9)
 - UI for configuring xmas app features :nail_care: [see issue #10](https://github.com/tomneedham/oc_xmas/issues/10)
  
 ## :rocket: Get Involved!
 Why not take one of the ideas above and submit a pull request to the repository with your fix?
 
## Install app for testing & development

Install Docker: http://www.itzgeek.com/how-tos/linux/debian/how-to-install-docker-on-debian-9.html

Install ownCloud via docker:

```
cd ~
git clone https://github.com/owncloud-docker/server docker-owncloud
cd docker-owncloud
export OWNCLOUD_VERSION=10.0
export OWNCLOUD_DOMAIN=localhost
export OWNCLOUD_ADMIN_USERNAME=admin
export OWNCLOUD_ADMIN_PASSWORD=admin
export OWNCLOUD_HTTP_PORT=80
export OWNCLOUD_HTTPS_PORT=443
docker-compose up -d
```

You can now log in to your ownCloud on https://localhost/ .

To install the app, enter the docker container command line:

```
docker exec -ti dockerowncloud_owncloud_1 bash
```

Now you have to install a few dependencies and the app itself:

```
apt update
apt install npm git make
cd apps
git clone https://github.com/LambEXTREME/oc_xmas
cd oc_xmas
make
```

Then you can go to http://localhost/settings/admin?sectionid=apps&category=disabled , find
the disabled oc_xmas app, and enable it.

If there is no error message, it should work now.
