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

5. Télécharger les fichiers ADCD V1R3 et les placer dans un folder DASD dans /opt/homebrew/Cellar/hercules/4.8
   Si mis ailleurs le chemin vers le folder DASD doit être mis à jour dans le fichier de configuration hercules.cnf
   Un téléchargement direct ou par torrent est disponible ici : https://archive.org/details/zos-v1r3-adcd#review-1721052117
```
DEFSYM DASD "/opt/homebrew/Cellar/hercules/4.8/DASD"
```
6. Installer c3270 et x3270 (terminaux pour accéder à TSO) avec homebrew:
```
brew install x3270
```   
7. Lancer hercules, puis deux terminaux c3270 ou x3270 (XQuartz nécessaire pour x3270):
```
c3270 localhost:3270
```
ou
```
x3270 localhost:3270
```
<img width="1199" height="789" alt="Capture d’écran 2025-07-27 à 19 48 22" src="https://github.com/user-attachments/assets/5b7892c4-038e-44b4-81cd-6c1026b98ae3" />

8. Appuyer sur ECHAP pour accéder à l'interface graphique du terminal Hercules:
<img width="590" height="385" alt="Capture d’écran 2025-07-27 à 19 50 01" src="https://github.com/user-attachments/assets/07391af4-6df1-477c-94d2-5cbaed910a7c" />

9. Appuyer sur "I" puis "P" puis "L" et voir ce message en bas à droite: "SELECT DEVICE FOR IPL"
<img width="590" height="385" alt="Capture d’écran 2025-07-27 à 19 51 11" src="https://github.com/user-attachments/assets/0b85edd2-f5fc-4725-946b-040abad2d380" />
10. Sélectionner le disque A en appuyant sur la touche "A", l'IPL se lance alors automatiquement:
<img width="590" height="385" alt="Capture d’écran 2025-07-27 à 19 52 08" src="https://github.com/user-attachments/assets/110c0430-72c5-4ad3-893e-8c34b339ef78" />
ectionner A en appuyant sur la touche "A"

