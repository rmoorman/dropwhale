# dropwhale
A Drop-in Docker environment for Drupal module testing

## Purpose

Dropwhale is a drop-in Docker environment aimed at Drupal module 
developers. Instead of maintaining a separate Drupal installation, 
Dropwhale does all the downloading and initialization of Drupal with a 
few easy commands. No need for you to download and install core. No 
need to argue with xdebug or get Drush installed. It's all built in!

## Use

Download Dropwhale and copy the .docker directory to the root of your
module repository. You can choose to commit the directory to your module
repository, or gitignore it. Dropwhale doesn't care.

Copy the .docker/docker-compose-override.yml.dist file to 
.docker/docker-compose-override.yml (no 'dist'). 

Edit the .docker/docker-compose-override.yml file, adding the
installation directory of your module, and adding your module name to 
the MODULE_ENABLE environment variable.

cd to the root of your module repository. Execute .docker/start.sh

If you need to rebuild Drupal at any time, execute .docker/build.sh

## License

Dropwhale is licensed under the GPLv3. 
