Le projet est propre et bien documenté pour un travail très conséquent. Quelques remarques. Certaines sont sous formes de questions auxquelles vous devriez répondre pour vous-même.

* Diagramme de cas d'utilisation
    * pour les scénarios d'un cas d'utilisation (nominal et alternatifs) les pré-conditions sont toujours communes et donc, les mêmes.
    * la notion de _duel_ n'est pas très claire dans le diagramme

* Diagramme de classes
    * pensez aux conventions de nommage des attributs, les noms de la plupart des attributs _my***_ pourraient être remplacés par _***_
    * les rôles des associations ne devraient pas être publics (ce sont des attributs des classes au final)
    * pourquoi n'y a-t-il pas de lien entre `Moderator` et `UserAccount`. Une classe mère (abstraite si vous préférez) `User` spécialisée en `Moderator` et `SiteParticipant` (ou un autre nom plus approprié) serait plus judicieux.
    * quel est le sens de la classe `Mission` ?
    * quel est le sens de la classe `Proposal` alors qu'on a déjà la classe `Comment` ?
    * pas mal de setters... quid du principe d'encapsulation ?
    * quelques soucis avec les responsabilités des classes : il faudrait vérifier que les méthodes sont dans les bonnes classes. Par exemple `publishComment()` devrait être un méthode de la classe `UserAccount`.

Globalement les diagrammes sont claires et respectent la cohérence entre eux et avec le cahier des charges. Les objectifs sont clairs.
Certaines méthodes du diagramme de classes ne paraissent pas si évidente à définir.
Il faudrait donc être vigilant lors de la phase d'implémentation en Java, votre modèle risque de changer pas mal.
