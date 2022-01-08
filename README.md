# free-the-bash

Updates macOS Bash shell to a latest version and sets it as a default login shell

> Why 'free-the-bash' name? I wanted to name it 'escape-from-zsh', but it did not sound fair for zsh.
> 'free-the-bash' enables first class modern Bash experince on macOS.

## Why

Latest macOS comes preinstalled with zsh login shell. Bash shell is still available for scripting, but it stuck at version 3.2 written back in 2007. I write software to run on modern Linux servers, I need full, unrestricted Bash shell on par with Linux. There are several blog posts outlining the steps on how to update Bash to the latest version and how to make updated Bash a default login shell, however I could not find a proper 'prepackaged' solution automating this task.

## What it does

1. Installs latest Bash shell via Homebrew package manager
2. Adds updated Bash to a list of available login shells
3. Sets updated Bash as a default login shell for a logged in user

In shell script it pretty much does the following:

```sh
BREW_BASH="$(brew --prefix)/bin/bash"
brew install bash
echo "$BREW_BASH" | sudo tee -a /private/etc/shells
sudo chpass -s "$BREW_BASH" "$USER"
```

But with proper checks and error handling

## Dependencies

- [Homebrew](https://brew.sh)

## References

- [Google Shell Guide](https://google.github.io/styleguide/shellguide.html)

## License

[MIT](LICENSE)