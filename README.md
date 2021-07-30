One of the first things that occurred to me after exploring the Splunk Style Guide was turning most of its content into rules for the Vale prose linter, so that we can check adherence of docs against our style guide automatically, either while editing them using VS Code or in a CI/CD pipeline.

From the [blog post](https://passo.uno/posts/first-steps-with-the-vale-prose-linter/) I wrote about it in my personal website:

> Vale is one of the most popular prose linters in circulation. Think of it as a robotic reconnaissance team that scouts documentation for stylistic issues before they get to anybody's eyes. This sort of computer-assisted editing can save you tons of time.

# Resources

- https://github.com/errata-ai/vale
- https://docs.splunk.com/Documentation/StyleGuide/current/StyleGuide/Howtouse

# How to test

1. Install Vale with `brew install vale`
2. Install the Vale add-on for Visual Studio Code (https://github.com/errata-ai/vale-vscode)
3. Restart Visual Studio Code
4. Run `vale .` from the root folder of the repo, or save/edit a file using VS Code

