# GitHub Actions Workflow Analysis

## 1. What triggers this workflow to run?

The workflow runs when code is pushed to the `main` branch or when a pull request targets the `main` branch.

## 2. What are the four main steps?

The four main steps are:

1. Checkout code
2. Validate HTML
3. Check links
4. Upload artifact

## 3. What does the Checkout code step do?

The Checkout code step copies the repository files into the GitHub Actions runner. This step is necessary because the later steps need access to the website files to validate the HTML, check links, and prepare the site for deployment.

## 4. What is the purpose of the environment configuration?

The environment configuration connects the deployment job to the `github-pages` environment. It also records the website URL and allows GitHub to use the correct deployment permissions and protections.

## 5. How does automated deployment improve reliability?

Automated deployment performs the same validation and link checks every time the workflow runs. The website is deployed only after the required checks pass, which reduces mistakes and makes deployment more consistent than doing everything manually.

## 6. What happens if code is pushed to another branch?

Pushing code to a branch other than `main` will not trigger the workflow through a push. The changes must be included in a pull request targeting `main` or merged into `main` before the workflow runs.
