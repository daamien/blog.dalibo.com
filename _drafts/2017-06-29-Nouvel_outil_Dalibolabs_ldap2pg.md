---
layout: post
title: Nouvel outil Dalibo Labs - ldap2pg
author: Léo Cossic
twitter_id: dalibolabs
github_id: dalibo
tags: [ldap, ldap2pg, postgresql, tool, opensource, dalibolabs, dalibo, labs]

---

*Paris, le 29 juin 2017*

[Étienne](https://github.com/bersace), un des développeurs de notre Agence dev, a commencé un nouveau projet pour répondre au besoin d'un client Dalibo. Le client a besoin d'exprimer finement les règles de synchronisation des rôles et des ACLs de Postgres depuis un annuaire Active Directory. Ainsi est né `ldap2pg` !


<!--MORE-->
---

`ldap2pg` est votre couteau-suisse pour synchroniser les rôles depuis n'importe quel répertoire LDAP. La livraisons de la version 1.0 avec la gestions complète des rôles est imminente. La suite du programme est la gestion des ACL : `GRANT` et `REVOKE`.

`ldap2pg` est sous license Postgres, toutes contributions sont les bienvenues, même et surtout les plus petites !  Le projet est publié sur GitHub avec tests unitaires et tests fonctionnels exécutés par CircleCI. Le projet est testé sur CentOS 7, pour python2.7 et python3.4.