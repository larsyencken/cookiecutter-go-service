# cookiecutter-go-service

A Go service template for [cookiecutter](https://github.com/audreyr/cookiecutter), based on Mark Wolfe's [go-bootstrap](https://github.com/wolfeidau/go-bootstrap).

## Use it now

If you don't have `cookiecutter` installed, you'll need to install that first using Python's pip command:

```console
$ pip install cookiecutter
$ cookiecutter https://github.com/larsyencken/cookiecutter-go-service.git
```

You will be asked about your basic info (name, project name, app name, etc.). This info will be used in your new project. Once you've answered these, you'll need to make an initial Git commit to make things work:

```console
$ cd mygolangservice
$ git init
$ git add -A .
$ git commit -m 'Initial scaffolding.'
```

Now you're ready! Run `make help` to see what commands are available for the project.

## Features

_TO DO_

## License

BSD licensed.

## Changelog

### devel

- Initial pass at importing `go-bootstrap`
