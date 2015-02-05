# wordpress


## set up

### 1.download
git clone git@github.com:high5/wordpress.git

### 2.database
Database name is optional.

```
mysql>CREATE DATABASE wordpress_1 CHARACTER SET utf8;
```

```
mysql>CREATE USER wordpressuser@localhost;
```

```
mysql>SET PASSWORD FOR wordpressuser@localhost= PASSWORD("password");
```


```
mysql>GRANT ALL PRIVILEGES ON wordpress_1.* TO wordpressuser@localhost IDENTIFIED BY 'password';
```

```
mysql>FLUSH PRIVILEGES;
```


### 3.edit config
```
$ cp wp-config-sample.php wp-config.php
```

```
// ** MySQL settings - You can get this info from your web host ** //
/** The name of the database for WordPress */
define('DB_NAME', 'wordpress_1');

/** MySQL database username */
define('DB_USER', 'wordpressuser');

/** MySQL database password */
define('DB_PASSWORD', 'password');

```
