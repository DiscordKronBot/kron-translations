---
title: Sauvegarde des rôles
category: modules
emoji: 🛟
summary: Instantanés des rôles, de leurs permissions et de qui les a ; répare un serveur abîmé.
order: 6
---

Un membre du staff a supprimé des rôles, changé leurs permissions ou retiré des rôles à tout le monde ? **Sauvegarde des rôles** remet le serveur comme avant.

## Ce qui est sauvegardé

Toutes les heures, Kron note :

- chaque rôle : nom, couleur, affichage séparé, mentionnable, **permissions**, place dans la liste ;
- **qui a quel rôle** ;
- les **permissions des rôles dans chaque salon**.

Rien n'est enregistré si rien n'a changé. Kron garde les 60 dernières sauvegardes automatiques et les 20 dernières manuelles. Le bouton **Sauvegarder maintenant** en fait une tout de suite.

## Réservé au propriétaire

Seul le **propriétaire du serveur** voit cette page, active ou coupe le module et lance une restauration. Il peut permettre aux **administrateurs** de l'utiliser aussi. Un membre qui a « Gérer le serveur » ne peut rien y faire : celui qui a causé les dégâts ne peut pas effacer la solution.

## Réparer

1. Choisis une sauvegarde d'**avant** le problème, puis **Comparer**. Kron affiche ce qu'il ferait, sans rien changer :
   - les rôles supprimés à recréer (et combien de membres les avaient) ;
   - les rôles modifiés à remettre comme avant ;
   - les membres qui récupèrent leurs rôles ;
   - les permissions de salons à remettre.
2. Coche les étapes voulues, confirme, puis **Restaurer**. La progression s'affiche.

Une restauration **ne retire jamais rien** : elle recrée, répare et redonne. Une sauvegarde de l'état actuel est faite juste avant.

> [!NOTE]
> Un rôle recréé a un **nouvel identifiant** (Discord ne permet pas de reprendre l'ancien). Kron met à jour ses propres réglages qui visaient l'ancien rôle (tickets, formulaires, niveaux…). Les autres bots devront être reconfigurés.
>
> Les membres qui ont **quitté** le serveur ne peuvent pas être ramenés.

## Alerte

Choisis un **salon d'alerte** : quand un rôle est supprimé, Kron y écrit lequel et **qui** l'a supprimé (journal d'audit).

Le rôle **Kron** doit être tout en haut de la liste des rôles pour recréer et redonner tous les rôles.
