# CodeIgniter-JWT-Sample

Simple Codeigniter, REST Server, JWT implementation.

**Update**

As per multiple requests, I am adding logic for timeout.  
Please check ```application\controllers\Authtimeout.php``` for more details.

**Note:** I did not add logic for expired token replacement after timeout.


Setup
=====

Set up project on php server (XAMPP/Linux). 

* **.htaccess** file at project root

    This project contains .htaccess file for windows machine. Please update this file as per your requirements.  
[Sample htaccess code (Win/Linux)] (http://stackoverflow.com/questions/28525870/removing-index-php-from-url-in-codeigniter-on-mandriva)  
* `encryption_key` in `application\config\config.php`  
[Encryption key generator] (http://jeffreybarke.net/tools/codeigniter-encryption-key-generator/)  
```
$config['encryption_key'] = '';
```  

* `jwt_key` in `application\config\jwt.php`

```
$config['jwt_key']	= '';
```

* **For Timeout** `token_timeout` in `application\config\jwt.php`

```
$config['token_timeout']	= ;
```

Run
=====

GET auth token

    URL: http://host/CodeIgniter-JWT-Sample/auth/token
    Method: GET

Check decoded token

    URL: http://host/CodeIgniter-JWT-Sample/auth/token
    Method: POST
    Header Key: Authorization
    Value: Auth token generated in GET call
    
GET auth token with **timeout**

    URL: http://host/CodeIgniter-JWT-Sample/authtimeout/token
    Method: GET

Check decoded token with **timeout**

    URL: http://host/CodeIgniter-JWT-Sample/authtimeout/token
    Method: POST
    Header Key: Authorization
    Value: Auth token generated in GET call of authtimeout controller

Project uses 
=======
[CodeIgniter] (https://www.codeigniter.com/)  
[REST Server] (https://github.com/chriskacerguis/codeigniter-restserver)  
[Reference for JWT implementation] (https://github.com/rmcdaniel/angular-codeigniter-seed)

Contact
=====
For any questions mail me paritoshvaidya@gmail.com
  
  
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://github.com/ParitoshVaidya/CodeIgniter-JWT-Sample/blob/master/license.txt)
