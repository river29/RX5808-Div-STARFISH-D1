# Outil RX5808-Div
Guide de téléchargement du micrologiciel RX5808

RX5808下载固件指南

一1. Version STM32

Le firmware du STM32 est STM32_Firmware.zip. Le STM32 peut être téléchargé via USB, UART ou SWD, je n'entrerai donc pas dans les détails ici.

二2. Version ESP32


1、Décompressez le dossier ESP32_FirmWare.zip dans ce répertoire et obtenez trois fichiers xxx.bin, comme indiqué ci-dessous :

![image](https://user-images.githubusercontent.com/66466560/183941319-5b98264a-7aaf-42ed-a1c0-3359cdcafc04.png)

2、Décompressez le dossier flash_download_tool_3.9.2_0.zip dans ce répertoire pour obtenir les fichiers suivants :


![image](https://user-images.githubusercontent.com/66466560/183941369-ae1474e4-ccc6-4826-a105-4ce33f092943.png)
 
3、Double-cliquez sur flash_download_tool_3.9.2_0.exe pour ouvrir le programme de téléchargement :


![image](https://user-images.githubusercontent.com/66466560/183941402-a557a9e5-d548-456c-b53c-5481e826d153.png)

Sélectionnez ESP32 et cliquez sur OK.

4.Ouvrez les fichiers bin décompressés dans l'ordre suivant :：

         bootloader.bin     0x1000
         
         partition-table.bin  0x8000
         
         RX5808.bin        0x10000 
         
 ![image](https://user-images.githubusercontent.com/66466560/183941506-98f46ba4-1fad-475d-91d7-f391da223f43.png)

5.Réglez SPIFLASH comme indiqué ci-dessous :


![image](https://user-images.githubusercontent.com/66466560/183941552-d3622ece-0861-4cdc-a700-2601824ec92c.png)
 
6.Sélectionnez le port COM et téléchargez : (L'image suivante montre le téléchargement terminé)
 
![image](https://user-images.githubusercontent.com/66466560/183941582-fadea089-f43e-490e-819a-48b0e2b0c2e5.png)

7.Si vous rencontrez un problème de distorsion de l'écran,
utilisez le firmware ESP32_FirmWare_Slow.

La nouvelle version du firmware du module ajoutée en 2022.8.10 est ESP32_Model_FirmWare. 
