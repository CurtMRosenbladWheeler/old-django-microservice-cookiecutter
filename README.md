# Django Microservice Cookiecutter

[![CI](https://github.com/CurtMRosenbladWheeler/django-microservice-cookiecutter/actions/workflows/ci.yml/badge.svg)](https://github.com/CurtMRosenblad/django-saas-template/actions/workflows/ci.yml) [![Black code style](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/ambv/black)

Powered by [Cookiecutter](https://github.com/CurtMRosenbladWheeler/django-microservice-cookiecutter), Cookiecutter Django is a framework for jumpstarting
production-ready Django projects quickly.

- Documentation: <https://cookiecutter-django.readthedocs.io/en/latest/>
- See [Troubleshooting](https://cookiecutter-django.readthedocs.io/en/latest/troubleshooting.html) for common errors and obstacles
- If you have problems with Cookiecutter Django, please open [issues](https://github.com/CurtMRosenbladWheeler/django-microservice-cookiecutter/issues/new) don't send
  emails to the maintainers.

## Features

Here's the edited list of features that includes the specified additions for a Django 4.2-based microservice template:

- For Django 4.2
- Works with Python 3.12
- Renders Django projects with 100% starting test coverage
- Tailwind CSS v3
- [12-Factor](https://12factor.net) based settings via [django-environ](https://github.com/joke2k/django-environ)
- Secures with SSL by default.
- Optimized development and production settings
- Microservice templates
- Comes with enterprise-level authentication microservice
- Optional basic ASGI setup for Websockets
- Optional custom static build using Gulp or Webpack
- Send emails via [Anymail](https://github.com/anymail/django-anymail) (using [Mailgun](http://www.mailgun.com/) by default or Amazon SES if AWS is selected as the cloud provider, but switchable)
- Media storage using Amazon S3, Google Cloud Storage, Azure Storage, or nginx
- Docker support using [docker-compose](https://github.com/docker/compose) for development and production (using [Traefik](https://traefik.io/) with [LetsEncrypt](https://letsencrypt.org/) support)
- [Procfile](https://devcenter.heroku.com/articles/procfile) for deploying to Heroku
- Instructions for deploying to [PythonAnywhere](https://www.pythonanywhere.com/)
- Run tests with unit test or pytest
- Customizable databases (PostgreSQL, MySQL, Redis, MongoDB, and Cassandra)
- Works with cloud databases on AWS, GCP, and Azure
- Designed to work with AWS, GCP, Azure services, and non-cloud systems. 
- Default integration with [pre-commit](https://github.com/pre-commit/pre-commit) for identifying simple issues before submission to code review

## Optional Integrations

_These features can be enabled during initial project setup._

- Serve static files from Amazon S3, Google Cloud Storage, Azure Storage or [Whitenoise](https://whitenoise.readthedocs.io/)
- Configuration for [Celery](https://docs.celeryq.dev) and [Flower](https://github.com/mher/flower) (the latter in Docker setup only)
- Integration with [Mailpit](https://github.com/axllent/mailpit/) for local email testing
- Integration with [Sentry](https://sentry.io/welcome/) for error logging

## Constraints

- Only maintained 3rd party libraries are used.
- Environment variables for configuration (This won't work with Apache/mod_wsgi).

---

### PyUp

PyUp brings you automated security and dependency updates used by Google and other organizations. Free for open-source projects!

## Usage

Let's pretend you want to create a Django project called "myproject". Rather than using `startproject`
and then editing the results to include your name, email, and various configuration issues that always get forgotten until the worst possible moment, get [cookiecutter](https://github.com/CurtMRosenbladWheeler/django-microservice-cookiecutter](https://github.com/CurtMRosenbladWheeler/django-microservice-cookiecutter) to do all the work.

First, get Cookiecutter. Trust me, it's awesome:

    $ pip install "cookiecutter>=1.7.0"

Now run it against this repo:

    $ cookiecutter https://github.com/CurtMRosenbladWheeler/django-microservice-cookiecutter

You'll be prompted for some values. Provide them, then a Django project will be created for you.

**Warning**: After this point, change 'Mathias Rosenblad', 'CurtMRosenbladWheeler', etc to your own information.

Answer the prompts with your own desired options. For example:

    Cloning into 'cookiecutter-django'...
    remote: Counting objects: 550, done.
    remote: Compressing objects: 100% (310/310), done.
    remote: Total 550 (delta 283), reused 479 (delta 222)
    Receiving objects: 100% (550/550), 127.66 KiB | 58 KiB/s, done.
    Resolving deltas: 100% (283/283), done.
    project_name [My Project]: My Project
    project_slug [my_project]: my_project
    description [Behold My Awesome Project!]: A project.
    author_name [Mathias Rosenblad]: Mathias Rosenblad
    domain_name [example.com]: example.com
    email [mathias-rosenblad@example.com]: CurtMRosenbladWheeler@gmail.com
    version [0.1.0]: 0.0.1
    Select open_source_license:
    1 - MIT
    2 - BSD
    3 - GPLv3
    4 - Apache Software License 2.0
    5 - Not open source
    Choose from 1, 2, 3, 4, 5 [1]: 1
    Select username_type:
    1 - username
    2 - email
    Choose from 1, 2 [1]: 1
    timezone [UTC]: America/New_York
    windows [n]: n
    Select an editor to use. The choices are:
    1 - None
    2 - PyCharm
    3 - VS Code
    Choose from 1, 2, 3 [1]: 1
    use_docker [n]: n
    Select postgresql_version:
    1 - 15
    2 - 14
    3 - 13
    4 - 12
    5 - 11
    6 - 10
    Choose from 1, 2, 3, 4, 5 [1]: 1
    Select cloud_provider:
    1 - AWS
    2 - GCP
    3 - None
    Choose from 1, 2, 3 [1]: 1
    Select mail_service:
    1 - Mailgun
    2 - Amazon SES
    3 - Mailjet
    4 - Mandrill
    5 - Postmark
    6 - Sendgrid
    7 - SendinBlue
    8 - SparkPost
    9 - Other SMTP
    Choose from 1, 2, 3, 4, 5, 6, 7, 8, 9 [1]: 1
    use_async [n]: n
    use_drf [n]: y
    Select frontend_pipeline:
    1 - None
    2 - Django Compressor
    3 - Gulp
    4 - Webpack
    Choose from 1, 2, 3, 4 [1]: 1
    use_celery [n]: y
    use_mailpit [n]: n
    use_sentry [n]: y
    use_whitenoise [n]: n
    use_heroku [n]: y
    Select ci_tool:
    1 - None
    2 - Travis
    3 - Gitlab
    4 - Github
    Choose from 1, 2, 3, 4 [1]: 4
    keep_local_envs_in_vcs [y]: y
    debug [n]: n

Enter the project and take a look around:

    $ cd my_project/
    $ ls

Create a git repo and push it there:

    $ git init
    $ git add .
    $ git commit -m "Initial commit."
    $ git remote add origin git@github.com:CurtMRosenbladWheeler/myproject.git
    $ git push -u origin master

Now take a look at your repo. Don't forget to carefully look at the generated README. Awesome, right?

## Community

- If you think you found a bug or want to request a feature, please open an [issue](https://github.com/CurtMRosenbladWheeler/django-microservice-cookiecutter/issues).
- For anything else, you can chat with us on [Discord](https://github.com/CurtMRosenbladWheeler/django-microservice-cookiecutter/discussions).

## For PyUp Users

If you are using [PyUp](https://pyup.io) to keep your dependencies updated and secure, use the code _cookiecutter_ during checkout to get 15% off every month.

## "Your Stuff"

Scattered throughout the Python and HTML of this project are places marked with "your stuff". This is where third-party libraries are to be integrated with your project.

## Releases

Need a stable release? You can find them at <https://github.com/CurtMRosenbladWheeler/django-microservice-cookiecutter/releases>

## Have Ideas?

We are open to any ideas on how to make our cookiecutter better. Create a [discussion](https://github.com/CurtMRosenbladWheeler/django-microservice-cookiecutter/discussions) post to submit your idea.

### Fork This

If you have differences in your preferred setup, I encourage you to fork this to create your own version.
Once you have your fork working, let me know and I'll add it to a '_Similar Cookiecutter Templates_' list here.
It's up to you whether to rename your fork.

If you do rename your fork, I encourage you to submit it to the following places:

- [cookiecutter](https://github.com/CurtMRosenbladWheeler/django-microservice-cookiecutter) so it gets listed in the README as a template.
- The cookiecutter [grid](https://www.djangopackages.com/grids/g/cookiecutters/) on Django Packages.

### Submit a Pull Request

We accept pull requests if they're small, atomic, and make our own project development
experience better.
