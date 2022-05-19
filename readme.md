
This is a Dockerfile to run php scripts with composer
# How to use this php dockerfile

```bash
cd <dir with Dockerfile from this repo>
docker build -t phprunner .

cd <file_with_php_script>
```

#### CMD shell
```bash
docker run --name myapp -v %cd%:/usr/src/myapp -d phprunner   
```
#### Powershell
```bash
docker run --name myapp -v ${pwd}:/usr/src/myapp -d phprunner   
```

#### Bash
```bash
docker run --name myapp -v $PWD:/usr/src/myapp -d phprunner   
```

Once the php code is running in the `myapp` container you are able to run by entering the shell, as follows:

```bash
docker exec -it myapp bash
composer install
php <path-to-php-file>
```

You are also able to edit the code using Visual Studio Code with the [Remote Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
