# Docker ERPNext (Multi-container)

This code was originally forked from [donysukardi/docker-frappe](https://github.com/donysukardi/docker-frappe).

Follow the steps below to run your own local installation of [ERPNext](https://github.com/frappe/erpnext).

*NOTE: Please do not consider this "production ready".*

## Deprecation Notice

This project is no longer maintained.

## Start a local version of ERPNext

1. First we need to bootstrap the installation: `docker-compose run app`.
1. When asked to reset the database press `y` and enter.
1. After this process completes you will need to exit the container (for example: `ctrl+c`). The process completes after you see messages stating: `Booting worker with pid`...
1. Start the containers: `docker-compose up -d`.
1. Watch the container logs: `docker-compose logs -f`.

You should be able to log in to the server at `http://localhost`. The username is `Administrator` and the password is `frappe`. Follow the prompts to complete the initial setup.

## Notes

1. This [Docker](https://www.docker.com/) image is based on the [ianneub/frappe](https://hub.docker.com/r/ianneub/frappe/) image.

## Environment Variables

The image is configuring using environment variables. Bellow is a list of variables and their default settings. These variables will be set in the `site_config.json` file.

* `ADMIN_PASSWORD`=`frappe`
* `DB_HOST`=`db`
* `DB_NAME`=`frappe`
* `DB_PASSWORD`=`frappe`
* `DB_USER`=`frappe`
* `MAIL_LOGIN`=``
* `MAIL_PASSWORD`=``
* `MAIL_PORT`=``
* `MAIL_SERVER`=``
* `REDIS_CACHE_URL`=`redis-cache`
* `REDIS_QUEUE_URL`=`redis-queue`
* `REDIS_SOCKETIO_URL`=`redis-socketio`
* `ROOT_PASSWORD`=`root`
* `USE_SSL`=`false`
* `DEVELOPER_MODE`=`false`
