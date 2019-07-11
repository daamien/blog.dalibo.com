---
layout: post
title: ldap2pg - release v1.0
author: Étienne Bersac, Léo Cossic
twitter_id: dalibolabs
github_id: dalibo
tags: [ldap, ldap2pg, postgresql, dalibolabs, release, dalibolabs]
---

*Paris, le 06 juillet 2017*

Dalibo annnonce la première version officielle de son dernier projet [`ldap2pg`](https://ldap2pg.readthedocs.org), votre couteau-suisse pour synchroniser les rôles depuis n'importe quel annuaire LDAP. La version 1.0 apporte la gestion complète des rôles.


<!--MORE-->


Les administrateurs de bases de donnée et les administrateurs système le savent : l'authentification de [PostgreSQL s'intègre bien avec LDAP](https://www.postgresql.org/docs/current/static/auth-methods.html#AUTH-LDAP). Le postulat est seulement que les rôles soient déjà définis dans l'instance PostgreSQL. C'est là que `ldap2pg` se rend utile : il synchronise les rôles dans PostgreSQL à partir de requêtes LDAP.

Cette première version apporte une gestion complète des rôles : création et suppression, définition des options et mise-à-jour des rôles existants, gestion de l'héritage des rôles. Par défaut, `ldap2pg` fonctionne en mode audit et permet de visualiser les opérations à faire et de présenter les requêtes exactes qui seront exécutées.

Un fichier de configuration en YAML, [copieusement documentée](https://ldap2pg.readthedocs.org/en/latest/config/), permet de déclarer de manière expressive la carte de synchronisation des entrées de l'annuaire avec les rôles de PostgreSQL : comment est représenté l'héritage, quelles options attacher à un rôle, etc.

`ldap2pg` est sous license PostgreSQL, toutes contributions sont les bienvenues, même et surtout les plus petites !  Le projet est [publié sur GitHub](https://github.com/dalibo/ldap2pg) avec tests unitaires et tests fonctionnels exécutés par CircleCI. Le projet est particulièrement testé sur CentOS 7, pour python2.7 et python3.4.

---
La **prochaine étape majeure** de `ldap2pg` est de gérer les ACLs: nettoyer les ACLs avant de supprimer un rôle, s'assurer qu'un rôle a tout ses accès et pas plus, etc. Une mécanique complexe mais pas insolvable, qui simplifiera beaucoup le travail d'intégration de PostgreSQL dans votre infrastructure et améliorera la confiance dans votre gestion des accès à vos données.
