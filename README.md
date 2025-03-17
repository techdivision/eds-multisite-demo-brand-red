# Demo for Multi-Site projects with AEM Edge Delivery Services
This is a demo project to illustrate a way to achieve multi-site and multi-brand sites with AEM Edge Delivery Services.

This solution is based on multiple GitHub Repositories:
- One main Git repository, this is the only repository that is actively used: https://github.com/techdivision/eds-multisite-demo-main
- Multiple child repositories that are synced to by the main repository. They are not intended to be interacted with by developers.
  - TBD
  - TBD

The goal of this approach is to have one single shared codebase for multiple sites. This solution has the following advantages
- All features and implementations are shared across sites
- One unified and centralized way to develop all sites
- Possibility for overrides and customizations for the sites as required (read more below)

## Getting Started
- Copy the Sync Job `.github/workflows/sync.yaml` into your repository and adapt it to your needs
- Copy the `.multisite` folder into your project
- Adapt the `.mutlisite/config.yaml` to your needs

## Environments
- Preview: https://main--{repo}--{owner}.aem.page/
- Live: https://main--{repo}--{owner}.aem.live/

## Documentation

Before using the aem-boilerplate, we recommand you to go through the documentation on https://www.aem.live/docs/ and more specifically:
1. [Developer Tutorial](https://www.aem.live/developer/tutorial)
2. [The Anatomy of a Project](https://www.aem.live/developer/anatomy-of-a-project)
3. [Web Performance](https://www.aem.live/developer/keeping-it-100)
4. [Markup, Sections, Blocks, and Auto Blocking](https://www.aem.live/developer/markup-sections-blocks)

## Installation

```sh
npm i
```

## Linting

```sh
npm run lint
```

## Local development

1. Create a new repository based on the `aem-boilerplate` template and add a mountpoint in the `fstab.yaml`
1. Add the [AEM Code Sync GitHub App](https://github.com/apps/aem-code-sync) to the repository
1. Install the [AEM CLI](https://github.com/adobe/helix-cli): `npm install -g @adobe/aem-cli`
1. Start AEM Proxy: `aem up` (opens your browser at `http://localhost:3000`)
1. Open the `{repo}` directory in your favorite IDE and start coding :)
