Nouveautés logicielles
----------------------

* `Shinken`_ : la version 2.4 est sortie le 5 mai 2015.
  Initialement prévue pour le 31 mars 2015, la phase de release a finalement duré un mois supplémentaire.
  La prochaine version devrait être décalée en conséquence. 
  Les changements apportés sont surtout au niveau de la qualité du code.
  Les éléments les plus notables sont la conformité du code aux règles pep8,
  le chargement des modules et les corrections de régressions introduites dans la version 2.2


* `InfluxDB`_ : la version 0.9 devait sortir à la fin du mois d'avril mais a été repoussée à une date ultérieure
  Cette version introduit un gros changement dans l'API et l'ajout de cluster.
  Il reste cependant beaucoup de travail pour arriver à la release finale : il y a encore une centaine
  de tickets ouverts sur le dépôt du projet. Cependant, l'activité du projet est importante,
  beaucoup d'utilisateurs remontent des bugs et les demandes de changement de code acceptées sont nombreuses.


* `Grafana`_ : la version 2.0 est sortie le 20 avril 2015.
  Cette version implémente un nouveau backend en Go utilisé pour les nouvelles fonctionnalités :
  l'authentification (panel d'administration) et le partage de dashboard (notion de snapshot dashboard) par exemple
  Le nouveau backend est utilisé aussi pour le stockage des dashboards, une procédure de migration est disponible
  pour importer les anciens dashboards (depuis InfluxDB par exemple).
  Autres nouveautés intéressantes : le rendu côté serveur d'une image (comme le fait Graphite),
  la possibilité d'avoir un dashboard en favori et les echelles logarithmiques.
  Grafana fourni des paquets RPM et DEB pour faciliter l'installation dans la plupart des distributions
  Plus de détails: `Annonce`_, `Nouveautés`_, `Migration`_


* `SNMPBooster`_ : c'est un module Shinken destiné à faire des requêtes en SNMP plus efficace qu'avec
  de simple sondes de supervision. Il permet de grouper les requêtes SNMP afin de réduire la consommation réseau et cpu.
  Une nouvelle version vient de sortir (1.99.13) suite à des remontées de bug par des utilisateurs.
  Un package de la dernière version est disponible sur les dépôts du projet Kaji.

.. raw:: html

    <br/>
    <br/>
    <br/>

Revue d'évenements
------------------

* Pycon Montréal 2015: `Finding Spammers & Scammers through Rate Tracking with Python & Redis`_
  `Talk (anglais)`_ traitant des problèmes rencontrés par des employés d'Evenbrite pour détecter
  par exemple les dénis de service ou les événements populaires.
  La solution présentée permet de collecter des actions réalisées et de les compter sur des périodes de temps.
  Le stockage des données et fait dans une base Redis et le schéma est similaire au principe de Carbon (projet Graphite):
  on a un compteur pour un intervalle de temps donné (pas de temps atomique pour une donnée). Cela permet un
  gain de place de stockage.
  Ces données collectées peuvent être ensuite analysées par un systeme (une intelligence artificielle, non décrit dans la présentation)
  afin d'extraire des tendances selon le type d'actions et de déduire s'il s'agit d'une activité "normale" pour le site ou non.
  Quelques détails sur Redis et le principe de "hit" `ici`_


* `Meetup Montreal Monitoring`_: Prochain événement le mardi 9 juin 2015 dans les locaux de l'UQAM.
  De nouveaux exemples de supervision seront présentés : supervision de logs,  supervision des APIs Openstack,
  supervision d'Influxdb. Une présentation de Surveil est aussi prévue (voir ci-dessous).

Développments SFL
-----------------

* `Surveil`_: Un projet orienté pour Openstack afin d'offrir une API de monitoring.
  Elle est pour l'instant basée sur Shinken pour le moteur de supervision.
  L'API elle même est developpée python, basée sur le framework d'API REST Pecan.
  L'objectif est de centraliser les requêtes au moteur de supervision et aux bases contenant
  les métriques et de fournir de l'authentification.
  La première release est prévue pour le mois de septembre


* `Kaji`_ : Le projet est toujours dans une version béta (0.2). La prochaine version de Kaji est prévue pour suivre
  le projet Surveil. En effet, l'API va venir remplacer Adagios pour la partie REST. Pour l'interface graphique,
  un frontend en Angular JS (`Bansho`_) est en cours de développement, il utilisera l'API pour récupérer les données.


* Supervision applicative : Développement du plugin check_influxdb
  Le plugin permet d'obtenir des statistiques sur une base de données InfluxDB :
  le temps de fonctionnement, le nombre d'écritures / lectures et la mémoire utilisée font
  partie des données disponibles.


* Packaging : Une mise à jour du packaging a été faite pour des modules Shinken,
  des packs de configuration Shinken et des plugins de supervision
  Les paquets ont été mis sur les dépôts du projet Kaji.



.. _Shinken: http://www.shinken-monitoring.org
.. _InfluxDB: http://influxdb.com
.. _Grafana: https://grafana.org
.. _Annonce: http://grafana.org/blog/2015/04/20/Grafana-2-Released.html
.. _Nouveautés: http://docs.grafana.org/guides/whats-new-in-v2/
.. _Migration: http://docs.grafana.org/installation/migrating_to2/
.. _SNMPBooster: https://github.com/savoirfairelinux/mod-booster-snmp.git
.. _Finding Spammers & Scammers through Rate Tracking with Python & Redis: https://us.pycon.org/2015/schedule/presentation/383/
.. _Talk (anglais): https://www.youtube.com/watch?v=tIBkiXvEAC0
.. _ici: https://engineering.eventbrite.com/heavy-hitters-in-redis/
.. _Surveil: https://github.com/stackforge/surveil
.. _Meetup Montreal Monitoring: https://www.meetup.com/Montreal-Monitoring
.. _Kaji: https://kaji-project.org
.. _Bansho: https://github.com/stackforge/bansho

