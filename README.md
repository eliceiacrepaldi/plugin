# plugin linux 
git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.8.0

Alternately, you can clone the whole repo and checkout the latest branch:

git clone https://github.com/asdf-vm/asdf.git ~/.asdf
cd ~/.asdf
git checkout "$(git describe --abbrev=0 --tags)"

Add to your Shell
Operating System
Shell Installation Method

Add the following to ~/.bashrc:

. $HOME/.asdf/asdf.sh

Completions must be configured by adding the following to your .bashrc:

. $HOME/.asdf/completions/asdf.bash

Restart your shell so that PATH changes take effect. (Opening a new terminal tab will usually do it.)

You are ready to use asdf 🎉
Having Issues?

If you’re having issues with your shell not detecting newly installed shims, it’s most-likely due to the sourcing of asdf.sh or asdf.fish not being at the BOTTOM of your .bash_profile, .zshrc, config.fish config file. It needs to be sourced AFTER you have set your $PATH and AFTER you have sourced your framework (oh-my-zsh etc).
Migrating Tools

If you’re migrating from other tools and want to use your existing version files (eg: .node-version or .ruby-version), look at the legacy_version_file flag in the configuration section.
Update
Installation Method

asdf update

If you want the latest changes that aren’t yet included in a stable release:

asdf update --head

Remove

Uninstalling asdf is as simple as:

    In your .bashrc/.bash_profile/.zshrc/config.fish find the lines that source asdf.sh and the completions (this may be a ZSH Framework plugin). In Bash, the lines look something like this:

    . $HOME/.asdf/asdf.sh
    . $HOME/.asdf/completions/asdf.bash

Remove these lines and save the file.

Run

rm -rf ${ASDF_DATA_DIR:-$HOME/.asdf} ~/.tool-versions

    to completely remove all the asdf files from your system.

    (Optional) If you installed asdf using a package manager, you may want to use that package manager to uninstall the core asdf files.

That’s it! 🎉
