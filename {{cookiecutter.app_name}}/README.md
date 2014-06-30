# {{cookiecutter.app_name}}

{{cookiecutter.project_short_description}}

## Customizing

Congratulations, you've now started a beautiful new Go service.

- Add code to the agent in `command/agent/command.go`, this is where the long running service logic lives
- Add any status, action commands you need to `commands.go`

## Developing

The full set of management commands can be checked with `make help`. In particular:

### Building

Run ``make`` or ``make build``

### Testing

Run ``make test``
