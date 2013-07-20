## Part Four: Plugin Components

As you learned in the introduction, WordPress plugins vary quite significantly in how they extend the WordPress experience. Some plugins are less than ten lines of code, and others are thousands of lines with bundled JavaScript and CSS.

For the purpose of deconstructing how WordPress plugins do what they do, we'll break them into a series of components. Each component will then relate to one of WordPress' internal APIs.

To provide context on how using WordPress makes it easier to solve common problems, here are a few examples:

* The **Settings API** enables you to create an administrative interface for the user to change plugin options.
* **Admin AJAX** endpoints allow JavaScript to dynamically interact with WordPress.
* **Internationalization** support in every plugin will make it possible for translators to contribute localized strings.

Most importantly, following the design patterns expressed by each component means its easier for other WordPress developers to dive into your code.

