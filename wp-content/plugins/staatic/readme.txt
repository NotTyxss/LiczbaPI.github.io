=== Staatic - Static Site Generator ===
Contributors: staatic
Tags: performance, seo, security, static, speed
Stable tag: 1.9.3
Tested up to: 6.5
Requires at least: 5.0
Requires PHP: 7.1
License: BSD-3-Clause

Staatic lets you create and deploy a streamlined static version of your WordPress site.

== Description ==

Staatic lets you create and deploy a streamlined static version of your WordPress site, enhancing performance, SEO, and security simultaneously.

Features of Staatic include:

* Powerful Crawler to transform your WordPress site quickly.
* Supports multiple deployment methods, e.g. GitHub, Netlify, AWS (Amazon Web Services) S3 or S3-compatible providers + CloudFront integration, or even your local server (dedicated or shared hosting).
* Very flexible out of the box (allows for additional urls, paths, redirects, exclude rules, etc.).
* Supports HTTP (301, 302, 307, 308) redirects, custom “404 not found” page and other HTTP headers.
* CLI command to publish from the command line.
* Compatible with WordPress MultiSite installations.
* Compatible with WPML (multilingual) installations.
* Supports HTTP basic auth protected WordPress installations.
* Various integrations to improve compatibility with popular WordPress plugins.

Depending on the chosen deployment method, additional features may be available.

== Installation ==

Installing Staatic is simple!

### Install from within WordPress

1. Visit the plugins page within your WordPress Admin dashboard and select ‘Add New’;
2. Search for ‘Staatic’;
3. Activate ‘Staatic’ from your Plugins page;
4. Go to ‘After activation’ below.

### Install manually

1. Upload the ‘staatic’ folder to the `/wp-content/plugins/` directory;
2. Activate the ‘Staatic’ plugin through the ‘Plugins’ menu in WordPress;
3. Go to ‘After activation’ below.

### After activation

1. Click on the ‘Staatic’ menu item on the left side navigation menu;
2. On the settings page, provide the relevant Build & Deployment settings;
3. Start publishing to your static site!

== Frequently Asked Questions ==

= How will Staatic improve the performance of my site? =

Staatic transforms your dynamic WordPress site into a streamlined static site. Starting at the homepage or a designated URL, Staatic uses a web crawler to methodically navigate through every link, post, and page. As it moves through the site, dynamically generated content is captured and converted into static HTML files, while simultaneously fetching related assets like images and scripts.

By eliminating both WordPress and PHP from the delivery process, pages from your site are served instantly, bypassing the delay of on-the-fly generation. This guarantees the quickest possible load times and significantly reduces the time to first byte (TTFB), offering an unparalleled browsing experience for your visitors and enhancing your site’s SEO positioning.

= Why not use a caching plugin? =

Caching plugins boost site performance by storing data for quicker access, yet they don’t fully bypass WordPress, introducing some latency. Additionally, after every update, these plugins need cache prewarming to serve the first requests quickly. In contrast, static sites are always ‘warmed up’, ensuring consistently rapid load times.

Furthermore, with Staatic, you gain the flexibility to host your site on any platform of your choice. This means you could opt for an ultra-fast cloud provider or a robust content delivery network, further amplifying your site’s performance and ensuring optimal user experience.

= Will the appearance of my site change? =

No, it shouldn’t. However, if there is a difference in the static version of your site, it might be due to invalid HTML in your original WordPress site that couldn’t be accurately converted. In such instances, consider checking your HTML’s validity using services like the [W3C Markup Validation Service](https://validator.w3.org/).

= How will Staatic improve the security of my site? =

By converting your site into static HTML pages, you substantially minimize the potential attack surface. This strengthens your website’s security and reduces the ongoing need to update WordPress, its plugins, and themes constantly. As a result, you can enjoy greater peace of mind, knowing your site is resilient to most threats.

= Is Staatic compatible with all plugins? =

Not entirely. When your site undergoes conversion to a static format, dynamic server-side functionalities become unavailable. As a result, plugins relying on these features – such as those processing forms or fetching external data – might not function immediately or might be unsupported altogether.

To accommodate such features, adjustments or alternatives may be necessary. Alternatively, you can opt for Staatic Premium, which seamlessly integrates some of these functionalities. For detailed insights, visit [staatic.com](https://staatic.com/wordpress/).

= Will Staatic function on shared or heavily restricted servers? =

Staatic offers broad compatibility, only requiring the permissions to write to the working directory and to initiate an HTTP connection with your dynamic WordPress installation.

= Where can I get help? =

If you have any questions or issues, please have a look at our [documentation](https://staatic.com/wordpress/documentation/) and [FAQ](https://staatic.com/wordpress/faq/) first.

If you cannot find an answer there, feel free to open a topic on our [Support Forums](https://wordpress.org/support/plugin/staatic/).

Want to get in touch directly? Please feel free to [contact us](https://staatic.com/wordpress/contact/). We will get back to you as soon as possible.

== Screenshots ==

1. Use your WordPress installation as a private staging environment and make all of the modifications you need. Then publish these changes to your highly optimized and consumer facing static site with the click of a button.
2. Monitor the status of your publications while they happen and review details of past publications to easily troubleshoot any issues.
3. Configure and fine tune the way Staatic processes your site to suit your specific needs.

== Changelog ==

= 1.9.3 =

Release date: March 26th, 2024.

**Improvements**

* Improves support for the AVIF image format.
* Various performance optimizations.
* Adds limited WordPress Playground support.
* The “Local Directory” deployment method now stores HTML files directly, rather than in subdirectories.
* No longer excludes `wp-content/uploads/cache` directory by default.
* Removes unnecessary content type directives from the generated Netlify config file.
* Updates external dependencies.

**Fixes**

* Correctly transforms complex URLs when using “Offline URLs” type destination URL.
* Uses correct status code when not explicitly specified for additional redirect.
* Fixes default value of “Excluded URLs” setting in directory-based network sites.
* Fixes default value of “Page Not Found Path” setting in directory-based network sites.

= 1.9.2 =

Release date: February 28th, 2024.

**Improvements**

* Updates external dependencies.

**Fixes**

* Fixes additional path legacy format conversion.

= 1.9.1 =

Release date: February 24th, 2024.

**Improvements**

* Improves overall compatibility with [WPML](https://wpml.org/) plugin.
* Adds support for spaces in additional URLs, paths, redirects and exclude rules.

**Fixes**

* Fixes URL detection on WPML installations.
* Fixes additional path URL conversion on Windows environment.
* Ensures consistent override of site's base URL and WordPress URL.

= 1.9.0 =

Release date: February 20th, 2024.

**Improvements**

* Re-enables compression of publication resources files.
* Adds support for symlinked uploads directory when having “Symlink/Copy Uploads” setting enabled.
* Improves environment specific path and URL detection for providing default configurations.
* Improves display of publication log summary on publication detail screen.
* Displays a notice for live publication status if preparation takes longer than expected.
* Allows the database to be reset in case database upgrades fail.
* Adds support for AWS region `ca-west-1`.
* Updates external dependencies.

**Fixes**

* Fixes reliability issue with compression of publication resource files.
* Delays scheduling of events while schedule does not exist.
* Fixes sorting latest publication overview by publisher and status.

= Earlier releases =

For the changelog of earlier releases, please refer to [the changelog on staatic.com](https://staatic.com/wordpress/changelog/).

== Upgrade Notice ==

= 1.8.2 =
Emergency patch to disable compression of publication resource files due to reliability issue.

= 1.8.0 =
Type definitions for `staatic_additional_paths` and `staatic_additional_redirects` filter hooks have changed.

== Staatic Premium ==

In order to support ongoing development of Staatic, please consider going Premium. In addition to helping the authors maintain Staatic, Staatic Premium adds additional functionality.

For more information visit [Staatic](https://staatic.com/wordpress/).
