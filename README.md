[Vale](https://github.com/errata-ai/vale) is an open source prose linter that can check the content of documents in several formats against style guide rules. The goal of a prose linter is automating style guide checks in docs-as-code environments, so that style issues are detected before deploy or while editing documentation in a code editor. This repo contains a set of linting rules for Vale based on the [Splunk Style Guide](https://docs.splunk.com/Documentation/StyleGuide/current/StyleGuide/Howtouse).

# Get started

1. Clone the repository.
2. Install Vale with `brew install vale` or similar commands. See [Installation](https://docs.errata.ai/vale/install).
3. (Optional) Install the [Vale add-on for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=errata-ai.vale-server).
4. (Optional) Set `vale.core.useCLI` to `true` in the extension settings (Preferences > Extensions > Vale > Use CLI).
5. Run `vale .` from the root folder of the repo, or save/edit a file using Visual Studio Code.

For more information, see [Usage](https://docs.errata.ai/vale/cli).

# Folder structure

- `.vale.ini` contains the Vale settings. See [Configuration](https://docs.errata.ai/vale/config).
- `styles/Splunk` contains the Splunk rules for Vale. See [Styles](https://docs.errata.ai/vale/styles).

# Use as a git submodule

To use the contents of this repository as a [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules), run the following git commands from the target repo:

```bash
git submodule add git@github.com:splunk/vale-splunk-style-guide.git
git submodule update --init --recursive
git commit -m "Added the Vale submodule to the project."
git push
```

Copy the sample `.vale.ini` file to the root of your repository, and change the path to point to the submodule:

```ini
StylesPath = vale/styles
```

To update the submodule, run the following git command from the root folder of the repository:

```
git submodule update --remote --merge
```

# Resources

- [Vale's official documentation](https://docs.errata.ai/vale/about)
- [Regex101, a web-based regular expressions editor](https://regex101.com/)
