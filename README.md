# cookiecutter-go-service

A Go service template for [cookiecutter](https://github.com/audreyr/cookiecutter), adapted from Mark Wolfe's [go-bootstrap](https://github.com/wolfeidau/go-bootstrap). Use it to make a new project with the recommended layout and tooling all built-in from scratch.

## Use it now

If you don't have `cookiecutter` installed, you'll need to install that first using Python's pip command:

```console
$ pip install cookiecutter
$ cookiecutter https://github.com/larsyencken/cookiecutter-go-service.git
```

You will be asked about your basic info (name, project name, app name, etc.). This info will be used to customize your new project.

Run `make help` to see the available management commands, or just run `make` to build your project.

## Features

- Generous `Makefile` with management commands
- Works with either in a global `GOPATH` or with a local vendor directory
- Uses [gogpm](https://github.com/mtibben/gogpm) for dependency management
- Comes with an example command-line binary and example agent
- Sensible default contribution guidelines for open source projects

## License

BSD licensed.

## Changelog

### devel

- Initial pass at importing `go-bootstrap`
- Use `gogpm`, installing it on demand
- Makefile supporting either global or local GOPATH
