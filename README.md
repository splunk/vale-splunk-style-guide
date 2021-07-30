# Splunk Style Guide for Vale

This repo contains a set of linting rules for Vale based on the [Splunk Style Guide](https://docs.splunk.com/Documentation/StyleGuide/current/StyleGuide/Howtouse). The project originated as ([Hack 1277](https://cd.splunkdev.com/hackathons/2021/hack-1277-automate-prose-linting-for-o11y-docs)). 

[Vale](https://github.com/errata-ai/vale) is an open source prose linter that can check the content of documents in several formats against style guide rules. The goal of a prose linter is automating style guide checks in docs-as-code environments, so that style issues are detected before deploy or while editing documentation in a code editor. For a quick introduction on Vale and its features, read my blog post [First steps with Vale](https://passo.uno/posts/first-steps-with-the-vale-prose-linter/).

# Get started

1. Install Vale with `brew install vale` or similar commands. See [Installation](https://docs.errata.ai/vale/install).
2. (Optional) Install the [Vale add-on for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=errata-ai.vale-server).
4. Run `vale .` from the root folder of the repo, or save/edit a file using Visual Studio Code.

For more information, see [Usage](https://docs.errata.ai/vale/cli).

# Folder structure

- `.vale.ini` contains the Vale settings. See [Configuration](https://docs.errata.ai/vale/config).
- `styles/Splunk` contains the Splunk rules for Vale. See [Styles](https://docs.errata.ai/vale/styles).
- `test-set` contains subfolders with sample docs. Pass the path as an argument to Vale to test specific docs.

# Resources

- [Vale's official documentation](https://docs.errata.ai/vale/about)
- [Vale Studio, a web-based Vale rules editor](https://vale-studio.errata.ai/)
- [Regex101, a web-based regular expressions editor](https://regex101.com/)

# Contribute

To contribute to this repo, open a merge request.

I suggest that contributors get acquainted with Vale first. Basic knowledge of regular expressions and YAML is a must.

# Goals

The main goals of this project are the following:

- Create a set of Vale rules with highest possible coverage of what's in the Splunk Style Guide.
- Use this repository as a git submodule for any docs-as-code repository that requires prose linting.
- Adjust the scoping, error level, and quality of each rule so that they don't interfere with deployments.


