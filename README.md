# free-the-bash

Updates macOS Bash shell to a latest version and sets it as a default login shell

> Why 'free-the-bash' name? Originally I wanted to name
> it 'escape-from-zsh', but it did not sound fair for
> zsh. I just want modern Bash to be a first class
> citizen in macOS ecosystem.

## Why

Latest macOS comes preinstalled with zsh login shell. Bash shell is still available for scripting, but it stuck at version 3.2 written in 2007. There are several blog posts outlining the steps on how to update Bash to the latest version and how to make updated Bash a default login shell, however I could not find a 'prepackaged' solution automating this task.

## What it does

1. Installs latest Bash shell via Homebrew package manager
2. Adds updated Bash to a list of available login shells
3. Sets updated Bash as a default login shell for a logged in user

## Dependencies

- [Homebrew](https://brew.sh)

## References

- [Google Shell Guide](https://google.github.io/styleguide/shellguide.html)

## License

[MIT](LICENSE)