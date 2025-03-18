# Demo for Multi-Site projects with AEM Edge Delivery Services
This is a demo project to illustrate a way to achieve multi-site and multi-brand sites with AEM Edge Delivery Services.

This solution is based on multiple GitHub Repositories:
- One main Git repository, this is the only repository that is actively used: https://github.com/techdivision/eds-multisite-demo-main
- Multiple child repositories that are synced to by the main repository. They are not intended to be interacted with by developers.
  - https://github.com/techdivision/eds-multisite-demo-brand-red
  - https://github.com/techdivision/eds-multisite-demo-brand-blue

The goal of this approach is to have one single shared codebase for multiple sites. This solution has the following advantages
- All features and implementations are shared across sites
- One unified and centralized way to develop all sites
- Possibility for overrides and customizations for the sites as required (read more below)

## Getting Started
- Clone this repository, **or**:
- Copy the Sync Job `.github/workflows/sync.yaml` into your repository and adapt it to your needs
- Copy the `.multisite` folder into your project
- Adapt the `.mutlisite/config.yaml` to your needs

## Authentication within GitHub
As you can see in the `.github/workflows/sync.yaml` we use an GitHub App for authentication within GitHub (from the main repo to the other repos). Read https://github.com/actions/create-github-app-token for more information.
You can use any preferred method you want to authenticate the GitHub Job against the other repositories. Adapt the Job accordingly.

## Environments
- Brand Red: https://main--eds-multisite-demo-brand-red--techdivision.aem.page/
- Brand Blue: https://main--eds-multisite-demo-brand-blue--techdivision.aem.page/

## Configuration
You need to register new sites in the `.multisite/config.yaml`

## Overrides
To override specific files for a specific child repository, you can add the file in the `.multisite` directory. See `.multisite/brand-blue/styles/theme.css` for an example.
