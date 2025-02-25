# cookiecutter-ampel

[cookiecutter](https://cookiecutter.readthedocs.io/en/stable/README.html) template for Ampel plugins that sets up basic directory structure, linting, type checking, and CI.

## Usage

Best used with [cruft](https://cruft.github.io/cruft/).

- [Install cruft](https://cruft.github.io/cruft/#installation)
- Create a project with `cruft create https://github.com/AmpelAstro/cookiecutter-ampel` and fill out variables, e.g.:
```
  [1/6] project_name (SomeTelescope): LS4
  [2/6] github_org_or_username (AmpelAstro): 
  [3/6] description (LS4 support for the Ampel system): 
  [4/6] author_full_name (Alexandra Stronomer): 
  [5/6] author_email (a.stronomer@mail.to): 
  [6/6] version (0.10.0a0): 
```

Then, fill out and push your project:

```
cd Ampel-LS4
poetry lock
git init .
git add .; git commit -m 'initial commit'
git remote add origin git@github.com:AmpelAstro/Ampel-LS4.git
git push -u origin main
```

## Synchronizing generated projects

This template provisions a workflow that synchronizes the generated repository with the current state of the template, and files a PR with those changes. If the action fails with the error message "GitHub Actions is not permitted to create or approve pull requests", you must (allow GitHub Actions to create and approve pull requests)[https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/managing-github-actions-settings-for-a-repository#preventing-github-actions-from-creating-or-approving-pull-requests], both on the organization, and, if applicable, on the repository level.