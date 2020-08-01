# NUnit Documentation

This repository serves the content that is found at <http://docs.nunit.org>.

![NUnit Documentation Build Process](https://github.com/nunit/docs/workflows/NUnit%20Documentation%20Build%20Process/badge.svg)

## What is the Docs site? How does it work?

The docs site is a project within the NUnit organization. [Read the vision at VISION.md](VISION.md) to understand more about how the documentation fits into the overall organization and how it supports the other projects.

## How to Build these docs locally

* Prerequisite: Install [docfx](https://dotnet.github.io/docfx/) (using [Chocolatey](https://chocolatey.org/)? The command is `choco install docfx -y`)
* Pull this repository
* `cd docs`
* Run `docfx build`
* Run `docfx serve` and navigate to <http://localhost:8080/_site>

## Linting Locally

* Install `markdownlint`: `npm install markdownlint-cli -g`
* Open the root of the project (`/`, not `/docs`)
* Run `markdownlint docs/**/*.md`

We'd love your contributions! See [The contributing guide](CONTRIBUTING.md) for how to get involved.

## How the Docs are Built and Deployed

* We build the docs via the GitHub actions located in `./github/workflows`.
* The workflow uses a container with docfx installed; the container builds the docs.
* The workflow then uses another container to push the results to the `gh-pages` branch, using a personal access token that is stored in the repository's settings.
* GitHub serves the outputted site from the `gh-pages` branch, and the DNS of `docs.nunit.org` points there.
