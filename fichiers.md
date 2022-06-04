---
layout: page
title: Fichiers
permalink: fichiers.html
---

Unités, tailles de fichier: qu’est-ce qu’un Giga, un Mega, un Kilobyte... 

Baes du système d’information binaire 

ASCII / UTF-8 

## Notions de File System.  

- Hierarchie des repertoires 
- Extensions de fichier 
- Metadonnées 
- Chemins 
- Alias /symlink 

Faire de la place sur son disque: connaître des outils pour faciliter cela (p.ex. [Daisydisk](https://daisydiskapp.com/)). 

Effacement accidentel, comment récupérer des données (p.ex. [Disk Drill](https://www.cleverfiles.com/fr/))

## Connectique et transfer de fichiers

Manières de transférer des données

- USB (vitesses de transfer)
- AirDrop

***

## Stockage cloud

Stockage iCloud vs stockage sur le disque (comment solutionner le cas d'un Macbook qui stocke tout dans un iCloud saturé) 

### Transmission de fichiers

Savoir transmettre un fichier, choisir la bonne méthode en fonction de la taille. Usage de Dropbox / NextCloud / GoogleMicrosoftOneBoxDriveCloud / Etc.  

## Sauvegardes

Sauvegarde: TimeMachine, Backblaze... 

***

## Formatage de disques

Formater un disque externe. Clé USB, carte mémoire, disque dur, SSD...

IMPORTANT : Le reformatage d'un disque efface toutes les données présentes sur celui-ci.

- **Apple File System (APFS)** : Le système de fichiers utilisé par macOS 10.13 ou ultérieur. À privilégier avec macOS, sur les disques internes des Mac et les disques externes USB que vous n'utiliserez que sur Mac.
- **Mac OS étendu (HFS+)** : Le système de fichiers utilisé par macOS 10.12 ou antérieur.
- **FAT, FAT32, ExFAT, NTFS** : Les systèmes de fichiers qui sont compatibles avec Windows.
- **FAT** : ce format très ancien ne peut être utilisé que sur des dispositifs de stockage de faible capacité, de 2 Go maximum. On le retrouve sur de vieilles clés USB ou cartes mémoire, souvent formatées en FAT. Au-delà de 2 Go, FAT32 et exFAT ont pris la relève.
- **FAT32** : bien que vieillissant, c'est le format le plus universel, en particulier pour les supports amovibles. Il peut être lu et écrit par les PC, les Mac, Linux, les appareils photo numériques, les TV, les consoles de jeux, les box Internet, les smartphones... Principales restrictions : **un fichier ne peut dépasser 4 Go**, ce qui est contraignant pour créer ou lire de grosses vidéos en haute définition, et la partition sur le disque ne peut excéder 2 To. Préférez-lui ExFAT quand c'est possible.
- **ExFAT** : sous l'impulsion de Microsoft, ce format a vocation à remplacer FAT32, dont il supprime les limites. Il a été conçu pour les stockages amovibles comme les clés USB et les petites cartes mémoire. Il peut être lu et écrit par Windows, macOS et Linux, et est également reconnu et correctement géré par les périphériques multimédias récents, comme la Playstation 4 et la Xbox One (mais pas la PS3 ou la Xbox 360, par exemple). Les anciens appareils ne le reconnaissent pas toujours. Si un périphérique accepte les deux formats, préférez un formatage exFAT plutôt que FAT32.

Utiliser Disk Utility sur Macos: [Guide d'utilisation](https://support.apple.com/fr-ch/guide/disk-utility/welcome/mac)

Source: [CommentCaMarche.net](https://www.commentcamarche.net/informatique/stockage/1425-choisir-un-systeme-de-fichiers-pour-le-formatage/)

### Formater en ExFAT

Guide Apple: [Formater un disque pour des ordinateurs Windows dans Utilitaire de disque sur Mac](https://support.apple.com/fr-ch/guide/disk-utility/dskutl1010/mac)

Lorsque vous formatez un disque en ExFAT, gardez les points suivants à l'esprit :

- ExFAT n'est pas compatible avec Time Machine.
- Depuis Big Sur (MacOS 11), APFS est devenu le format par défaut pour Time Machine.
- Les disques en exFAT doivent être **éjectés de manière sécurisée** pour éviter toute corruption des données, car exFAT n'est pas un système de fichiers journalisé.
- Lorsque vous utilisez des disques à la fois sur macOS et sur Windows, vous devez toujours les formater sur macOS, car les tailles d'unités d'allocation Windows (tailles de cluster) ne sont pas toutes compatibles avec macOS et pourraient empêcher le montage du disque.

Source: [site de Seagate](https://www.seagate.com/fr/fr/support/kb/how-to-format-your-drive-exfat-on-macos-big-sur-and-later/)