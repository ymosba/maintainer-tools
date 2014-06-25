# OCA Maintainers Tools

## Installation

    $ git clone git@github.com:OCA/maintainers-tools.git
    $ cd maintainers-tools
    $ virtualenv env
    $ . env/bin/activate
    $ python setup.py install

## Usage

Get a token from Github, you may have to delete the existing one from Account settings -> Applications -> Personnal Access Token

    $ oca-github-login USERNAME

Copy the users from the maintainers team to the other teams

    $ oca-copy-maintainers

## Developers

As a developer, you want to launch the scripts without installing the
egg. 

    $ git clone git@github.com:OCA/maintainers-tools.git
    $ virtualenv env
    $ . env/bin/activate
    $ pip install -e maintainers-tools

Get a token from Github

    $ python -m tools.github_login USERNAME

Run a script

    $ python -m tools.copy_maintainers

You can use the `GITHUB_TOKEN` environment variable to specify the token

    $ GITHUB_TOKEN=xxx python -m tools.copy_maintainers