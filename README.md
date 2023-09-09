# What is WP-CLI?

[WP-CLI](https://wp-cli.org/) is an open-source project that is actively developed and maintained by a community of developers. It is compatible with most UNIX-like operating systems, including Linux, macOS, and Windows. WP-CLI requires PHP 5.6.0 or later and can be installed as a global package or a local dependency using the Composer package manager.

One of the main advantages of using WP-CLI is its speed and efficiency. Using command-line tools is often faster than navigating through a GUI, especially when performing repetitive tasks or automating complex operations. WP-CLI commands can be easily scripted and integrated with other command-line tools, making them powerful for developers.

# Advantages of WP-CLI
- Speed and Efficiency
- Improved Productivity
- Enhanced Control
- Improved Security
- Task Automation (WP-CLI can automate many common WordPress tasks, such as backups, updates, and optimization. This can save you time and reduce the risk of human error.)

# Requirements of WP-CLI
To install WP-CLI, you need a hosting solution that offers SSH access.
- **PHP:** WP-CLI requires PHP 5.6.0 or later.
- **WordPress:** WP-CLI is designed to work with WordPress 3.7 or later.
- **Operating System:** WP-CLI is compatible with Linux, macOS, and Windows OS. However, WP-CLI offers limited support in the Windows environment.

These are the basic requirements to install and use WP-CLI. 

# How to Install WP-CLI
To install WP-CLI, you can follow these simple steps:
- **Step 1: Connect to the Root Directory via SSH**

To use SSH access to your server, you need credentials (admin username, password), server IP, and port.

**For Windows,** PuTTY;

**For Linux,** Ubuntu;

**For Mac,** Termius;

 I use PuTTY.
- In PuTTY, go to Sessions;
- Enter the Host Name (or IP address) and Port;
- Select SSH for Connection Type;
- Click the Open button at the end.

In the next step, the process will prompt you to enter your username and password, which you can find in the Server Details.

- **Step 2: Download WP-CLI on Your Server**

R  un the following command to download the WP-CLI:
```
curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
```
```
chmod +x wp-cli.phar
```
```
php wp-cli.phar --info
```

# How to Use WP-CLI

Once you have installed WP-CLI on your computer, you can open a Terminal window and run different WP-CLI commands by typing “wp” followed by the command and its arguments.

- **1. Manage WordPress via WP-CLI**

**Download WordPress**
The following command will download the latest version of the WordPress core files.

```
wp core download
```

**Create wp-config File**

Use the following command to create the wp-config.php file

```
wp config create --dbname=WPcli --dbuser=root --dbpass=password 
```
I have used the following database details:
- **Database Name:** WPcli
- **Database Username:** root
- **Database Password:** password

**Create Database**
Use the following command to create the database. Note that this command will create a fresh database with the name used in the wp-config file.
```
wp db create
```

**Install WordPress**
It is easy to install WordPress from the command line using WP-CLI on your server. The command requires parameters including URL, Title, Admin Username, Password, and Admin Email.

```
wp core install --url=your_domain --title=Your_Blog_Title --admin_user=username --admin_password=password --admin_email=your_email.com
```
- **2. Manage WordPress Theme via WP-CLI**
Using WP-CLI, you can connect the server directly to the WordPress theme repository and import the theme quickly. Installing and activating WordPress via WP-CLI processes are simple. You can also update and delete themes through WP-CLI as well.

Use the following command to install a theme. For example, Twenty Twenty Three,
```
wp theme install twentytwentythree
```
To activate the theme, run the following command.
```
wp theme activate twentytwentythree
```
- **3. Manage WordPress Plugin via WP-CLI**
To install a WordPress plugin, run the following command.
Let’s also install WooCommerce
```
wp plugin install woocommerce
```
to activate it, run the following command.
```
wp plugin activate woocommerce
```
- **4. Manage WordPress Core via WP-CLI**
To check the version of the WordPress Core, run the following command.
```
wp core version
```
That will return the version of the WordPress Core. To update the Core files, run the following command.
```
wp core update
```

- **5. Search or Replace Strings via WP-CLI**
Use the following WP-CLI command for search & replace:
```
wp search-replace https://oldsite.com https://newsite.com
```

- **6. List All Supported Commands of WP-CLI**
Run the following command to get more details about the command
```
wp help <command name>
```
Run the following command to get more details about the plugin commands.
```
wp help plugin
```

## List of WP-CLI Commands
| Command | Function  |
| :---:   | :---: | 
| wp help | Details about command and options   | 
| wp cli version | To check the WP CLI version   | 
| php wp-cli.phar –info	 | Making file executable   | 
| wp core download	 | Download the latest version of the WordPress core files   | 
| wp config create | Create config file   | 
| wp db create | Create a new DB   | 
| wp theme install | Install theme | 
| wp theme activate | Activate theme  | 
| wp theme deactivate | Deactivate theme  | 
| wp plugin install | Install plugin  | 
| Install plugin | Activate plugin  | 
| wp search-replace | Searches/replaces strings in DB  | 
| wp help plugin | Details about the Plugin command  | 
