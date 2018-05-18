# composer
Docker container to run PHP Composer with SSH keys

The container will look for a directory called `ssh` in the root of the project if found it will copy
the `/opt/project/ssh/id_rsa` to `~/.ssh/id_rsa` and run composer passing any parameters.

# Usage

 * For PHP 7
   * BASH (Linux/OS X)    `docker run --rm -it -v $(pwd):/opt/project jstormes/composer install`
   * PowerShell (Windows) `docker run --rm -it -v ${pwd}:/opt/project jstormes/composer install`
   * CMD (Old Windows)    `docker run --rm -it -v %cd%:/opt/project jstormes/composer install`
