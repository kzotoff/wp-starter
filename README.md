# Very simple starterpack to run dockerized Wordpress in a minute


1. Copy folders `mysql`, `nginx`, `php`, and `wp` along the `docker-compose.yml` into a new folder

2. Unzip wordpress zip into wp folder. Existing `.gitkeep` can be removed.

3. Make wp folder writable to all:
```
chmod -R a+w wp
```

4. Start:
```
docker compose up
```
5. Proceed to `localhost:8080`

6. Perform wordpress installation using the following parameters:
	- database name: wordpress
	- username: wordpress
	- password: wordpress
	- database host: mysql

7. Add this row to newly created `wp-config.php`:
```
define('FS_METHOD', 'direct');
```
There is a special place for user-defined things at the end of the file.
