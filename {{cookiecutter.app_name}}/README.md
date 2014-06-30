# {{cookiecutter.app_name}}

{{cookiecutter.project_short_description}}

## Getting started

This project requires Go to be installed. On OS X with Homebrew you can just run `brew install go`.

Running it then should be as simple as:

```console
$ make
$ ./bin/{{cookiecutter.app_name}}
```

Add your long-running agent logic to `command/agent/command.go`, and any status or action commands you need to `commands.go`.

### Testing

``make test``

## License

_Fill me in._

## Contributing

See `CONTRIBUTING.md` for more details.
