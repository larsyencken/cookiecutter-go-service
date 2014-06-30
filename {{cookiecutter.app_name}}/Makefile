#
#  Makefile
#
#  The kickoff point for all project management commands.
#

# Program version
VERSION := $(shell grep "const Version " version.go | sed -E 's/.*"(.+)"$$/\1/')

# Binary name for bintray
BIN_NAME={{cookiecutter.app_name}}

# Project owner for bintray
OWNER={{cookiecutter.github_username}}

# Project name for bintray
PROJECT_NAME={{cookiecutter.app_name}}

# Project url used for builds
# examples: github.com, bitbucket.org
REPO_HOST_URL=github.com

# Grab the current commit
GIT_COMMIT="$(shell git rev-parse HEAD)"

# Check if there are uncommited changes
GIT_DIRTY="$(shell test -n "`git status --porcelain`" && echo "+CHANGES" || true)"

# Add the godep path to the GOPATH
GOPATH=$(shell godep path):$(shell echo $$GOPATH)

default: build

help:
	@echo 'Management commands for {{cookiecutter.app_name}}:'
	@echo
	@echo 'Usage:'
	@echo '    make build    Compile the project.'
	@echo '    make test     Run tests on a compiled project.'
	@echo '    make clean    Clean the directory tree.'
	@echo

build: .git
	@echo "building ${OWNER} ${BIN_NAME} ${VERSION}"
	@echo "GOPATH=${GOPATH}"
	gogpm install && \
	go build -ldflags "-X main.GitCommit ${GIT_COMMIT}${GIT_DIRTY}" -o bin/${BIN_NAME}

clean:
	@test ! -e bin/${BIN_NAME} || rm bin/${BIN_NAME}

.git:
	git init
	git add -A .
	git commit -m 'Initial scaffolding.'

test:
	go test ./...

.PHONY: build dist clean test help default
