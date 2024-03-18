## Install guide for NixOs  

### 1. Add git, gnu stow and firefox for easy access to this tutorial
```
environment.systemPackages = with pkgs; [
      git
      stow
      firefox
]
```
### 2. Rebuild
```
sudo nixos-rebuild switch
```
### 3. Add Unstable
```
nix-channel --add https://nixos.org/channels/nixpkgs-unstable nixpkgs-unstable
```
### 4. Activate Unstable
```
nix-channel --update
```
### 5. Clone dotfiles
```
git clone https://github.com/EdgeLordKirito/dotfiles.git
```
### 6. Symlink nixconfig
in the etc/nixos directory run
```
ln -s ~/.config/nix/configuration.nix configuration.nix
ln -s ~/.config/nix/hardware-configuration.nix hardware-configuration.nix
```
### 6. Run stow 
```
cd dotfiles
stow .
```
### 7. Rebuild
```
sudo nixos-rebuild switch
```

### 8. Celebrate
Congrats you should now have my NixOs setup from a minimal installation
