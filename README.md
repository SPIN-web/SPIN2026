# SPIN2025


This is the website for SPIN 2025, adapted from that of [SPIN 2024]
(https://spin-web.github.io/SPIN2024/), for which you can find the sources [here](https://github.com/SPIN-web/SPIN2024).

This brief guide was written by Gidon Ernst <gidon.ernst@lmu.de> (LMU Munich). Feel free to get in touch with any question.

## Setup

The website is made with Jekyll and hosted on [GitHub pages](https://docs.github.com/en/pages/). It should work out-of-the-box by pushing the respective changes to the `main` branch of the repository.

It is recommended to develop and test this site locally with the built-in web server of the toolchain. This guide is for Unix-like systems and has been tested on Arch Linux (September 2024).

Install [Ruby](https://www.ruby-lang.org), e.g., with the standard package manager of your distribution, make sure the binary `bundle` of its [package manager](https://bundler.io/) is available.

Set up `bundle` to use a user-writable directory for installing dependencies, cf. [this Stack Overflow question](https://stackoverflow.com/questions/40385493/how-to-run-bundle-install-as-normal-user).
You may want to persist this as part of your shell configuration.

    export GEM_HOME="$(ruby -e 'puts Gem.user_dir')"
    export PATH="$GEM_HOME/bin:$PATH"

Install the dependencies for the website (once)

    bundle install

Run the built-in webserve and point your browser to the "Server address" as shown

    bundle exec jekyll serve

