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



