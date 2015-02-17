Nouveautés logicielles
----------------------

* `Shinken`_ : la version 2.2 est sortie le 16 janvier 2015.
  D'importants changements ont été apportées fait depuis la version 2.0 : la lecture
  de la configuration a été retravaillé, corrections de nombreux bugs, amélioration de la
  documentation, ajout d'une fonctionnalité de snapshot lors d'un probleme 
  Actuellement, la branche principale est en déloppement pour la version 2.4 et inclue majoritairement
  du nettoyage de code. La prochaine version de Shinken est prévu pour le 31 mars 2015. 
  Les prochaines releases devraient être plus fréquentes par la suite : une tout les trois mois. 
   

* `InfluxDB`_ : InfluxDB est une technologie de base de données de type TSDB (time series database).
  Elle est ecrite en Go et correspond parfaitement aux besoins rencontrés en supervision.
  La version 0.9 est sortie en decembre avec la gestion de clustering et de tags.
  La version 1.0 est en cours de développement et devrait sortir cette année


 
* `Grafana`_ : Grafana est une technologie de dashboard et de graphique avec des grandes capabilités.
  Elle possède une intégration native avec InfluxDB et Graphite. La dernière version stable est 1.9.0
  Pour la version 2.0, le support d'autre bases de données est prévu : mysql et postresql.
  Une partie d'authentification est aussi attendue.



* `Kaji`_ : Création d'un projet basé sur Shinken, InfluxDB, Grafana, Nagvis et Adagios comme composants principaux.
  L'idée est d'avoir une solution de monitoring fonctionnelle completement open-source.
  Des paquets RPM et Deb sont disponible sur le site de projet et une demonstration est en ligne pour essayer.



Événements à venir
------------------

* Montreal Monitoring : La date retenue pour le  à 18h. On espère vous voir nombreux dans
  les locaux de l'UQAM. Plus d'information sur la `page`_ du Meetup. Une présentation de Kaji est prévu pour
  ceux qui souhaiterais en savoir plus sur le sujet. 


Développments SFL
-----------------

* Check_snow_clearance : vérification du déneigement des rue. Les données sont collectés depuis le site 
  infoneige.ca Il sera bientot  disponible sur `Quebec24x7`_

* Supervision applicative : Développemetn de deux plugins supervisant des serveurs. 
  Le premier permet d'avoir acces aux métriques interne d'apache via une page web (état des worker etc).
  Le second vérifie la connection à une base redis et récupère quelques métriques (nombre de client connectés etc)

Revue d'évenements
------------------

* Nettoyage de code - Shinken pep8 party.
  Plusieurs employés de Savoir-faire Linux ont pris le quelques heures pour passer dans le code du core de Shinken
  afin de le rendre conforme aux normes de style de code en python (PEP8).
  La principale raison de ceci est de pouvoir améliorer la lisibilité du code ainsi que sa qualité.
  Une vérification est maintenant faite par l'outil d'intégration continue (Travis) pour s'assurer que les règles
  de style sont présent sur chaque commit et chaque pull request.
  Il est prévu de faire un evénement similaire avec Pylint, un outil d'analyse plus en profondeur de code.
  Il permettra de detecter par exemple du code inutilisé ou des problèmes de conceptions.


* Premier meetup Montreal monitoring.
  Merci à tous ceux qui ont pu venir pour le premier meetup autour de la supervision.
  L'évenement aura été beaucoup plus long que prévu, avec beaucoup de discussion sur les besoins et
  les utilisations de la supervision dans différents métiers.
  Cela nous a permis de rencontrer un public varié, de découvrir d'autres méthodes et de partager
  les notres.
  
.. raw:: html
 
    <br/>
    <br/>
    <br/>
    <br/>
    <br/>
    <br/>
    <br/>


.. _Shinken: http://www.shinken-monitoring.org
.. _InfluxDB: http://influxdb.com
.. _Grafana: https://grafana.org
.. _Kaji: https://kaji-project.org
.. _page: http://www.meetup.com/Montreal-Monitoring
.. _Quebec24x7: http://quebec247.org

