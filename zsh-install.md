# Install ZSH and Powerlevelk10

## Updating the System
sudo apt update && sudo apt dist-upgrade -y
sudo apt install build-essential curl file git -y

**Install zsh**  
sudo apt install zsh -y

**Checking if install correct**  
zsh --version

## Installing Oh-My-Zsh Plugin and font
sudo apt install git-core curl fonts-powerline -y

sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

**Answer Y to next**  
Do you want to change your default shell to zsh? [Y/n]

## Install Powerlevel10k
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

**Add Powerlevel theme to .zshrc**  
ZSH_THEME="powerlevel10k/powerlevel10k"

**Config and follow instruction**  
reboot or run 'p10k configure'

## Install plugins (zsh-autosuggestions and zsh-syntax-highlighting)
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions  
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting

**Add plugins to .zshrc**  
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
