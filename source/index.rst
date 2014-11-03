Nouveautés logicielles
----------------------

* Shinken : `Le framework de supervision <http://www.shinken-monitoring.org>`_ a sorti plus tôt cette année une version 2.0 attendu depuis plusieurs mois. De grosses modifications ont été apportées depuis la version 1.4 : le découpage des modules et du coeur de la solution, l'utilisation de HTTP pour les communication inter démon et le changement des chemins d'installation par défaut. Actuellement, la branche principale est en version 2.0.3 et inclue beaucoup de corrections ainsi que des refonte de code sur la phase de lecture de configuration. 

* Adagios : `L'interface de configuration et visualisation <http://adagios.org>`_ a mis en ligne la version 1.6.0 du projet fin aout de cette année. Les principales améliorations sont : le support de l'interface `Multisite <http://mathias-kettner.com/check_mk_introduction.html>`_ (beta), l'intégration native de `Graphite <https://github.com/graphite-project/graphite-web>`_ et le support des préférences utilisateurs. En ce qui concerne la branche principale developpement, une migration de `Django <https://www.djangoproject.com/>`_ version 1.4 vers 1.6 est en cours. 




Développments SFL
-----------------

* Check_hydro_quebec : Nouveau plugin réalisé par l'équipe de supervision. Il récupère les informations disponibles sur le site d'`Hydro Québec <http://pannes.hydroquebec.com/pannes/bilan-interruptions-service/>`_ à propos des pannes en cours dans les différentes provinces du Canada. Il sera bientot disponible sur `Quebec24x7 <http://quebec247.org>`_

* Supervision de génératrices éléctriques : Suite à une demande client, l'équipe de supervision doit récupérer des métriques depuis des groupes électrogènes de marque Cat®. Le début du développement est prévu pour bientôt. 



Événements à venir
------------------

Création d'un Meetup autour de la supervision à Montréal pour bientôt. L'objectif étant de faire le premier avant la fin de cette année. On espère vous voir nombreux. Plus d'information sur la `page <http://www.meetup.com/members/21695861/>`_ de Savoir-faire Linux sur Meetup.


Revue d'évenements
------------------

* MTL Data : Données ouvertes de la ville de Montréal
  Le Mercredi 22 octobre a eut lieu un meetup autour des données ouvertes de la ville ouvertes. Il était question de présenter l'avancement du processus d'ouverture de donnée. Ce qui en est ressorti et que l'ouverture de données est un enjeu avant tout politique et pas technique. En effet, il était question de négociations entre plusieurs acteurs, notamment les fournisseurs (créateurs de données). Ce constat est très intéressant pour la supervision si on le rapproche au projet `quebec247 <http://quebec247.org>`_, car il utilise des données publiques. La problématique d'ouverture seule traité lors de ce meetup est la même en supervision et en analyse de données. L'utlisation en sera par contre différente. 


