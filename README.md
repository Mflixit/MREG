iredmail
allow iframe
SSL....generate and install certs
auto-Login php
SMTP
create user script



2 computers 1 domain 2 subdomains 2 certs....but different ones, does that matter? it should if we are exploting subdomain readablity of cookies for session data?

smtp might be  inscure but we can use it on internal network only, firewall external




generate and save key, convert with puttygen
cloud launch
attach IP
registar- set IP in DNS table


login ssh via web interface
run following command to get wp login credentials

sudo cat /opt/bitnami/var/data/bitnami_credentials/credentials


also get rid of banner logo with the following command


Generate And Install A Let's Encrypt SSL Certificate For A Bitnami Application
A little outdated, but you can figure it out.

enable multisite

create new profle in notepadd++ (after manually installing the ftp plugin)
 edit /opt/btnami/apps/wordpress/htdocs/wp-config.php and add the following piece of code at the top of the file, just below the <?php header:

define('WP_ALLOW_MULTISITE', true);





# MREG
Backups and How Tos for MREG sites


# For plaintext passwords
* @param WP_User|WP_Error $user   WP_User object if the login and reset key match. WP_Error object otherwise
*/
	do_action( 'validate_password_reset', $errors, $user );
#FIRES ON RESET PAGE LOAD -MORGAN
		"if ( ( ! $errors->get_error_code() ) && isset( $_POST['pass1'] ) && !empty( $_POST['pass1'] ) ) {
		reset_password($user, $_POST['pass1']);"
#FIRES AFTER NEW PASSWORD RESET ACEPTED -MORGAN
#BEGINING OF MY CODE -MORGAN
		$my_file = 'C:\Bitnami\wordpress-4.9.1-0\apps\wordpress\htdocs\wp-content\plugins\text.txt';	
		$handle = fopen($my_file, a') or die('Cannot open file:  '.$my_file);	
		$myvariable1 = "Hello World1";
		$myvariable2 = "Hello World2";
		$myvariable3 = "$myvariable1, $myvariable2";
		$myvariable4 = $_POST['pass1'];
		fwrite($handle, "$myvariable4");
#END OF MY CODE -MORGAN


# For emby user create 
. c:\embyusers\EmbyLib.ps1
Create-EmbyUser -username $args[0] | Out-Null
Set-EmbyUserPassword -username $args[0] -newPassword $args[1] | Out-Null
$args[0] >> 'c:\embyusers\file9.txt'
#$args[1] >> 'c:\embyusers\file9.txt'

# For iredmail
Open ports at cloud level
25 110 465 143...
# bitnami wordpress multisite



# For subdomains on wordpress
Edit /opt/bitnami/acpache/conf/bitnami/bitnami.conf

<VirtualHost _default_:80>
  DocumentRoot "/opt/bitnami/apps/wordpress/htdocs/kexow"
  ServerName kexow.kexow.com
      <Directory "/opt/bitnami/apps/wordpress/htdocs/kexow">
        Options Includes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>

# For to remove x frame same origin 
// X-Frame-Options HTTP header value sent to prevent from Clickjacking.
// Possible values: sameorigin|deny|allow-from <uri>.
// Set to false in order to disable sending the header.
$config['x_frame_options'] = false;
