Nouveautés logicielles
----------------------

* `Shinken`_ : la version 2.2 est sortie le 16 janvier 2015.
  D'importants changements ont été faits depuis la version 2.0 : la lecture
  de la configuration a été retravaillée, corrections de nombreux bugs, amélioration de la
  documentation, ajout d'une fonctionnalité de snapshot lors d'un problème 
  Actuellement, la branche principale est en développement pour la version 2.4 et inclue majoritairement
  du nettoyage de code. La prochaine version de Shinken est prévue pour le 31 mars 2015.
  Les prochaines releases devraient être plus fréquentes par la suite : une tous les trois mois. 
   

* `InfluxDB`_ : InfluxDB est une technologie de base de données du type TSDB (time series database).
  Elle est écrite en Go et correspond parfaitement aux besoins rencontrés en supervision.
  La version 0.9 Beta est sortie en décembre avec la gestion de clustering et de tags.
  Cette version intègre de gros changements dans l'API d'influxdb et dans les concepts.
  La nouveauté sur les tags est très intéressante pour la supervision car elle permet d'ajouter
  des filtres facilement. 

 
* `Grafana`_ : Grafana est une technologie de dashboard et de graphique avec des grandes capacités.
  Elle possède une intégration native avec InfluxDB et Graphite. La dernière version stable est 1.9.0
  Pour la version 2.0, le support d'autres bases de données est prévu : mysql et postresql.
  Une partie d'authentification est aussi attendue.


* `Kaji`_ : Création d'un projet basé sur Shinken, InfluxDB, Grafana, Nagvis et Adagios comme composants principaux.
  L'idée est d'avoir une solution de monitoring fonctionnelle et complètement open-source.
  Des paquets RPM et Deb sont disponibles sur le site de projet et une démonstration est en ligne pour essayer.


.. raw:: html
 
    <br/>
    <br/>
    <br/>
    <br/>
    <br/>
    <br/>
    <br/>
    <br/>
    <br/>



Revue d'évenements
------------------

* Nettoyage de code - Shinken pep8 party.
  Plusieurs employés de Savoir-faire Linux ont pris quelques heures pour passer dans le code du core de Shinken
  afin de le rendre conforme aux normes de style de code en python (PEP8).
  La principale raison de ceci est de pouvoir améliorer la lisibilité du code ainsi que sa qualité.
  Une vérification est maintenant faite par l'outil d'intégration continue (Travis) pour s'assurer que les règles
  de style sont présentes sur chaque commit et chaque pull request.
  Il est prévu de faire un evénement similaire avec Pylint, un outil d'analyse plus en profondeur de code.
  Il permettra de détecter par exemple du code inutilisé ou des problèmes de conceptions.


* Premier meetup Montreal-Monitoring.
  Merci à tous ceux qui ont pu venir pour le premier meetup autour de la supervision.
  L'événement aura été beaucoup plus long que prévu, avec beaucoup de discussion sur les besoins et
  les utilisations de la supervision dans différents métiers.
  Cela nous a permis de rencontrer un public varié, de découvrir d'autres méthodes et de partager
  les nôtres.

* Second meetup Montreal-Monitoring. 
  Merci à ceux qui sont venus. La salle réservée à l'UQAM convenait mieux que la précédente.
  Nous pensons réutiliser les locaux pour le prochain meetup. 
  La `présentation de Kaji`_ était une première, n'hésitez pas à faire des retours
  car elle va devenir la présentation officielle. 
  Les prochains meetup devraient se concentrer davantage sur des exemples métiers : 
  les plugins de supervision représentent une grande richesse. 



Développments SFL
-----------------

* Check_snow_clearance : vérification du déneigement des rues. Les données sont collectées depuis le site 
  infoneige.ca Il sera bientôt disponible sur `Quebec24x7`_

* Supervision applicative : Développement de deux plugins supervisant des serveurs. 
  Le premier permet d'avoir accès aux métriques internes d'apache via une page web (état des workers etc).
  Le second vérifie la connexion à une base redis et récupère quelques métriques (nombre de clients connectés etc)



.. _Shinken: http://www.shinken-monitoring.org
.. _InfluxDB: http://influxdb.com
.. _Grafana: https://grafana.org
.. _Kaji: https://kaji-project.org
.. _page: http://www.meetup.com/Montreal-Monitoring
.. _Quebec24x7: http://quebec247.org
.. _présentation de Kaji: http://savoirfairelinux.github.io/presentations/meetup/2015-03-02/

