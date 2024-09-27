

### Vocabulaire

**Réponse à Incident** : Ensemble de processus et d’action à déclencher en cas d’incident informatique (Isoler les machines touchées, mener une investigation, PCA/PRA, etc ...)
**First Responder** : Première personne qualifiée arrivant sur les lieux pour mener les premières investigations
Certaines organisations appellent les équipes de réponses aux incidents “équipe de réponse aux incidents de sécurité informatique” (CSIRT) ; “équipe de réponse aux incidents de sécurité” (SIRT) ou “équipe de réponse aux incidents informatiques” (CIRT).

**Chain of custody** : Représente un rapport ou procès-verbal établi lors de la saisie d'une information numérique et de son support (peut contenir les informations suivantes) :
- Numéro d’enquête associé
- Dates, lieux et conditions de l’acquisition
- Détenteur antérieur
- Nature du support (description physique + photo si besoin)
- Les métadonnées, structure des données
- Situation d’accès aux données
- Le libellé du support
- Les dates d’ouverture/fermeture du support
- Les modifications potentielles
- Etat de restitution du support

**Imaging** : Processus de copie d’un support de stockage à investiguer sans modifier son intégrité. 
**Artefact** : Élément (à analyser/vérifier) pouvant être pertinent pour l'investigation (Fichiers, Logs, clefs de registre, etc ...). Un artefact est comparable à un indice.
**Evidence** : Élément pertinent pour l’enquête parce qu'il soutient ou réfute une hypothèse. Une évidence est comparable à une preuve.
**Chain of evidence** : Séquençage des preuves identifiées lors de l’investigation (dans l’ordre chronologique des faits)
**Timeline** : Collecte d’information (actions,évènements, données, ... ) d’une date A à une date B pouvant dévoiler des informations précieuse sur l’enquête et conduire les investigateurs à des évidences.
**compromission** : intrusion dans un système ayant pour conséquence la divulgation, la modification ou la destruction d'informations. Son étendue peut être plus ou moins importante (un système, un réseau ...)
**signe de compromission** : comportement suspect laissant à penser à une compromission (service avec un nom bizarre, alerte antivirus, popup, ralentissement général ...)
**Indicateur de compromission (IOC)** : élément d'investigation numérique qui indique d'un endpoint ou un réseau a été compromis (IP/Domaine, exécutable, librairie DLL, code exécutable ...)





--------

# METHODOLOGIE

## 1 - Contexte et constat de l'incident

- Prise en compte du contexte
- Etablir un périmètre
- Témoignage
- Bref rapport de situation

## 2 - Description du problème

- Live
- Récupérer des informations sur le système
- Découverte des premières hypothèses
- Définir les priorités de l'investigation

## 3 - Acquisition des preuves

- Capture de la RAM
- Copie bas niveau des disques
- Montage des images en lecture seule
- Respect d'intégrité
- Extraction des logs, ruches, et autres fichiers importants
- Calcul des hashs

## 4 - Analyse de la timeline

- Génération d'une timeline globale
- Recherche d'éléments suspicieux
- Analyse des MAC times
- Chronologie des faits

## 5 - Analyse des fichiers

- Recherche d'artefacts
- Découverte de fichiers suspects
- Garder à l'esprit l'existence d'anti-forensic

## 6 - Recherche de bytes/Chaine

- Découverte de strings dans les fichiers suspects
- Recherche de signatures

## 7 - Récupération des données

- Copie des fichiers découverts sur le système
- Calculs des hashs
- Découverte de fichiers suprimés
- Analyse en profondeur du système de fichiers
- Corrélation des données

## 8 - Documenter les résultats

- Décrire toutes les manipulations de l'investigation
- Déterminer les actions à venir et priorités d'investigation
- Recommandations et réponse à incident
- Vulgarisation et support



--------------

# Artefacts systèmes Windows

- Chercher des dossiers différents des dossiers d'origine du système (autre que Programmes, Programmes (x86), Utilisateurs, Windows)
- Vérifier le chemin d'installation des programmes dans REGEDIT
	HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion       
	==ProgramFilesDir== ,  ==ProgramFilesDir (x86)== et ==ProgramFilesPath==
- Vérifier le répertoire Windows pour trouver des fichiers suspects
	%Windir%\\System32\\
	Présence de la base SAM, Base de registre, drivers, fichier host ...
- Données d'applications
	- AppData :
	%userprofile%\\AppData
	%AppData%
	- ProgramData
	%ProgramData%

- Données utilisateur
	C:\\Users\\%username%\\==NTUSER.DAT==










# Toolbox

## Commandes et outils Windows

#### Système de fichiers NTFS (_MFT - Master File Table_)
- Secteur = 512 Octets
- Cluster = 4096 Octets sous NTFS
- $MFT sur le secteur 0
	Récupérable par plusieurs moyens et outils :
		- **FTK Imager** (sans oublier d'enlever les attributs [Invite de commande] : `attrib -S -H $MFT`)
		- **Sleuthkit** : Copie sous système Linux après montage de l'image
			- `mmls /root/Case01/clone1.raw`
			- _identifier la partition système_
			- `icat -o 239616 /root/Case01/clone1.raw 0 > MFT`
	$MFTMirr : Copie des 4 premières entrées de la $MFT
	$LogFile : Fichier de journalisation des changements de métadonnées
	$Volume : Contient toutes les informations du volume (label, version ...)
	$AttrDef : Table de tous les attributs NTFS ($10, $30...)


#### Base de registre
- Extraction d'une ruche
	- Commande en live, sous Windows : `reg save HKLM\\SYSTEM C:\\system_backup.reg`
	- Sous Linux, récupérer le dossier : **C:\\Windows\\system32\\config** 
		Les fichiers utiles composants la base de registre sont :
		- Components
		- default
		- SAM
		- Security
		- Software
		- System
	Outils utiles : 
	- **AccessData FTK Imager** pour l'extraction
	- **Registry Explorer** pour visualiser le contenu et l'exploiter (load hive --> Select ALL)


#### Journaux d'évènements
- Windows 2000/Server2003/Windows XP : **%SystemRoot%\\System32\\Config\\**
- Windows Vista et + : **%SystemRoot%\\System32\\winevt\\Logs\\**



#### Services systèmes
- Vérifier les services lancés : HKLM\\SYSTEM\\CurrentControlSet\\Services
- Groupes de services : HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Svchost
- Pour lister les services   `C:> sc queryex type= service state= all`

#### Volume Shadow Copy (Volume Snapshot Service ou VSS)
Outils : **mslink**, **VSC toolset**, **vssadmin**, **shadowExplorer**
	REGEDIT :
		- HKLM\\SYSTEM\\CurrentControlSet\\Services\\VSS --> Fournit les informations de configuration de VSS
		- HKLM\\SYSTEM\\CurrentControlSet\\Control\\BackupRestore
			- FileNotToBackup : fichiers exclus de la sauvegarde ou de la restauration
			- FilesNotToSnapshot : fichiers à supprimer avant backup
			- KeysNotToRestore : clés de registre à ne pas restaurer

#### Calcul de hash
- Windows [Powershell] :  `PS C:\Windows\system32> get-date -Format "dddd MM/dd/yyyy HH:mm K" ; Get-FileHash C:\Users\Root\Desktop\info.txt -Algorithm SHA1`
- Windows [invite de commande] `certutil -hashfile c:\file.zip MD5`
-  Outil : Bento (Acquire/Hash) **HashMyFile**


#### Timestamp et fuseau horaire
par défaut, **UTC 0**


Historique des applications


MRU



Périphériques USB (Stockage de masse)





post compromise active directory list pwndef : https://www.pwndefend.com/2021/09/15/post-compromise-active-directory-checklist/
LOGONTRACER github


## Machine virtuelle, VMDK

--> Utiliser les fonctionnalités de VirtualBox pour ajouter le VMDK à la VM dédiée aux investigations

Convertir un disque virtuel au format RAW
	`C:\Program Files\Oracle\VirtualBox> VBoxManage.exe clonemedium D:\path\src\to\file.vmdk X:\path\dst\file.img --format raw`


## Commandes LINUX

`lsblk` : Lister les disques et partitions

`dd` : utilitaire pour cloner une partition/un disque
	`dd if=/dev/sdb of=/root/share/clone.img bs=4096 status=progress`

Monter une image disque en format Raw
	`mount -t ntfs -o ro,show_sys_file,streams_interface=windows,offset=$((512*yy)) /root/Case01/clone1.raw /mnt/Case01`
	Alternative :
	`kpartx -a /root/Case01/clone1.raw`
	`mount -t ntfs -o ro,show_sys_file,streams_interface=windows,offset=$((512*yy)) /dev/mapper/loop1p2.raw /mnt/Case01`




--------------
----------

# Outils

### Système Windows déconnecté


| Dossier cible                        | contenu                             | logiciel(s) associé(s)                                                                                                                                                                   |     |
| ------------------------------------ | ----------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| [root]\$MFT                          | Master File Table d'un système NTFS | Extraction : **AccessData FTK Imager**, **Autopsy**<br>Création d'une timeline : (Zimmermans-tools) **MFTECmd.exe**<br>Visualisation timeline : (Zimmermans-tools) **Timeline Explorer** |     |
| [root]\\Users                        | Fichiers profiles utilisateurs      | Extraction : **AccessData FTK Imager**, **Autopsy**<br><br>                                                                                                                              |     |
|                                      |                                     |                                                                                                                                                                                          |     |
| [root]\\Windows\\System32\\drivers   | Fichiers drivers et dépendances     | Extraction : **AccessData FTK Imager**, **Autopsy**<br><br>                                                                                                                              |     |
| [root]\\Windows\\System32\\config    | Base de registre et base SAM        | Extraction : **AccessData FTK Imager**, **Autopsy**<br>Exploitation : (Zimmermans-tools) **Registry Explorer**<br>Exploitation : (Bento) **USBDeview** pour [...]\\config\SYSTEM<br>     |     |
| [root]\\Windows\\Prefetch            | Système de cache Windows            | Extraction : **AccessData FTK Imager**, **Autopsy**<br>Exploitation : (Bento) **WinPrefetchView**                                                                                        |     |
| [root]\\Windows\\System32\\winevt    | journaux d'évènements en *.evtx     | Extraction : **AccessData FTK Imager**, **Autopsy**<br><br>                                                                                                                              |     |
| [root]\\Windows\\temp                | souvent utilisé par les malwares    | Extraction : **AccessData FTK Imager**, **Autopsy**<br><br>                                                                                                                              |     |
| [root]\\~dossier d'image~\\thumbs.db | Windows Thumbnail Cache             | Extraction : **AccessData FTK Imager**, **Autopsy**<br>Exploitation :                                                                                                                    |     |
|                                      |                                     |                                                                                                                                                                                          |     |
