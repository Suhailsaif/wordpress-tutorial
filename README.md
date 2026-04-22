📘 WordPress Tutorial – README
📌 Overview

This project is a complete WordPress tutorial covering everything from basic setup to advanced development. It is designed for beginners as well as developers who want to build custom themes, plugins, and REST APIs.

🚀 Features Covered
WordPress Installation (Local & Live)
Theme Development (Custom Theme)
Plugin Development (Custom Plugin)
Custom Post Types (CPT)
Custom Fields (ACF / Meta Fields)
WordPress REST API
Authentication (JWT / Cookies)
Hooks (Actions & Filters)
Shortcodes
Widgets
Security Best Practices
Performance Optimization
Headless WordPress (Vue.js / React)
🛠️ Prerequisites

Make sure you have:

PHP (>= 7.4 or 8.x)
MySQL
Apache / Nginx (XAMPP / WAMP / MAMP)
Basic knowledge of:
HTML, CSS, JavaScript
PHP
⚙️ Installation Guide
1. Download WordPress
Go to WordPress official website
Download latest version
2. Setup Project
# Move WordPress to htdocs (XAMPP)
C:/xampp/htdocs/wordpress-project
3. Create Database
Open phpMyAdmin
Create a database (e.g. wp_tutorial)
4. Configure wp-config.php
define('DB_NAME', 'wp_tutorial');
define('DB_USER', 'root');
define('DB_PASSWORD', '');
define('DB_HOST', 'localhost');
5. Run Project
http://localhost/wordpress-project
📂 Project Structure
wordpress-project/
│
├── wp-admin/
├── wp-content/
│   ├── themes/
│   │   └── custom-theme/
│   ├── plugins/
│   │   └── custom-plugin/
│
├── wp-includes/
└── wp-config.php
🎨 Theme Development
Create Theme Folder
wp-content/themes/custom-theme
Required Files
style.css
index.php
Example: style.css
/*
Theme Name: Custom Theme
Author: Your Name
Version: 1.0
*/
Example: index.php
<?php get_header(); ?>

<h1>Hello WordPress Theme</h1>

<?php get_footer(); ?>
🔌 Plugin Development
Create Plugin File
wp-content/plugins/custom-plugin/custom-plugin.php
Basic Plugin Example
<?php
/*
Plugin Name: Custom Plugin
Description: My first plugin
Version: 1.0
*/

function my_custom_function() {
    echo "Hello from plugin!";
}
add_action('wp_footer', 'my_custom_function');
🔗 Hooks in WordPress
Action Hook
add_action('init', function() {
    // Runs on init
});
Filter Hook
add_filter('the_title', function($title) {
    return "Modified: " . $title;
});
📡 REST API Example
Register Custom Route
add_action('rest_api_init', function () {
    register_rest_route('api/v1', '/data', array(
        'methods' => 'GET',
        'callback' => 'my_api_callback',
    ));
});

function my_api_callback() {
    return ['message' => 'Hello API'];
}
🔐 Security Tips
Sanitize inputs (sanitize_text_field)
Escape output (esc_html)
Use Nonces
Avoid direct SQL queries
⚡ Performance Tips
Use caching plugins
Optimize images
Minify CSS/JS
Use CDN
🧠 Advanced Topics
Gutenberg Block Development
Headless WordPress with:
Vue.js
React.js
WooCommerce Customization
Multisite Setup
📚 Useful Resources
Official Docs: https://developer.wordpress.org
Plugin Repo: https://wordpress.org/plugins
🤝 Contributing

Feel free to fork and contribute to this project.

📄 License

This project is open-source and free to use.

👨‍💻 Author

Mohammad Suhail
Full Stack Developer (Laravel | Vue.js | WordPress)
