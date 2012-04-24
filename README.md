google-news-sitemap-generator
=============================

Git clone of http://plugins.svn.wordpress.org/google-news-sitemap-generator/trunk/ (which seems unmaintained)

Fixes :

  1. Remove DATEDIFF usage within the sitemap creation - this should lead to a reasonable performance increase, especially if there is an index on the appropriate field(s) in wp_posts (see below).
  2. Use a long style opening PHP tag.
  3. Fix issue with latest post not appearing (See http://wordpress.org/support/topic/plugin-google-news-sitemap-generator-fix-to-not-adding-latest-post-to-sitemap)
  4. Try to ensure google-news-sitemap.xml is saved to the right place - see http://wordpress.org/support/topic/plugin-google-news-sitemap-generator-not-synched-outside-webroot
  5. Try to stop special characters from  messing up the XML formatting... see new function _escape_html_stuff($string).
  6. Remove any HTML tags which might be present in the title - see http://wordpress.org/support/topic/plugin-google-news-sitemap-generator-in-title?


You almost certainly want to create an additional index on your wp_posts table as follows :

  CREATE INDEX post_status_post_date_gmt_type_idx on wp_posts(post_status, post_date_gmt, post_type);

Which will make it perform a lot better, especially as your site grows and has many thousands of wp_post entries.
