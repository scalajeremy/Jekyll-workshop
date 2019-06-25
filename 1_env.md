# 1. Let's start with the setup of your environnement

We're gonna install a Ruby environnement.

You can do it by following the official [doc here](https://jekyllrb.com/docs/installation/) or follow these steps if you know what you doing:

## Linux

### Get the dependencies

```bash
# Ubuntu users
sudo apt-get install ruby-full build-essential zlib1g-dev

# Fedora users
sudo dnf install ruby ruby-devel @development-tools

# Debian users
sudo apt-get install ruby-full build-essential
```

### Setup Gem installation folder

#### For bash users:

```bash
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

#### For zsh users:

```bash
echo '# Install Ruby Gems to ~/gems' >> ~/.zshrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.zshrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

#### Don't remembering your shell?

```bash
echo $SHELL
# Expected result -> /usr/bin/zsh or /usr/bin/bash
```

## MacOS

Sorry guys but you'll need to follow [these steps](https://jekyllrb.com/docs/installation/macos/) carefully.

## Next step: [2.Install Jekyll](2_install.md)
