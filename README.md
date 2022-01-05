# newkdev/setup-depot-tools
This action will install Google's Depot Tools to the workflow's PATH, allowing for easy interaction within your workflow. This allows your subsequent action steps to utilize the tools contained within Depot Tools.
> The Chromium depot_tools suite contains many git workflow-enhancing tools which are designed to work together to enable anyone to wrangle the Chromium codebase expertly. [The Chromium Project](https://commondatastorage.googleapis.com/chrome-infra-docs/flat/depot_tools/docs/html/depot_tools_tutorial.html#_setting_up)

## Example Usage
```yml
- name: Install Depot Tools
  uses: newkdev/setup-depot-tools@v1.0.0
```

## Home does this work?
Depending upon the platform of the workflow being used, the proper code will be downloaded and added to the action's PATH. This mean cloning the [depot_tools repo](https://chromium.googlesource.com/chromium/tools/depot_tools) for unix systems and extracting the [depot_tools bundle](https://storage.googleapis.com/chrome-infra/depot_tools.zip) for windows. This also overrides the local Python installations with that of Depot Tools and then runs `gclient` to install platform-specific tools not stored within the source.

# Contributing
We love to see contributions and suggestions regarding how to better our projects! Opening an issue or pull request will prompt the team to review your work, and we'll work with you to incorporate your changes! For further inquiries please reach out to us at [contact@newk.dev](mailto:contact@newk.dev).