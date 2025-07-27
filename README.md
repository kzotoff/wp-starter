1. copy folders `mysql`, `nginx`, `php`, and `wp` along the `docker-compose.yml` into a new folder

2. unzip wordpress zip into wp folder

3. make wp folder writable to all:
```
chmod -R a+w wp
```

4. start:
```
docker compose up
```
5. proceed to `localhost:8080`

6. perform wordpress installation using the following parameters:
	- database name: wordpress
	- username: wordpress
	- password: wordpress
	- database host: mysql

7. add this row to newly created `wp-config.php`:
```
define('FS_METHOD', 'direct');
```
There is a special place for user-defined things at the end of the file
