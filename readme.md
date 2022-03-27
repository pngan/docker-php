
This is a Dockerfile to run php scripts with composer
# How to use this php dockerfile

cd <dir with Dockerfile>
docker build -t myimage .

cd <file_with_php_script>


#### CMD shell
docker run --name myapp -v %cd%:/usr/src/myapp -d myimage   

#### Powershell
docker run --name myapp -v ${pwd}:/usr/src/myapp -d myimage   

docker exec -it myapp bash

composer install
