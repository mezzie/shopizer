# Rocket Shopizer

This is a fork of Shopizer for Rocket Insights mad experiments!

First things first, please make sure you are using the `2.7.0` branch to get going quickest, it's the most stable (as of this commit). It's been set as the default branch in this forked repo so hopefully you're already on it!

This is a huge repo with lots of maven modules. To get you going, here's some helpful hints:

* The build instructions are actually pretty good.  Follow 'em!
* `sm-shop` is the main web application and where you're going to be running out of.  The docs help you get going, but thought we'd call it out. It's a good starting point to go from.
* Once you have the app up and running locally, you can see swagger API docs at: [http://localhost:8080/swagger-ui.html#/](http://localhost:8080/swagger-ui.html#/)
* In addition to the store itself that the build guide links you to, we think using the admin interface at [http://localhost:8080/admin/](http://localhost:8080/admin/) is a good way to start understanding the data model. Login using username `admin` and password `password`.  The docs that shopizer has for the admin credentials are *wrong*.
* It's tough to get new test data into this app, so for ad hoc testing, we recommend simply going to the admin interface and adding it that way 
  * TODO once this is figured out, add a script to add some better test data
* Good luck!


Shopizer (for java 1.8 +)
-------------------
[![last_version](https://img.shields.io/badge/last_version-v2.7.0-blue.svg?style=flat)](https://github.com/shopizer-ecommerce/shopizer/tree/2..6.0)
[![Official site](https://img.shields.io/website-up-down-green-red/https/shields.io.svg?label=official%20site)](http://www.shopizer.com/)
[![Docker Pulls](https://img.shields.io/docker/pulls/shopizerecomm/shopizer.svg)](https://hub.docker.com/r/shopizerecomm/shopizer)
[![stackoverflow](https://img.shields.io/badge/shopizer-stackoverflow-orange.svg?style=flat)](http://stackoverflow.com/questions/tagged/shopizer)
-------------------

Java open source e-commerce software

- Shopping cart
- Catalogue
- Search
- Checkout
- Administration
- REST API

See the demo:
-------------------
http://demo.shopizer.com:8080


Get the code:
-------------------
Clone the repository:
     
	 $ git clone git://github.com/shopizer-ecommerce/shopizer.git

If this is your first time using Github, review http://help.github.com to learn the basics.

You can also download the zip file containing the code from https://github.com/shopizer-ecommerce/shopizer 

To build the application:
-------------------	
From the command line with Maven installed:

	$ cd shopizer
	$ mvn clean install
if Maven is not installed, use maven wrapper
       
	$ mvnw clean install
	

Run the application from Tomcat 
-------------------
copy sm-shop/target/ROOT.war to tomcat or any other application server deployment dir

Increase heap space to 1024 m

### Heap space configuration in Tomcat:


If you are using Tomcat, edit catalina.bat for windows users or catalina.sh for linux / Mac users

	in Windows
	set JAVA_OPTS="-Xms1024m -Xmx1024m -XX:MaxPermSize=256m" 
	
	in Linux / Mac
	export JAVA_OPTS="-Xms1024m -Xmx1024m -XX:MaxPermSize=256m" 

Run the application from Spring boot 
-------------------

       $ cd sm-shop
       $ mvn spring-boot:run
if Maven is not installed, use maven wrapper
       
	   $ mvnw spring-boot:run

Run the application from Spring boot in eclipse
-------------------

Right click on com.salesmanager.shop.application.ShopApplication

run as Java Application

### Access the application:
-------------------

Access the deployed web application at: http://localhost:8080/

Acces the admin section at: http://localhost:8080/admin

username : admin

password : password

The instructions above will let you run the application with default settings and configurations.
Please read the instructions on how to connect to MySQL, configure an email server and configure other subsystems


### Documentation:
-------------------

Documentation available from the wiki <http://shopizer-ecommerce.github.io/shopizer/#>

ChatOps <https://shopizer.slack.com>  - Join our Slack channel https://shopizer-slackin.herokuapp.com/

More information is available on shopizer web site here <http://www.shopizer.com>

### Participation:
-------------------

If you have interest in giving feedback or for participating to Shopizer project in any way
Feel to use the contact form <http://www.shopizer.com/contact.html> and share your email address
so we can send an invite to our Slack channel


