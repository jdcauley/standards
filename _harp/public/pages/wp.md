Cuberis often uses WordPress to create client sites and develops custom functionality through plugin and them integrations as needed.

### Theme Development

Cuberis uses a modified verstion the Roots.io/sage theme. This provides significant development advatages including Gulp powered preprocessing, linting, minification, and concatenation. Additionally, the theme uses Browsersync to smooth testing and allows the ability to navigate pages in multiple browsers.

For documentation specifically related to theme features please refer to the documenation at https://roots.io/sage/docs/

The tools and functions of Sage allow for rapid development using industry best practices. This includes concatenation and minification of all CSS and JS files.

The theme also includes a bower file for importing the Bootstrap frontend framework for baseline mobile first CSS and JavaScript.

### Function File

As a general practice Cuberis embraces the file structure concepts of Sage. Assets and Function are placed in folders and referenced accordingly.

The <code>functions.php</code> file is only used to reference appropriate files in the lib folder.

This allows for subfolders to include advanced functionality including external libraries with out crowding the theme's root directory. An example might be a custom, theme specific external integration to APIs like Zendesk or Stripe.

### Plugins

As a rule Cuberis embraces a minimalistic approach to the use of plugins. If functionality can easily be built into the theme, that is prefereable to addition of external plugins. For more complicated enhancements there are several plugins that are used within nearly every project including:

* Advanced Custom Fields
* Gravity Forms
* WordPress SEO
* Backup Buddy
