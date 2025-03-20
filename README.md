# auto-gh-pages-deploy

This `deploy.yml` file allows for comfortable deployments to GitHub pages without the need to have a local clone of your repository.

Move this file to `./.github/workflows/deploy.yml`, and any changes to the `master` branch will be deployed.

This script uses Node `v.22` and tests for a production-ready build version before executing the `cypress tests` of the repository.

If you have no Cypress e2e tests, feel free to remove the `Run Cypress Tests` and `Upload Cypress Artifacts` entries.

If all steps execute flawlessly, the `github-actions[bot]` will deploy the latest version to GitHub pages.

❗ If the `master` branch is protected, replace the `secrets.GITHUB_TOKEN` with a freshly generated Personal Access Token (in your repository secrets), which could be named `DEPLOY_TOKEN`, and swap it for `secrets.DEPLOY_TOKEN` in the `deploy.yml` file.
