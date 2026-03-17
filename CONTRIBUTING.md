# Contributing to NotPrivateAPIs

First off, thank you for taking the time to contribute! This project aims to document Apple's Private APIs to make them more accessible and understandable for developers. 

The following is a set of guidelines for contributing to **NotPrivateAPIs**.

## Code of Conduct

This project and everyone participating in it is governed by the [NotPrivateAPIs Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## How Can I Contribute?

### Discussing Changes and Issues

When contributing to this repository with structural changes or taking on a large batch of APIs, please first discuss the change you wish to make via a GitHub issue. This helps avoid duplicated effort and ensures your contribution aligns with the project goals.

### Adding Documentation for a Private API

The primary way to contribute is by adding documentation for undocumented or private APIs. 

1. **Verify the API:** Ensure that the private API functions as expected. Note any OS version requirements or specific behaviors.
2. **Follow the Style Guide:** We have a specific styling format for our DocC bundle. Please refer to [StyleGuide.md](StyleGuide.md) for the **DocC Documentation Style Guide**. This includes:
   - Proper folder organization (`Framework/Class/Method`).
   - Adding required `@Metadata` (including the precise `@PageColor` and `@TitleHeading`).
   - Maintaining the warning blocks acknowledging the risks of using private APIs.
   - Providing concrete code `<Examples>` and crediting the original researcher.
3. **Link Your Pages:** Make sure any new method, property, or initializer pages are linked in their parent class/struct file under the `## Topics` section. This ensures that it properly renders in the DocC documentation.

### Pull Request Process

1. **Fork and Branch:** Fork the repository and create a new branch for your feature or API documentation.
   - Branch names should be in the format `feature/short-description` or `fix/short-description`, or `docs/short-description` for documentation changes.
2. **Clean Up:** Ensure that your Markdown files are clean and properly formatted.
3. **Commit Details:** Make clear, descriptive commit messages.
4. **Submit PR:** Submit your pull request. If this pull request is related to an open issue, please reference it in the description of the PR (e.g., `Fixes #123`).
5. **Review:** A maintainer will review your pull request, potentially ask for changes or clarifications, and then merge it in!

Again, thank you for your contributions to NotPrivateAPIs!
