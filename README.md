# Example app for GitHub Releases workshop

A basic web app built with Angular and deployed as SPA with Firebase Hosting. Serves to demonstrate using **multiple environments** and **triggering production deployment via GitHub Release**.

## Environments

Environments are defined in repository settings, secrets are defined separately per environment.

- [**production** environment](./.github/workflows/production.yml) is triggered by `v*` tag pushed by creating GitHub Release
- [**staging** environment](./.github/workflows/staging.yml) is automatically deployed on every push to `main` branch (e.g. after PR merge)
- [**preview** environments](./.github/workflows/preview.yml) are deployed individually for every PR (a comment is posted with a URL which is unique to the branch)

## Release instructions

In GitHub UI, [create a new release](https://github.com/flowup/releases-example-app/releases/new). Create a new tag in the format `vX.Y` (increment that last released version by 1). Generate release notes, select as latest release and publish. This will trigger a [deployment to production](https://github.com/flowup/releases-example-app/actions/workflows/production.yml).

## Links

- [Actions](https://github.com/flowup/releases-example-app/actions)
- [Releases](https://github.com/flowup/releases-example-app/releases)
- [Deployments](https://github.com/flowup/releases-example-app/deployments)
