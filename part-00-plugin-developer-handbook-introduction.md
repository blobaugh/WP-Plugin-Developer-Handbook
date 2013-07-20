Hi! Thanks for checking out the Plugin Developer Handbook. Whether you’re writing your first plugin or your fiftieth, we hope this resource helps you write the best plugin possible.

The Plugin Developer Handbook covers a variety of topics; everything from what should be in the plugin header, to security best practices, to tools you can use to build your plugin. It’s also a work in progress — if you find something missing or incomplete, please edit and make it better.

### What are Plugins?

Plugins are packages of code that extend the core functionality of WordPress. WordPress plugins are made up of PHP code, and often some CSS, JavaScript, and other files.

By making your own plugin, you’re building additional functionality on top of what WordPress already offers.  For instance, you could write a plugin that allows you to show links to the 10 most recent posts on your site.

Or, using WordPress’ custom post types, you could write a plugin that that creates a full-featured support ticketing system with email notifications, custom ticket statuses, and a client-facing portal. The possibilities are endless.

Most WordPress plugins are comprised of many files, but a plugin really only needs two main files – the main plugin PHP file and a README.txt file.

Hello Dolly, one of the first plugins, is only [82 lines long](http://plugins.trac.wordpress.org/browser/hello-dolly/trunk/hello.php). Hello Dolly shows lyrics from the famous song in the WordPress Dashboard. There’s some CSS in the PHP file to control how the lyric is styled. Its [README.txt](http://plugins.trac.wordpress.org/browser/hello-dolly/trunk/readme.txt) file contains information about the plugin including version and author data, and explains what the plugin does, and how it’s listed in the [WordPress.org Plugin Repository](http://wordpress.org/extend/plugins/hello-dolly/).

As a WordPress.org plugin author, you have an amazing opportunity to have your plugin installed, tinkered with, and loved by millions of WordPress users. All you’ll need to do is turn your great idea into code. And we’re here to help you with that.