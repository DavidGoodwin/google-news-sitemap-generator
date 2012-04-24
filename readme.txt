(Original readme.txt file - see http://plugins.svn.wordpress.org/google-news-sitemap-generator/trunk/readme.txt )

=== Google News Sitemap Generator ===

Contributors: Chris Jinks, David Stansbury
Donate link: http://www.southcoastwebsites.co.uk/wordpress/
Tags: Google News, Sitemap, XML

Basic XML sitemap generator for submission to Google News.

== Description ==

Automatically generates a Google News XML sitemap for submission online via Webmaster Tools.

Follows Google guidelines:

* 50,000 item limit
* Posts from the last 2 days

Keywords for sitemap are generated from post category and post tags.

Optional categories can be excluded from Google News sitemap.

Updated to conform with new Google News Sitemap format.



== Installation ==

This section describes how to install the plugin and get it working.

1. Upload `google-news-sitemap-generator` directory to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Move the file "google-news-sitemap.xml" into your blog root directory and CHMOD to 777 so it is writable
4. Save/publish/delete a post to generate the sitemap
