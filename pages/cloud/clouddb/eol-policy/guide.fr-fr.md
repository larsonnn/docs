---
title: 'Politique de fin de vie des bases de données managées'
slug: managed-db-life-cycle-policy
section: 'Ressources techniques'
---

**Dernière mise à jour le 07/01/2022**

## Objectif

Les bases de données managées OVHcloud proposent plusieurs Systèmes de Gestion de Bases de Données (SGBD), comme MySQL ou PostgreSQL. Chaque version de ces logiciels atteint, à un moment ou à un autre, sa fin de vente puis sa fin de support. Elle peut ensuite être mise à jour par nos services ou cesser d'être fonctionnelle ("fin de vie"). Nous souhaitons ici vous permettre de comprendre le cycle de vie des bases de données managées OVHcloud, afin de mieux anticiper et préparer leurs évolutions.

**Découvrez ici la politique de fin de vie des bases de données managées par OVHcloud.**

## Prérequis

Disposer d'une ou plusieurs des offres suivantes:

- Un [Hébergement web](https://www.ovhcloud.com/fr/web-hosting/) comprenant des bases de données.
- Un pack de base de données [Start SQL](https://www.ovhcloud.com/fr/web-hosting/options/start-sql/).
- Un serveur [SQL privé](https://www.ovhcloud.com/fr/web-hosting/options/).
- Un serveur [Cloud Databases](https://www.ovh.com/fr/cloud-databases/).

## En pratique

### Produits couverts

Les produits couverts par cette politique de fin de vie sont :

- Les services Cloud Databases Publics, instances SGBD dédiées joignables via le réseau public ([voir les annonces](https://docs.ovh.com/fr/clouddb/clouddb-eos-eol/)).

- Les services Cloud Databases Web Hosting (également connues sous le nom de services SQLPrivé), instances SGBD dédiées joignables via le réseau Web Hosting ([voir les annonces](https://docs.ovh.com/fr/hosting/sql_eos_eol)).

- Les services SharedSQL Web Hosting, bases de données MySQL joignables via le réseau Web Hosting ([voir les annonces](https://docs.ovh.com/fr/hosting/sql_eos_eol)).

### Définitions et lignes directrices de la politique de fin de vie

![timeline](images/ovh.eol.policy.timeline.png)

EOL = End Of Life

#### Annonce de fin de vie ("End of Life" - EOL)

C'est la publication des dates de fin de vente et de fin de support. En règle générale, OVHcloud respectera un délai de 90 jours entre l'annonce d'une fin de vie et son application.

#### Fin de vente ("End of Sale")

Le produit concerné ne peut plus être commandé au-delà de cette date. Comme annoncé précédemment, cette règle s'applique au minimum 90 jours après l'annonce de fin de vie.

#### Fin de support ("End of Support")

La date jusqu'à laquelle le client peut bénéficier d’une assistance pour le produit selon les modalités du contrat de service ou les conditions générales de la garantie.
Après cette date, le produit ne fait plus l'objet de services d'assistance et est considéré comme obsolète.
S'applique au minimum 6 mois après l'annonce de fin de vie.

#### **Période d'obsolescence**

Elle survient après la fin de support.

Quand un service de bases de données managées OVHcloud devient obsolète, il peut entrer dans les deux cas listés ci-après.
Comme il peut y avoir des conséquences sur votre service, une notification vous sera envoyée par e-mail au minimum un mois avant la période d'obsolescence.

**Mise à jour majeure du service**

Votre service reste actif et nous mettons à jour son SGBD vers une nouvelle version majeure.
Ce type de mise à jour peut induire des comportements non souhaités sur vos applications. C'est pourquoi nous conseillons aux clients d'anticiper sur les changements de versions de leur base de données et de ne pas attendre la fin de support.

**Cessation du service**

Au lieu de mettre à jour le SGBD de votre service vers la prochaine version majeure disponible, nous pouvons décider de cesser le service, pour plusieurs raisons telles que:

- La mise à jour est déconseillée par l'éditeur du SGBD.

- Le développement sur le SGBD a pris fin.

La cessation peut être faite de deux façons, selon les cas:

- Nous arrêtons le renouvellement du service. Dans ce cas, le service sera suspendu à la fin de la période d'engagement.

- Nous suspendons le service et vous recréditons du surplus payé.

## Aller plus loin

Échangez avec notre communauté d'utilisateurs sur <https://community.ovh.com>.