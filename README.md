# RX5808-Div
## 1. Conception d'interface basée sur LVGL
Pour une vidéo de démonstration, veuillez consulter : https://www.bilibili.com/video/BV1yr4y1371b

![ui](https://user-images.githubusercontent.com/66466560/218503938-571cd1fa-2c89-4279-a6aa-281c7fcf8234.jpeg)


1) Sur l'interface principale, appuyez longuement sur le bouton OK pour verrouiller/déverrouiller le canal manuel, puis appuyez brièvement pour accéder au menu. Une fois déverrouillé, appuyez vers le haut, le bas, la gauche ou la droite pour régler la fréquence.

2) L'interface du menu est divisée en trois parties : Numérisation ; Paramètres ; À propos.

Appuyez sur le haut et le bas pour changer d'options de menu, confirmez pour accéder au sous-menu et sur le bouton gauche pour revenir à l'interface principale

3) Le menu de numérisation comporte trois sous-contenus :

L'analyse de l'image montre la force du signal de la fréquence 5300-5900MHz ;

L'écran de balayage de tableau affiche la puissance du signal du canal de transmission d'image dans différentes couleurs. Une fois le balayage terminé, la fréquence est commutée sur le canal avec la meilleure puissance de signal actuelle et affichée dans le coin supérieur droit.

L'étalonnage RSSI est utilisé pour étalonner le RSSI. Si la transmission d'image n'est pas activée, l'étalonnage échouera. En cas de réussite, le résultat sera enregistré.

4) L'interface de configuration permet de régler l'intensité du rétroéclairage de l'écran, la vitesse du ventilateur, l'animation de démarrage, le buzzer, etc. Le format OSD doit être enregistré et rouvert sur la page principale pour prendre effet.

5) L'interface À propos affiche les informations pertinentes.
 

## 2. Prise en charge OSD
La fonction OSD est ajoutée par Linmianbao (Bilibili ID), en mode non superposé, et peut être activée en déverrouillant l'interface principale.

Voir la vidéo de démonstration : https://www.bilibili.com/video/BV1ya411g78U qui est entièrement synchronisée avec l'interface utilisateur du récepteur.

système d'exploitation。

![osd](https://user-images.githubusercontent.com/66466560/218504602-102e7fe0-b935-48ca-be9e-f459200034c8.jpg)


## 3. Conception du matériel
Adresse open source du matériel : https://oshwhub.com/ftps/rx5808-div 




# CONTENU OSHWHUB : 
## 1. Conception d'interface basée sur LVGL
Pour une vidéo de démonstration, veuillez consulter : https://www.bilibili.com/video/BV1yr4y1371b

![ui](https://user-images.githubusercontent.com/66466560/218503938-571cd1fa-2c89-4279-a6aa-281c7fcf8234.jpeg)



### 1) Sur l'interface principale, appuyez longuement sur le bouton OK pour verrouiller/déverrouiller le canal manuel, et appuyez brièvement pour accéder au menu ; une fois déverrouillé, appuyez vers le haut, le bas, la gauche et la droite pour régler la fréquence.

### 2) L'interface du menu est divisée en trois parties : Numérisation ; Paramètres ; À propos.

Appuyez sur le haut et le bas pour changer d'options de menu, confirmez pour accéder au sous-menu et sur le bouton gauche pour revenir à l'interface principale

### 3) Le menu de numérisation comporte trois sous-contenus :

L'analyse de l'image montre la force du signal de la fréquence 5300-5900MHz ;

L'écran de balayage de tableau affiche la puissance du signal du canal de transmission d'image dans différentes couleurs. Une fois le balayage terminé, la fréquence est commutée sur le canal avec la meilleure puissance de signal actuelle et affichée dans le coin supérieur droit.

L'étalonnage RSSI est utilisé pour étalonner le RSSI. Si la transmission d'image n'est pas activée, l'étalonnage échouera. En cas de réussite, le résultat sera enregistré.

### 4) L'interface de configuration permet de régler l'intensité du rétroéclairage de l'écran, la vitesse du ventilateur, l'animation de démarrage, le buzzer, etc. Le format OSD doit être enregistré et rouvert sur la page principale pour prendre effet.

### 5) L'interface À propos affiche les informations pertinentes.

 

## 2. Prise en charge OSD
La fonction OSD est ajoutée par Linmianbao (Bilibili ID), en mode non superposé, et peut être activée en déverrouillant l'interface principale.

Voir la vidéo de démonstration : https://www.bilibili.com/video/BV1ya411g78U qui est entièrement synchronisée avec l'interface utilisateur du récepteur.


![osd](https://user-images.githubusercontent.com/66466560/218504602-102e7fe0-b935-48ca-be9e-f459200034c8.jpg)


Remarque : la fonction OSD n'est pas prise en charge sur le matériel d'origine : gpio25 doit être connecté à la vidéo (sortie vidéo).



## 3. Tutoriel
### 3.1 Préparez le matériel complet, y compris les planches supérieures et inférieures

Installez la carte et vérifiez si chaque alimentation est court-circuitée à la terre et s'il y a un joint de soudure à froid (principalement ESP32-PICO-D4).

Il ne devrait pas y avoir de problème avec le panneau inférieur.

### 3.2 Utilisez USB vers TTL pour vous connecter à la carte supérieure (le téléchargement ne nécessite pas de carte inférieure)

La connexion USB vers TTL et la connexion croisée TX, RX de la carte supérieure sont illustrées ci-dessous :



### 3.3 Télécharger le micrologiciel

Décompressez le dossier ESP32_FirmWare.zip dans la pièce jointe et obtenez trois fichiers xxx.bin, comme indiqué ci-dessous :



Décompressez le dossier flash_download_tool_3.9.2_0.zip dans la pièce jointe pour obtenir les fichiers suivants :



Double-cliquez sur flash_download_tool_3.9.2_0.exe pour ouvrir le programme de téléchargement :



Ouvrez les fichiers bin décompressés dans l'ordre indiqué ci-dessous :

chargeur de démarrage.bin 0x1000
table de partition.bin 0x8000
RX5808.bin 0x10000 



SPIFLASH est configuré comme indiqué ci-dessous :



Appuyez et maintenez BOOT et allumez , sélectionnez le port COM et téléchargez : (La figure suivante montre le téléchargement terminé)



## 4. Coût

Hors coût de fabrication de la planche, la planche supérieure coûte environ 30 à 40 yuans et la planche inférieure environ 60 à 70 yuans (à titre indicatif uniquement).

## 5. Remarque

### 1. J'ai vérifié la carte supérieure, mais j'ai ajouté une résistance du filtre à la sortie vidéo, j'ai supprimé la résistance de rappel du SI2302 et les étiquettes de io4 et io12 ont été inversées, ce qui a été corrigé. Les autres restent inchangées. Je n'ai pas vérifié la carte inférieure. Veuillez la vérifier vous-même avant de vérifier.

### 2. Le boîtier de l'ESP32 doit être de type LGA, ce qui sera plus difficile à souder. Lorsque 3,3 V et 5 V sont normaux, des problèmes tels que l'écran qui ne s'allume pas et l'impossibilité de télécharger sont essentiellement dus au fait que l'ESP32 n'est pas correctement soudé.

## 6. Vidéo du vol réel

La vidéo suivante est partagée par les internautes de Station B

https://www.bilibili.com/video/BV1Sv4y1T7fU

https://www.bilibili.com/video/BV1DB4y1a7WD

https://www.bilibili.com/video/BV1YY4y1P7ca

https://www.bilibili.com/video/BV1KV4y1x75c

https://www.bilibili.com/video/BV1Me411A71u

Vous pouvez rechercher plus de vidéos à la Station B

##Conception
Schéma (1 / 2)

voir lien pour schémas EDA pcb,...



