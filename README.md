# Hercules
Installation et Configuration d'Hercules sous MacOS Aarch64 avec ADCD V1R3

## Installation Step by Step 

1. Installer homebrew si pas déjà fait:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
2. Installer Hercules avec homebrew:
```
brew install hercules
```
3. Ajouter un fichier de configuration hercules.cnf dans /opt/homebrew/Cellar/hercules/4.8
   (le fichier est disponible dans ce repo)
4. Tester de lancer l'émulateur
```
hercules -f /opt/homebrew/Cellar/hercules/4.8/hercules.cnf
```
<img width="575" height="396" alt="Capture d’écran 2025-07-27 à 19 40 56" src="https://github.com/user-attachments/assets/ffa38de1-1a6f-424f-938e-273712569b4d" />


5. 
