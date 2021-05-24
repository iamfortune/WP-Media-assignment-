Hello! 
My site is showing a 500 error after I enabled WP Rocket. I need to fix this asap, this is really bad!


# Reply

Hello!
I'm sorry to hear this, however you can fix this with the steps below

- Create .htaccess backup: find your .htaccess file by connecting through your FTP client, once you find this, copy the current version and rename it. Next, remove all the WP Rocket rules and leave just the default WordPress rules. If your site comes back online after this, however if it doesn't, you can increase the memory limit of your server. 

to increase your memory limit, you can use `wp-config.php` and running the code block below

`define( 'WP_MAX_MEMORY_LIMIT', '256M' );`

This will increase your memory access, however if this doesn't work, you should consider running an increase in memory using `.htaccess`, this can be done by adding the snippet below 
`php_value memory_limit 128M`