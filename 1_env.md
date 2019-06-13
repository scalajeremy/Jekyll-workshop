# 1. Let's start with the setup of your environnement

First you'll need a ruby environnement. It's pretty easy how to do it, follow these steps:

[MacOSX](#macosx)

## Linux

Install dependencies:

```sh
sudo apt-get install ruby-full build-essential zlib1g-dev
```

### If you use Bash

```sh
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

### If you use ZSH

```sh
echo '# Install Ruby Gems to ~/gems' >> ~/.zshrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.zshrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

### Finally, install Jekyll

```sh
gem install jekyll bundler
```

That's it! You're ready to start using Jekyll.

## MacOSX
