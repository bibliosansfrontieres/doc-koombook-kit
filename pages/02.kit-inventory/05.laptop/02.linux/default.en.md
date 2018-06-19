---
title: 'Ubuntu Linux'
---

## Ubuntu

Ubuntu can be defined as a user-friendly Linux distribution with a "simple, intuitive, and secure" interface.

By default, the computer starts up using Ubuntu.

### Installation

LTS (Long Term Support) versions, which are supported for five years, are preferred.  Version 16.04 recently replaced 14.04.  There are currently some concerns regarding guest sessions on version 18.04.

The installation and configuration can both be done using an ansible playbook (an automization tool for configuration and management) called `idbuntu`
([that is available on Github](https://github.com/bibliosansfrontieres/idbuntu)). The reading, although technical, describes the implementation in its entirety.

## Sessions

There are three types of user sessions.

### Guest Sessions


### La session invité

**La session invité** est destinée aux utilisateurs.

Parmi ses caractéristiques, cette session est amnésique : à l'ouverture de session, c'est une session toute neuve qui est recréée d'après un modèle, et elle est effacée dès sa fermeture. Cela permet de ne pas avoir à se soucier des éventuelles informations laissées par chaque utilisateur (documents personnels, connexions aux comptes sur des sites web, ...).

### La session `ideasbox`

**La session `ideasbox`** est celle qui sert de modèle à la session `invité`.

Toutes les personnalisations qui y seront effectuées se verront répliquées dans la session `invité` : fond d'écran, raccourcis, etc.

Elle n'est donc pas à utiliser au quotidien.

Le login est `ideascube`, le mot de passe est communiqué à la demande par BSF.

### La session `Admin`

**La session `Admin`** sert à l'administration et l'entretien du système. C'est la seule session qui dispose des droits administrateurs, permettant ainsi d'ajouter ou supprimer des logiciels, intervenir sur la configuration réseau et toute autre composante du système.

Elle n'est utilisée que par des techniciens, en cas de problème.

Le login est `bsfadmins`, mais on préfère créer une session dédiée pour le technicien local. Les clés SSH des techniciens BSF restent présentes dans le compte root ; si elles sont supprimées, aucun support ne peut alors être fourni.

### Voir aussi

  * [Script de création des comptes](https://github.com/bibliosansfrontieres/idbuntu/blob/master/roles/users/tasks/main.yml)
  * [Personnalisation de la session invité](https://help.ubuntu.com/community/CustomizeGuestSession) sur le wiki Ubuntu (en anglais)

## Les logiciels

La liste des logiciels généralement installés figure dans [le playbook](https://github.com/bibliosansfrontieres/idbuntu/blob/master/roles/software/tasks/main.yml).

Y figurent des logiciels de bureautique, création d'image, montage vidéo, retouche photo, édition musicale, programmation, découverte, mais aussi des jeux.

On y ajoute également le Tor browser (pour surfer anonymement sur le web), mais aussi Skype.

## Administration

Pour procéder à l'administration du système, il faudra tout d'abord se mettre en rapport avec BSF pour la mise en place d'un compte dédié. Ce compte n'est pas systématiquement créé car les besoins sont rares. Cependant, sur certains projets disposant des ressources nécessaires, un tel compte sera un plus.

Par défaut, Ubuntu télécharge et applique automatiquement les mises à jour de sécurité.


