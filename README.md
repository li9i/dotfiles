# Getting started

```bash
# Clone repo in the home directory
git clone git@github.com:li9i/dotfiles.git ~/
```

```bash
# Use stow to symlink the contents of the directories under ~/dotfiles to one
# level up, under ~/.
# References:
#  * https://www.gnu.org/software/stow/
#  * https://linuxvox.com/blog/stow-linux/
cd ~/dotfiles
stow --dotfiles bash git octave tmux vim
```

File `bashrc_li9i_entrypoint` serves as an aggregator of all the different `.bashrc*` files

```bash
echo "if [ -f ~/.bashrc_li9i_entrypoint ]; then" >> ~/.bashrc
echo "  . ~/.bashrc_li9i_entrypoint"             >> ~/.bashrc
echo "fi"                                        >> ~/.bashrc
```
