---
node_id: 702
title: Using WP-SuperCache to optimize Wordpress on Cloud Sites
type: article
created_date: '2011-03-16'
created_by: Thomas Hester
last_modified_date: '2014-10-15'
last_modified_by: Jered Heeschen
product: Cloud Sites
product_url: cloud-sites
---

WP Super Cache is an available plugin for [Wordpress
installations](%20http://www.rackspace.com/cloud/sites/web-hosting/wordpress/)
to store cached versions of your dynamic PHP pages. Installing WP Super
Cache can also reduce the number of compute cycles used by a site since
it reduces the load on the cluster as well.

WP Super Cache is available at
<http://wordpress.org/extend/plugins/wp-super-cache> and is included by
default with the Wordpress One Click Install in the control panel.

### Before You Begin

-   Have your Rackspace Cloud Control Panel login credentials ready.

### Install WP Super Cache

To install WP Super Cache, follow the instructions provided for the
plugin located here:
<http://wordpress.org/extend/plugins/wp-super-cache/installation/>. If
you have installed Wordpress via the Wordpress One Click Installer you
already have Super Cache installed.

### Recommended configuration

In addition to the instructions included with the manual, the following
additional changes are recommend and have been tested and shown to
increase the efficiency of WP Supercache in Cloud Sites.

#### Advanced settings

Go to settings for SuperCache and click on the **Advanced** tab.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Tabs.png" width="615" height="52" />

Mark the following items:

-   Cache hits to this website for quick access. (Recommended)
-   Use mod\_rewrite to serve cache files. (Recommended)
-   Compress pages so they&rsquo;re served more quickly to visitors.
    (Recommended)
-   Don&rsquo;t cache pages for known users. (Recommended)
-   Cache rebuild. Serve a supercache file to anonymous users while a
    new file is being generated. (Recommended)
-   Mobile device support. (External plugin or theme required. See the
    FAQ for further details.)
-   Extra homepage checks. (Very occasionally stops homepage caching)
    (Recommended)

After making those changes, click **Update Status**.

#### Mod\_rewrite settings

After the screen refreshes scroll down to the Mod Rewrite Rules section
and click **Update Mod\_Rewrite Rules**.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/RewriteRules1.png" width="689" height="200" />

#### Expiry time and garbage collection

Scroll down to **Expiry Time & Garbage Collection**.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/gc_1.png" width="645" height="243" />

Change cache timeout to 0 seconds then click **Change Expiration**.

#### Preload settings

Click on the **Preload** tab next.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Preload_0.png" width="949" height="313" />

-   Select **Preload mode (garbage collection only on legacy
    cache files. Recommended.)**.
-   Set the refresh rate for preloaded supercache files by changing the
    number of minutes in the **Refresh preloaded cache files every
    \_\_\_ minutes** field (0 to disable, minimum 30 minutes) to a
    number appropriate for the traffic your site receives, like 1440
    (24 hours) or 10080 (1 week).
-   Click **Update Settings**, then after the page refreshes click
    **Preload Cache Now** and in around 10 or 15 seconds the cache will
    start building for the site. Depending on the size of the site and
    amount of content, the cache will take a few seconds to a minute
    to build. Once complete you will see a much improved response and
    load time.

Any time a layout change has been made (such as adding a widget or
changing the theme), it will be necessary to go to the admin panel and
click **Delete cache**, verify your page looks as you want, then go into
into the Supercache settings, go to the **Preload** tab and click
**Preload Cache Now** to regenerate the cache for the site.

### Updating the Supercache plugin

For security purposes and optimizations, it is important to keep the
plugin (and Wordpress itself) up-to-date. This can be done through the
Wordpress Dashboard.

1.  <span style="line-height: 1.538em;">Login to your
    WordPress Dashboard.</span>
2.  <span style="line-height: 1.538em;">Click the **Plugins** tab on the
    left-hand column.</span>
3.  <span style="line-height: 1.538em;">Check the box next to **Plugin**
    to select all available plugin updates.</span>
4.  <span style="line-height: 1.538em;">Click the **Bulk Actions** drop
    down and select **Update**.</span>
5.  <span style="line-height: 1.538em;">Click **Apply**.</span>
6.  <span style="line-height: 1.538em;">The page will change once all of
    the plugins are updated.</span>


