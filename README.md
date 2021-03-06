# Nginx Virtual Host Creator (Magento 1, Magento 2, Laravel, WordPress)

This Script creates Nginx virtual host for different applications.  
Some of the supported applications are:  
 - Magento 1
 - Magento 2
 - WordPress
 - Laravel
 - Html
 - ~~Others~~


## INSTALL
To install, simply download the script file and give it the executable permission.
```
curl -0 https://raw.githubusercontent.com/MagePsycho/nginx-virtual-host-bash-script/master/src/vhost-nginx.sh -o vhost-nginx.sh
chmod +x vhost-nginx.sh
```

To make it system wide command
```
sudo mv vhost-nginx.sh /usr/local/bin/vhost-nginx
```
OR  
(may not work with `sudo`)
```
mv vhost-nginx.sh ~/bin/vhost-nginx
```
Make sure your `$HOME/bin` folder is in executable path

## USAGE
### To display help
```
sudo ./vhost-nginx.sh --help
```
### To Create Virtual Host for Magento 1
```
sudo ./vhost-nginx.sh --domain=magento1938.test --app=magento1 --root-dir=/var/www/magento1/magento1938
```

### To Create Virtual Host for Magento 2
```
sudo ./vhost-nginx.sh --domain=magento223ce.test --app=magento2 --root-dir=/var/www/magento2/magento223ce
```

### To Create Virtual Host for WordPress
```
sudo ./vhost-nginx.sh --domain=wordpress494.test --app=wordpress --root-dir=/var/www/wordpress/wordpress494
```

### To Create Virtual Host for Laravel
```
sudo ./vhost-nginx.sh --domain=laravel560.test --app=laravel --root-dir=/var/www/laravel/laravel560
```

### To Create Virtual Host for Default (Html)
```
sudo ./vhost-nginx.sh --domain=website.test --app=laravel --root-dir=/var/www/html/website
```

**Notes**
 - In case of system-wide command, you can omit the `--root-dir` parameter if you run the command from the root directory of application. 

## Screenshots
![Nginx Virtual Host Creator Help](https://github.com/MagePsycho/nginx-virtual-host-bash-script/raw/master/docs/nginx-virtual-host-bash-script-help.png "Nginx Virtual Host Creator Help")
Screentshot - Nginx Virtual Host Creator Help

![Nginx Virtual Host Creator Result](https://github.com/MagePsycho/nginx-virtual-host-bash-script/raw/master/docs/nginx-virtual-host-bash-script-result.png "Nginx Virtual Host Creator Result")
Screentshot - Nginx Virtual Host Creator Result

## RoadMap
 - [ ] To Support multiple applications:
    - [x] Magento 1
    - [x] Magento 2
    - [x] WordPress
    - [x] Laravel    
    - [x] Html    
    - [ ] OroCrm    
    - [ ] OroCommerce    
    - etc.
 - [ ] Flexible settings for Nginx 
    - fastcgi_pass: tcp port (127.0.0.1:9000) or unix socket (/var/run/php-fpm.sock)
 - [ ] Option to configure virtual host template from separate file.
 - [ ] Option to add SSL configuration
