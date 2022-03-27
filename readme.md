
This is a Dockerfile to run php scripts with composer
# How to use this php dockerfile

```bash
cd <dir with Dockerfile>
docker build -t myimage .

cd <file_with_php_script>
```

#### CMD shell
```bash
docker run --name myapp -v %cd%:/usr/src/myapp -d myimage   
```
#### Powershell
```bash
docker run --name myapp -v ${pwd}:/usr/src/myapp -d myimage   
```
```bash
docker exec -it myapp bash

composer install
```