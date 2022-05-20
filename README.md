# NGINX REGEX TESTER FOR REWRITE RULES

This source code run an application on the browser to test regex patterns that may be useful for rewrite rules, building a docker conteiner with Nginx.

You don't need previous docker knowledge to use this application, but you need to install docker and docker compose on your machine.

This only runs in Linux OS.

### Setup

Before start the compose, check what ports are already in use, run the command below:

```
sudo lsof -i -P -n | grep LISTEN
```

After check the ports in use, if the port 30 is in use, edit the `docker-compose.yaml` file.

Change the value on left side of the colon `30:80` to other avaliable port, eg 40 -> `40:80`.

### Starting the Application

Open the terminal and go to the path where is this source code and run the command `docker compose --verbose up` depending on the docker compose package, can be `docker-compose --verbose up`. 

The `--verbose` option is usefull to check if any point of the application start appears any error.

If in the first run the application run without error, you could start the application with this command `docker compose up -d`, again, depending on the docker compose package the commando will be docker-compose up -d`.

### Accessing the Regex Tester

To access the application, open your browser and enter in this address: `http://localhost:30/regextester.php` if you change the port on the setup step, change the port in the application address. 

### Regex Patterns

To be included...

#### References
 * https://www.nginx.com/blog/regular-expression-tester-nginx/
 * https://nginx.org/en/docs/http/ngx_http_rewrite_module.html
 * https://www.thegeekstuff.com/2017/08/nginx-rewrite-examples/
 * https://linuxhint.com/url_rewriting/
 
 #### Feel free to contribute with this repo.
