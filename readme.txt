Plugin: Maintenance Mode
URL: http://habariproject.org
Version: 0.3
Author: Habari Project

Purpose 

The purpose of Maintenance Mode is to block access to your site while it is undergoing changes. When the site is in maintenance mode, anyone who is not a logged in user will see only a message saying the site is undergoing maintenance. There are three exceptions to this:

1. If a user is logged in, they will be able to view any page on the site.
2. In order to be able to log in, the login page is still accessible.
3. If the option is set to continue to supply feeds, all feeds will be viewable by all readers.

Requirements 

There are no special requirements.

Installation

1. Copy the plugin directory into your user/plugins directory or the site's plugins directory.
2. Go to the plugins page of your Habari admin panel.
3. Click on the Activate button for Maintenance Mode.

Usage

To configure Maintenance Mode, click on its configure button on the admin plugins page. You will see three options.

1. The text readers will see if they come to your site while it is maintenance mode. You can change this to anything you like. It can be styled in your theme's CSS (h2#maintenance_text). If you would prefer, you can also create a page named maintenance.php in your theme directory containing anything you like. If such a page is found, Maintenance Mode will display that page rather than using the text entered in the configuration options. That text is also accessible from the template should you want to use it, just use echo $theme->maintenance_text within maintenance.php.

2. A checkbox to put the site into maintenance mode and to take it out of maintenance mode.

3. A checkbox to set whether or not feeds will be available to all readers, even if the site is in maintenance mode.


Uninstallation

1. Got to the plugins page of your Habari admin panel.
2. Click on the Deactivate button.
3. Delete the maintenance_mode directory from your user/plugins directory.

Cleanup

None. Maintenance Mode deletes all options it creates on deactivation.

Changelog

Version 0.3
Changed: Added an option to allow feeds to be accessible to all readers, even if the site is in maintenance mode.
Changed: On deactivation, all options created by the plugin are removed from the database.
Fixed: Updated to allow for anonymous users.

Version 0.2
Changed default header from h1 to h2 and added an ID to make CSS styling easier.

Version 0.1
Initial release

