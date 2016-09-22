# Docker ERPNext (Multi-container)

This code was originally forked from [donysukardi/docker-frappe](https://github.com/donysukardi/docker-frappe).

Follow the steps below to run your own local installation of ERPNext.

## Start a local version of ERPNext

1. First we need to bootstrap the installation: `docker-compose run app`.
1. When asked to reset the database press `y` and enter.
1. After this process completes you will need to exit the container (for example: `ctrl+c`). The process completes after you see messages stating: `Booting worker with pid`...
1. Start the containers: `docker-compose up -d`.
1. Watch the container logs: `docker-compose logs -f`.

You should be able to log in to the server at `http://localhost`. The username is `Administrator` and the password is `frappe`. Follow the prompts to complete the initial setup.
