## Embed Functionality in Post Content with the Shortcode API

### Overview

WordPress' Shortcode API enables you to provide the end user with a macro they can place within Post Content. A macro is a *placeholder* to represent a photo gallery, list of posts, contact form or other piece of dynamic functionality.

At the minimum, using the Shortcode API involves registering both a shortcode and callback function with `add_shortcode();` It's as though you're allowing the end user to use PHP functions within their post content, but in a much safer, more protected manner.

### Why Shortcodes?

Shortcodes are a valuable way of keeping content clean and semantic, and affording end users some ability to programmatically alter the presentation of their content. When the end user adds a photo gallery to their post using a shortcode, they're using the least data possible to indicate how gallery should be presented. One key advantage: no markup is added to the post content, which means that markup and styling can easily be manipulated on the fly or at a later date. Shortcodes can also accept parameters, allowing users to modify how the shortcode behaves on an instance by instance basis.

### Diving Into Your First Shortcode

Sold on adding a shortcode or two to your plugin? Let's take a look at how they work under the surface.

#### The WordPress [gallery] Shortcode

WordPress bundles a photo gallery shortcode in every instance. Here's what that will look like to a writer or editor:

```
[gallery]
```

Drop that in the body of your post, upload a few photos as post attachments, and voila! When the post is previewed or published, the shortcode is transformed into a beautiful gallery.

Shortcodes can also have configuration parameters (or "attributes"). A gallery shortcode with a couple of attributes would look like this:

```
[gallery id="123" size="medium"]
```

#### Registering A Shortcode In Your Plugin

Shortcodes are registered with WordPress by declaring a shortcode and assigning a callback. At it's simplest, here's a Hello Dolly example:

function hello_dolly_shortcode() {
    return "Hello Dolly";
}
add_shortcode( 'hello-dolly', 'hello_dolly_shortcode' );

`[hello-dolly]` is your new shortcode, and use of the shortcode will trigger the hello_dolly_shortcode() callback function.

Shortcode callback functions can receive up to three parameters:

* $atts, an associative array of attributes, or an empty string if no attributes are given
* $content, the enclosed content (if the shortcode wrapped around some content)
* $tag, the current shortcode tag, useful for shared callback functions


ENCLOSING VS. SELF-CLOSING SHORTCODES

@todo just include this entire section from the document


### Shortcode Best Practices

**Return, don't output.** Your callback function should *return* the output, not *echo*. Doing the latter could cause your output to end up in unexpected locations, as shortcodes aren't always rendered within the Loop.

- Prefix your shortcode
- Sanitize the input, and escape the output
