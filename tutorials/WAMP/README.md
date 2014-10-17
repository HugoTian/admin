# WAMP (Windows, Apache, MySQL, PHP)
### Installation:
http://www.wampserver.com/en/

### Step-by-step
##### 1. Start your MAMP
You should see something like this: 

<img src="https://github.com/EECS485-Fall2014/staff/blob/master/tutorials/WAMP/1.png" width="50%" height="50%">

The icon is green because Apache server has already started as you start this application.

##### 2. Change Document Root
Open up httpd.conf of WAMP, as shown in the screenshot.

<img src="https://github.com/EECS485-Fall2014/staff/blob/master/tutorials/WAMP/2.png" width="50%" height="50%">

Then search for `DocumentRoot` in the file, find the one with a path which by default should be "***/wamp/www/" and replace that with where your index.php is located. 

<img src="https://github.com/EECS485-Fall2014/staff/blob/master/tutorials/WAMP/3.png" width="50%" height="50%">

You can see I changed my DocumentRoot to `E:\wamp\pa1_q350d6haor\html`. When I set it up, my folder is like this:

<img src="https://github.com/EECS485-Fall2014/staff/blob/master/tutorials/WAMP/0.png" width="75%" height="75%">

##### 3. Enable rewrite module

<img src="https://github.com/EECS485-Fall2014/staff/blob/master/tutorials/WAMP/6.png" width="50%" height="50%">

Click the `rewrite_module` will enable it. WAMP should restart automatically (turn yellow, and wait for a while it will turn green again).

##### 4. Set up MySQL
We will need to set up database which is referenced in your PHP code. For example, I have code 

	$user="group11"; 
	$password="friedcode"; 
	$database="group11";
	$con = mysql_connect("127.0.0.1", $user, $password) or die('Could not connect: ' . mysql_error()); 


We need to set up the user and database here. Go to "PHPMyAdmin"

<img src="https://github.com/EECS485-Fall2014/staff/blob/master/tutorials/WAMP/7.png" width="50%" height="50%">

Under "Users" Tab, add a new user, fill in username which correspond to the one you used in your code, choose localhost, fill in password (again should match what is in your PHP code), ignore "generate password", check all checkboxs in "Database for user" and "Global privileges" and scroll down to the bottom of the page to click ok. Here is a screenshot for reference:

<img src="https://github.com/EECS485-Fall2014/staff/blob/master/tutorials/WAMP/10.png" width="50%" height="50%">

##### 5. Run it! 
So far you should have everything set up to run the code, use your browser to go to "localhost/secret/pa#". Screenshot:

<img src="https://github.com/EECS485-Fall2014/staff/blob/master/tutorials/WAMP/11.png" width="50%" height="50%">

### Trouble-shooting
Please read Apache -> Apache error/access log carefully.

### Miscellaneous
You can turn off PHP debug info by going to PHP->PHP settings.
<img src="https://github.com/EECS485-Fall2014/staff/blob/master/tutorials/WAMP/9.png" width="50%" height="50%">