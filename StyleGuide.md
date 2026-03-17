# NotPrivateAPIs DocC Documentation Style Guide

This file serves as a reference for contributing to the NotPrivateAPIs DocC bundle. When creating new documentation articles, please adhere to the following conventions.

## 1. Organization Style
- **Framework Directories**: Group articles inside directories corresponding to the Apple framework they belong to (e.g., `UIKit`, `SwiftUI`, `NSObject`).
- **Topic Separation**:
  - Create a primary Markdown file for the main class or structure (e.g., `UIAlertController/UIAlertController.md`).
  - Create separate Markdown files for each specific method, initializer, or property within the same directory (e.g., `UIAlertController/_setHeaderContentViewController.md`).
- **Linking**: The primary class/struct file must include a `## Topics` section linking to its child pages using the `<doc:FileName>` syntax.
  ```markdown
  ## Topics

  - <doc:_setHeaderContentViewController>
  ```

## 2. Writing Style
- **Title**: Begin with an H1 (`#`) matching the exact API name (e.g., `# _setHeaderContentViewController(_:)`).
- **Metadata**: Include a `@Metadata` block immediately after the title specifying:
  - `@TitleHeading("Type")` where "Type" is "Class", "Structure", "Instance Method", "Initializer", etc.
  - `@Available` tags to specify OS availability if known.
  - `@PageColor(colorName)` based on the following correlation with `@TitleHeading`:
    - **blue**: `Class`, `Structure`
    - **red**: `Instance Method`, `Initializer`, `Technology Overview`
    - **green**: `Instance Property`
    - **orange**: `Protocol`
    - **purple**: `Tool`
  ```markdown
  @Metadata {
      @TitleHeading("Instance Method")
      @Available(iOS, introduced: "8.0")
      @PageColor(red)
  }
  ```
- **Short Description**: Provide a brief, one-line summary directly below the `@Metadata` block.
- **Overview**: A `## Overview` section detailing the API's purpose, background, and typical usage.
- **Warnings**: For private/internal APIs, include a GitHub-style blockquote warning such as: `> Warning: It is unknown when [API] was added... Testing is required...`
  ```markdown
  > Warning: It is unknown when `_setHeaderContentViewController(_:)` was added to `UIAlertController` and exactly which operating systems/versions support it. Testing is required before release into production and `_setHeaderContentViewController(_:)` may be removed in the future.
  ```
- **Sections**: Depending on the API, include `## Method`, `## Parameters`, or equivalent sections.
- **Examples**: A `## Example` section featuring a complete, compilable Swift code snippet (such as a full `UIViewController` or SwiftUI `ContentView`).
- **Credits**: A `## Credits` section linking to the researcher/developer who discovered the private API on X/Twitter or other social media platforms.
  ```markdown
  ## Credits

   - [Developer Name](https://x.com/username)
  ```

## 3. Image Layout Style 
- **Formatting**: Use standard Markdown syntax for images and videos: `![Alt Text](Filename)`.
- **Placement**: Place graphical examples inline directly within the `## Overview` section to visually demonstrate what the API does.
