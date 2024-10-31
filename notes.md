# Notes

## Subaccounts dans goHighLevel

### Que sont les subaccounts?

Les subaccounts sont un outils pour mieux gérer plusieurs clients. Ils permettent de créer des comptes à partir du compte de base.

### Pourquoi sont-ils essentiels?

Comme nous avons plusieurs clients avec des besoins différents et uniques, avoir des subaccounts permet de passer d'un à l'autre sans avoir à changer de plateforme. 

De plus, chaque subaccount peut être personnalisé pour le client, comme le logo, les couleurs et le nom de domaine.

Aussi, grâce aux subaccounts, il est facile de contrôler les accès de chaque client. Il est aussi possible de donner des permissions différentes à chaque personne d'une équipe de travail, pour que le data sensible reste caché.

De plus, avec les subaccounts, il est plus facile de partager des rapports, tableaux de bord et autre avec les clients ou les membres de l'équipe de travail.

### Comment créer un subaccount dans goHighLevel

Créer un subaccount dans goHighLevel semble très facile, voici les étapes à suivre:

1. Se connecter à notre compte goHighLevel et aller dans la section **paramètres**. 

2. Cliquer sur **Sub Accounts** et ensuite sur **Créer un nouveau Sub Account**.

3. Remplir toutes les informations demandées.

4. Choisir le niveau d'accès pour le client et les membres de l'équipe de travail. Il est possible de donner tous les accès ou donner des accès restreints.

5. Cliquer sur **"Créer Le Sub Account**. Le client a maintenant sont propre CRM giHighLevel.

### Les meilleures pratiques de gestions de subaccounts

- **Rester organisé**

- **Établir des attentes claires**

- **Revoir régulièrement les niveaux d'accès**

- **Former les clients**

- **Rester à jour**

### Conclusion

Créer des subaccounts semble une bonne façon de gérer plusieurs clients sans avoir à jongler avec plusieurs plateforme. De plus, le tout semble personnalisable selon les besoins du client. Aussi, la plateforme semble très facile à utiliser.

## Introduction à Make.com

Il s'agit d'une plateforme d'automatisation qui est *user friendly*. Grâce à cette plateforme, il est possible de créer des scénarios qui automatisent des tâches.

Make est utile pour automatiser des tâches répétitives comme l'envoie de données, les interaction entre plusieurs outils en ligne à jour de base de données.

Voici les étapes pour créer un scénario par exemple pour *scraper* des données via Phantombuster et ensuite les envoyer automatiquement à goHighLevel.

1. Créer un compte et aller au tableau de bord dans Make.com

2. Créer un nouveau scénario
    1. Cliquer sur le bouton **Créer un nouveau scénario**
    
    2. Ajouter Webhook comme premier module.

3. Configurer le module Webhook

    1. Ajout d'un Webhook, sélectionner **Custom Webhook**

    2. Créer un Webhook personnalisé: cliquer sur **Ajouter**

    3. Copier l'URL générer par Make

    4. Cliquer sur **OK** pour valider la création du module

4. Configurer Phantombuster pour *scraper* les données

    (Phantombuster est un outil de scraping permettant d'extraire des données provenant du web automatiquement)

    1. Se connecter à Phantombuster

    2. Choisir l'agent de *scraping*

    3. Configurer l'agent choisi: suivre les étapes pour configurer l'agent en fonction des besoins

    4. Ajouter l'URL du Webhook Make.com

    5. Tester l'exécution

5. Analyser les données JSON reçues

    (Les données envoyées par Phantombuster sont dans le format JSON)

    1. Ajouter un module JSON Parse

    2. Configurer le module: Choisir les données JSON reçues via Webhook en tant qu'entrées

    3. Tester le module, vérifier que le JSON est bien interprété

6. Utiliser un Routeur pour générer plusieurs chemins
    
    1. Ajouter le module Routeur

    2. Configurer les chemins

    3. Configurer les filtres

7. Valider les adresses courriel (optionnel)

    (Si le scénario inclut des adresses courriel, il est possible de les valider avant de les envoyer à goHighLevel)
    
    1. Ajouter le module ValidEmail

    2. Configurer le module

8. Envoyer les données à goHighLevel via HTTP

    1. Ajouter le module HTTP Make a Request

    2. Configurer la requête HTTP: 
        
        - Méthode: POST
        - URL: coller l'URL de l'API goHighLevel
        - Headers: ajouter les headers nécessaires
        - Body: utiliser les données *parsées* pour construire le *body* de la requête

    3. Tester la requête

## Comment entraîner ChatGPT avec notre propre data

Il y a des trous dans les connaissances de ChatGPT.

Il est possible de combler les trous.

### Comment utiliser les instructions personnalisées de ChatGPT

Les instructions personnalisées permettent de donner des informations de context et spécifier le format de réponse de ChatGPT.

#### Comment ajouter des instructions personnalisées

1. Dans ChatGPT, cliquer sur l'icône de profil 

2. Cliquer sur **Personnaliser ChatGPT**

3. Entrer les instructions sur ce que vous voulez que ChatGPT sache et comment vous voulez qu'il vous réponde

4. S'assurer qu'**Activer pour les nouveaux clavardages** soit activer

5. Enregistrer

Le désavantage de cela est qu'il n'est seulement possible d'avoir une paire d'instructions personnalisées, donc si vous avez besoins d'instructions différentes, il faut désactiver en décochant le bouton **Activer pour les nouveaux clavardages**.

### Comment construire son propre ChatGPT personnalisé

Contrairement aux instructions personnalisées, il est possible de créer plusieurs *chatbots*. 

*À noter que la construction d'un GPT personnalisé requiert ChatGPT Plus ou un compte d'entreprise.*

1. Dans ChatGPt, cliquer sur l'icône de profil

2. Cliquer sur **Mes GPT**

3. Cliquer sur le bouton **Créer**

4. Entrer les directives dans la boîte de texte, converser jusqu'à obtention de résultats désirés

5. Cliquer sur **Configurer** pour ajouter des configurations avancées

6. Cliquer sur **Créer**

7. Cliquer sur **Mettre à jour**

Vous verrez maintenant votre nouveau GPT dans la barre de gauche. Votre GPT est maintenant prêt à converser!

### Comment créer son propre *chatbot* avec Zapier

Le problème avec le fait d'utiliser seulement les instructions personnalisées est que le *chatbot* ne communique pas avec les autres applications.

C'est ici qu'entre en compte *Zapier Chatbots* et *Zapier Central*, ils permettent de lier l'IA avec l'automatisation.

#### Comment utiliser Zapier Chatbots

Il est facile de construire notre propre *chatbot* avec *Zapier Chatbots*. Il est possible de donné un URL au *chatbot* ou de l'intégrer directement au site web. Puisqu'il s'agit de Zapier, c'est connecté à des milliers d'autres applications.

Voici comment créer et partager un *Zapier Chatbot*:

1. Aller à l'adresse:  https://zapier.com/app/chatbots

2. Cliquer sur **Create** ou sur **Build your first chatbot**

3. Donner un nom à votre **chatbot** et cliquer sur **Create**

4. Connecter votre compte OpenAI avec Zapier

5. Cliquer sur **Save changes**

6. Depuis le **Chatbots builder**, cliquer sur **Instructions**

7. Donner les directives et ressources de connaissances au **chatbot**

8. Cliquer sur **Save changes**

Maintenant il ne reste qu'à configurer le *workflow* automatisé.

1. Depuis le *chatbots builder*, cliquer sur **Actions**

2. Choisir le type d'action désirée

3. Suivre les instructions pour finir de configurer l'action choisie

Il est possible à tout moment de cliquer sur le lien public (en haut de l'aperçu) pour tester.

Une fois le *chatbot* prêt à être mis en ligne, vous pouvez le partager à l'aide du lien mentionné plus tôt ou avec *Zapier Interface*.

#### Comment utiliser *Zapier Central*

*Zapier Central* sert à entraîner les assistants IA pour supporter le reste de votre travail.

1. Aller sur https://central.zapier.com et se créer un compte

2. Cliquer sur **New assistant**

3. Depuis la page **bot builder**, cliquer sur Untitled et entrer le nom de votre nouvel assistant

4. Cliquer sur **Behaviors** et ensuite cliquer sur **Create behavior**

5. Cliquer sur **Instant actions** et ensuite cliquer sur **Add action**

6. Cliquer sur **Data sources** et ensuite cliquer sur **Add data source**

Il est possible d'interagir avec votre *bot* pour s'assurer qu'il fonctionne comme désiré.

## Wordpress

### Variables globales

Presque tout l data généré par WordPress peut être trouvé dans un variable globale.

Pour avoir accès à une variable dans votre code, vous devez globaliser la variable avec `global $variable;`

#### Dans la variable *Loop*

Voici la liste des variables accessibles à l'intérieur d'une boucle, contenant des informations sur le *post* qui est en cours de traitement:

- `$post`: L'objet du *post* actuel

- `$posts`: utilisé par quelques fonctions natives, à ne pas mélangé avec `$query->$posts`.

- `$authordata`: l'objet de l'auteur du *post* actuel

- `$currentday` (string): jour où le *post* actuel a été publié 

- `$currentmonth` (string): mois où le *post* actuel a été publié

- `$page` (int): la page où le *post* actuel est consulté

- `$pages` (array): le contenu des pages du *post* actuel

- `$multipage` (boolean): `true` si le *post* actuel a plusieurs pages, `false` si il n'a qu'une seule page, relié à `$pages`

- `$more` (boolean): sert à savoir si WordPress doit forcer le *tag* `<!--more-->`

- `$numpages` (int): retourne le nombre de page du *post* actuel, relié à `$pages`

#### Booléen de détection de navigateur


- `$is_iphone`: Safari sur iPhone

- `$is_chrome`: Google Chrome

- `$is_safari`: Safari

- `$is_NS4`: Netscape 4

- `$is_opera`: Opera

- `$is_macIE`: Mac Internet Explorer

- `$is_winIE`: Windows Internet Explorer

- `$is_gecko`: FireFox

- `$is_lynx`: Lynx

- `$is_IE`: Internet Explorer

- `$is_edge`: Microsoft Edge

#### Booléen de détection de serveur web

Ces variables contiennent du data sur le serveur web sur lequel WordPress fonctionne.

- `$is_apache` (boolean): Apache HTTP Server

- `$is_IIS` (boolean): Microsoft Internet Information Services (IIS)

- `$is_iis7` (boolean): Microsoft Internet Information Services (IIS) v7.x

- `$is_nginx` (boolean): Nginx web server

#### Variables de version

- `$wp_version` (string): la version installée de WordPress

- `$wp_db_version` (int): le numéro de version de la base de données

- `$tinymce_version` (string): la version installée de TinyMCE

- `$manifest_version` (string): la version de la cache manifest

- `$required_php_version` (string): la version nécessaire de PHP pour ce WordPress

- `$required_mysql_version` (string): la version nécessaire de MySQL pour ce WordPress installé

#### Misc

- `$super_admins` (array): un tableau des ID des utilisateurs qui sont des super Admins

- `$wp_query` (object): la globale de l'instance de la classe WP_Query

- `$wp_rewrite` (object): la globale de l'instance de la classe WP_Rewrite

- `$wp` (object): Tla globale de l'instance de la classe WP

- `$wpdb` (object): la globale de l'instance de la classe wpdb

- `$wp_locale` (object): la globale de l'instance de la classe WP_Locale

- `$wp_admin_bar` (object): la globale de l'instance de la classe WP_Admin_Bar

- `$wp_roles` (object): la globale de l'instance de la classe WP_Roles

- `$wp_meta_boxes` (array): objet contenant toutes les metaboxes enregistrées, incluant leur Id, arguments, fonction de callback et titre

- `$wp_registered_sidebars` (array)

- `$wp_registered_widgets` (array)

- `$wp_registered_widget_controls` (array)

- `$wp_registered_widget_updates` (array)

#### Globales Administratives

- `$pagenow` (string): Used in wp-admin. 
See also get_current_screen() for the WordPress Admin Screen API.

- `$post_type` (string): Used in wp-admin

- `$allowedposttags` (array)

- `$allowedtags` (array)

- `$menu` (array)

### wp-config.php

Il s'agit d,un des fichier les plus importants dans l'installation de WordPress, il se situe à la racine du dossier WordPress et contient les détails de configuration du site.

#### Configurer les paramètres de base de données

Ouvrir le fichier `wp-config-sample.php` dans un éditeur de texte.

##### wp-config-sample.php par défaut

Voici un exemple du fichier `wp-config-sample.php`, les valeurs sont des exemples pour indiquer quoi faire.

```php
// ** MySQL settings - You can get this info from your web host ** //

/** The name of the database for WordPress */
define( 'DB_NAME', 'database_name_here' );

/** MySQL database username */
define( 'DB_USER', 'username_here' );

/** MySQL database password */
define( 'DB_PASSWORD', 'password_here' );

/** MySQL hostname */
define( 'DB_HOST', 'localhost' );
```

##### Configurer le nom de la base de données

*Remplacer 'database_name_here' par le nom de votre base de données*

```php
define( 'DB_NAME', 'database_name_here' ); // Example MySQL database name
```

##### Configurer l'utilisateur de la base de données

```php
define( 'DB_USER', 'username_here' ); // Example MySQL username
```

##### Configurer le mot de passe de la base de données

```php
define( 'DB_PASSWORD', 'password_here' ); // Example MySQL password
```

##### Configurer l'hôte de la base de données

Il est possible d'avoir besoin de spécifier le port.

```php
define( 'DB_HOST', 'localhost' ); // Example MySQL Database host
```

*Il est possible de ne pas avoir besoin de changer l'hôte.*

###### Port alternatif de MySQL

Si votre hôte utilise un port alternatif pour votre base de données, vous devrez changer la valeur de **DB_HOST** dans `wp-config.php`.

Pour localhost: 

```php
define( 'DB_HOST', '127.0.0.1:3307' );
or
define( 'DB_HOST', 'localhost:3307' );
```

Pour un server spécifique: 

```php
define( 'DB_HOST', 'mysql.example.com:3307' );
```

*Remplacer le nombre **3307** dans le code pour celui fourni par votre hôte.*

###### *Sockets* ou *Pipes* MySQL

Si votre hôte utilise des *sockets* ou *pipes* Unix, vous devrez changer la valeur de **DB_HOST** dans le fichier `wp-config.php`.

```php
define( 'DB_HOST', '127.0.0.1:/var/run/mysqld/mysqld.sock' );
// or define( 'DB_HOST', 'localhost:/var/run/mysqld/mysqld.sock' );
// or define( 'DB_HOST', 'example.tld:/var/run/mysqld/mysqld.sock' );
```
*Remplacer la chaîne de caractères `/var/run/mysqld/mysqld.stock` par l'information du **socket** ou **pipe** fourni par votre hôte.*

##### Configurer le jeu de caractères de la base de données

La valeur par défaut de **DB_CHARSET** est 'utf8', ce qui est souvent la meilleure option.

```php
define( 'DB_CHARSET', 'utf8' );
```

##### Classement de la base de données

**DB_COLLATE** existe pour désigner le classement de la base de données. Dans la plupart des cas, la valeur devrait rester vide (null), pour que le classement de la base de données soit automatiquement assigné à MySQL selon le jeu de caractères spécifié avec **DB_CHARSET**. Il peut être nécessaire de changer la valeur de **BB_COLLATE** lorsque la langue d'affichage ne correspond pas au jeu de caractères.

La valeur par défaut de WordPress: 

```php
define( 'DB_COLLATE', '' );
```

Classement général UTF-8 Unicode: 

```php
define( 'DB_COLLATE', 'utf8_general_ci' );
```

##### Clés de sécurité

Vous n'avez pas à vous rappeler des clés, donc il peut être une bonne idée d'utiliser un générateur comme [celui-ci](https://api.wordpress.org/secret-key/1.1/salt/). Il est possible de les changer à tout moment pour invalider tous les *cookies* existant, tous les utilisateurs devront alors se reconnecter.

Exemple (ne pas utiliser ces clés):

```php
define( 'AUTH_KEY',         't`DK%X:>xy|e-Z(BXb/f(Ur`8#~UzUQG-^_Cs_GHs5U-&Wb?pgn^p8(2@}IcnCa|' );
define( 'SECURE_AUTH_KEY',  'D&ovlU#|CvJ##uNq}bel+^MFtT&.b9{UvR]g%ixsXhGlRJ7q!h}XWdEC[BOKXssj' );
define( 'LOGGED_IN_KEY',    'MGKi8Br(&{H*~&0s;{k0<S(O:+f#WM+q|npJ-+P;RDKT:~jrmgj#/-,[hOBk!ry^' );
define( 'NONCE_KEY',        'FIsAsXJKL5ZlQo)iD-pt??eUbdc{_Cn<4!d~yqz))&B D?AwK%)+)F2aNwI|siOe' );
define( 'AUTH_SALT',        '7T-!^i!0,w)L#JK@pc2{8XE[DenYI^BVf{L:jvF,hf}zBf883td6D;Vcy8,S)-&G' );
define( 'SECURE_AUTH_SALT', 'I6`V|mDZq21-J|ihb u^q0F }F_NUcy`l,=obGtq*p#Ybe4a31R,r=|n#=]@]c #' );
define( 'LOGGED_IN_SALT',   'w<$4c$Hmd%/*]`Oom>(hdXW|0M=X={we6;Mpvtg+V.o<$|#_}qG(GaVDEsn,~*4i' );
define( 'NONCE_SALT',       'a|#h{c5|P &xWs4IZ20c2&%4!c(/uG}W:mAvy<I44`jAbup]t=]V<`}.py(wTP%%' );
```

### Metadata

#### Survol

L'**API Metadata** une une façon simple et standardisée d'aller chercher et de manipuler du metadata de plusieurs type d'objet WordPress.

Le metadata d'un objet est représenté par une simple paire clé-valeur.

Les objets peuvent avoir plusieurs entrées de metadata qui partagent la même clé et diffèrent seulement de valeur.

#### Fonction possibles

- [add_metadata()](https://developer.wordpress.org/reference/functions/add_metadata/)

- [delete_metadata()](https://developer.wordpress.org/reference/functions/delete_metadata/)

- [get_metadata()](https://developer.wordpress.org/reference/functions/get_metadata/)

- [update_metadata()](https://developer.wordpress.org/reference/functions/update_metadata/)

#### Exigences de base de données

Cette fonction assume qu'une table MySQL dédiée existe pour le `$meta_type` spécifié. Quelques `$meta_type` désiré ne vienne pas avec les tables pré-installées de WordPress, il faut donc les créer manuellement.

##### Tables par défaut meta

En assumant le préfixe `wp_`, les table meta incluses de WordPress sont:

- `wp_commentmeta`: Metadata pour des commentaires spécifiques.

- `wp_postmeta`: Metadata pour les pages, les posts et tous autres types post.

- `wp_usermeta`: Metadata pour les utilisateurs.

##### Structure de la table meta

Pour enregistrer des données pour les types meta non inclus dans la précédente liste, une nouvelle table doit être créée. Toutes les tables meta requiert 4 colonnes.

- meta_id – BIGINT(20): unsigned, auto_increment, not null, primary key.

- object_id – BIGINT(20): unsigned, not null.

Remplacer *object* avec le nom du contenu qui sera utilisé, au singulier.

Même si cette colonne est utilisé comme une clé étrangère, elle ne devrait pas être définie comme tel.

- meta_key – VARCHAR(255): La clé de votre meta data personnalisé.

- meta_value – LONGTEXT: La valeur de votre meta data personnalisé.

#### Fichier source

L'**API Metadata** se trouve dans `wp-includes/meta.php`

## GitHub

### Qu'est-ce Git?

Un système de contrôle de version gratuit et *open source*.

### Qu'est-ce que le contrôle de version?

La gestion des changements dans des documents, des programme d'ordinateur, de gros sites web et autres collections d'informations.

### Commandes Git

- clone

- add
 
- commit

- push

- pull

## GraphQL

### Introduction

GraphQL est un langage de requête pour les API et un runtime côté serveur permettant d'exécuter des requêtes avec un système de types pour les données. Il est indépendant de toute base de données spécifique et repose sur le code et les données existants.

### Requêtes et mutations

#### Champs

À son plus simple, GraphQL sert à demander des champs spécifiques sur des objets.

Exemple d'opération: 

```graphql
{
    hero{
        name
    }
}
```

Réponse: 

```graphql
{
  "data": {
    "hero": {
      "name": "R2-D2"
    }
  }
}
```

Il est aussi possible que les champs se réfèrent à des objets. Dans ce cas, il faut faire un sous-sélection des champs de cet objet.

Exemple d'opération:

```graphql
{
  hero {
    name
    # Queries can have comments!
    friends {
      name
    }
  }
}
```

Réponse:

```graphql
{
  "data": {
    "hero": {
      "name": "R2-D2",
      "friends": [
        {
          "name": "Luke Skywalker"
        },
        {
          "name": "Han Solo"
        },
        {
          "name": "Leia Organa"
        }
      ]
    }
  }
}
```

#### Arguments

Si il s'agissait seulement de traverser des objets et leurs champs, GraphQl serait déjà un langage très utile pour la récupération de données. Mais, lorsque l'on ajoute la capacité de passer des arguments aux champs, les choses deviennent encore plus intéressantes.

Exemple d'opération:

```graphql
{
  human(id: "1000") {
    name
    height
  }
}
```

Réponse:

```graphql
{
  "data": {
    "human": {
      "name": "Luke Skywalker",
      "height": 1.72
    }
  }
}
```

Grâce à GraphQL, il est possible de donner des arguments champs et objets imbriqués.

Exemple d'opération:

```graphql
{
  human(id: "1000") {
    name
    height(unit: FOOT)
  }
}
```

Réponse:

```graphql
{
  "data": {
    "human": {
      "name": "Luke Skywalker",
      "height": 5.6430448
    }
  }
}
```

Les arguments dans GraphQL peuvent être de plusieurs types, y compris des types d'énumération, qui limitent les valeurs possibles à un ensemble défini (comme METER ou FOOT pour des unités de longueur). GraphQL offre des types prédéfinis, mais les serveurs peuvent aussi créer des types personnalisés, à condition qu'ils puissent être sérialisés dans le format de transport choisi.


#### Alias

Il est possible de faire des alias pour faire plusieurs requêtes sur le même champs avec des arguments différents.

Exemple d'opération:

```graphql
{
  empireHero: hero(episode: EMPIRE) {
    name
  }
  jediHero: hero(episode: JEDI) {
    name
  }
}
```

Réponse:

```graphql
{
  "data": {
    "empireHero": {
      "name": "Luke Skywalker"
    },
    "jediHero": {
      "name": "R2-D2"
    }
  }
}
```

Dans l'exemple précédent, les deux champs `hero` auraient entré en conflit, mais puisque les alias permettent d'avoir des noms différents, il est possible d'avoir les deux dans la même requête.

#### Fragments

Si par exemple, il y avait une page relativement compliquée dans notre app, qui nous laisserais comparer deux héros un à côté de l'autre, avec leur amis. Il pourrait s,agir d'une requête plutôt compliquée.

C'est pour cette raison que GraphQL inclus les unités réutilisables appelé *fragments*. Les fragments nous laisse construire un ensemble de champs, ensuite il suffit de les inclure où nécessaire dans nos requêtes.

Exemple d'opération:

```graphql
{
  leftComparison: hero(episode: EMPIRE) {
    ...comparisonFields
  }
  rightComparison: hero(episode: JEDI) {
    ...comparisonFields
  }
}
​
fragment comparisonFields on Character {
  name
  appearsIn
  friends {
    name
  }
}
```

Réponse:

```graphql
{
  "data": {
    "leftComparison": {
      "name": "Luke Skywalker",
      "appearsIn": [
        "NEWHOPE",
        "EMPIRE",
        "JEDI"
      ],
      "friends": [
        {
          "name": "Han Solo"
        },
        {
          "name": "Leia Organa"
        },
        {
          "name": "C-3PO"
        },
        {
          "name": "R2-D2"
        }
      ]
    },
    "rightComparison": {
      "name": "R2-D2",
      "appearsIn": [
        "NEWHOPE",
        "EMPIRE",
        "JEDI"
      ],
      "friends": [
        {
          "name": "Luke Skywalker"
        },
        {
          "name": "Han Solo"
        },
        {
          "name": "Leia Organa"
        }
      ]
    }
  }
}
```

Comme il est possible de voir, la requête aurait facilement pu être répétitive si les champs avaient été répétés. Le concept de fragments est souvent utilisé pour séparer des requête contant du data d'application complexe, en plus petits morceaux.

#### Utiliser des variables à l'intérieur de fragments

Il est possible que les fragments aient accès aux variables déclarées dans la requête ou la mutation.

Exemple d'opération:

```graphql
query HeroComparison($first: Int = 3) {
  leftComparison: hero(episode: EMPIRE) {
    ...comparisonFields
  }
  rightComparison: hero(episode: JEDI) {
    ...comparisonFields
  }
}
​
fragment comparisonFields on Character {
  name
  friendsConnection(first: $first) {
    totalCount
    edges {
      node {
        name
      }
    }
  }
}
```

Réponse:

```graphql
{
  "data": {
    "leftComparison": {
      "name": "Luke Skywalker",
      "friendsConnection": {
        "totalCount": 4,
        "edges": [
          {
            "node": {
              "name": "Han Solo"
            }
          },
          {
            "node": {
              "name": "Leia Organa"
            }
          },
          {
            "node": {
              "name": "C-3PO"
            }
          }
        ]
      }
    },
    "rightComparison": {
      "name": "R2-D2",
      "friendsConnection": {
        "totalCount": 3,
        "edges": [
          {
            "node": {
              "name": "Luke Skywalker"
            }
          },
          {
            "node": {
              "name": "Han Solo"
            }
          },
          {
            "node": {
              "name": "Leia Organa"
            }
          }
        ]
      }
    }
  }
}
```

#### Nom d'opération

Dans plusieurs des exemples précédents, nous utilisions la syntaxe raccourcie où nous ne mettions pas le mot clé `query` et le nom de la requête, mais dans une application de production, il est utile de les utiliser pour éviter les ambiguïtés.

Voici un exemple qui inclut le mot clé `query` comme type d'opération et `HeroNameAndFriends` comme nom d'opération:

```graphql
query HeroNameAndFriends {
  hero {
    name
    friends {
      name
    }
  }
}
```

Réponse:

```graphql
{
  "data": {
    "hero": {
      "name": "R2-D2",
      "friends": [
        {
          "name": "Luke Skywalker"
        },
        {
          "name": "Han Solo"
        },
        {
          "name": "Leia Organa"
        }
      ]
    }
  }
}
```

Le **type d'opération** est soit *query*, *mutation* ou *subscription* et décrit le type d'opération voulue. Le type d'opération est requis à moins d'utiliser la syntaxe raccourcie.

Le **nom d'opération** est un nom explicite et significatif pour l'opération. Il n'est pas requis, sauf pour des documents multi-opération, mais il est tout de même recommandé de l'utiliser puisqu'il est plus facile de déboguer. Lorsqu'il y a un problème, il est facile d'identifier la requête par nom que d'essayer de trouver la requête à partir de son contenu. C'est l'équivalent d'un nom de fonction dans un langage de programmation. 

#### Variables

Jusqu'à présent, nous avons écrit tout nos arguments à l'intérieur de la chaîne de requête. Cependant, pour la plupart des applications, les champs d'arguments sont dynamiques, par exemple, il pourrait y avoir un *dropdown* qui nous laisse choisir un épisode, une barre de recherche ou un ensemble de filtres.

Lorsque nous utilisons des variables, il est important de suivre ces 3 étapes:

1. Remplacer la valeur statique dans la requête par `$variableName`

2. Déclarer `$variableName` comme étant une des variables acceptées dans la requête

3. Passer `variableName: value` dans dictionnaire de variables, souvent un JSON

Exemple d'opération:

```graphql
query HeroNameAndFriends($episode: Episode) {
  hero(episode: $episode) {
    name
    friends {
      name
    }
  }
}
```

Variables:

```graphql
{
  "episode": "JEDI"
}
```

Réponse:

```graphql
{
  "data": {
    "hero": {
      "name": "R2-D2",
      "friends": [
        {
          "name": "Luke Skywalker"
        },
        {
          "name": "Han Solo"
        },
        {
          "name": "Leia Organa"
        }
      ]
    }
  }
}
```

##### Définitions de variables

Les définitions de variable sont la partie ressemblant à `($episode: Episode)` dans la requête précédente. Elles fonctionnent de la même façon que des arguments pour une fonction dans un langage autre de programmation. Il s'agit d'une liste de toutes les variables, avec le préfixe `$` suivi par leur type, dans ce cas `Episode`.

Toutes les variables déclarées dans GraphQL doivent être de type scalaire, énumération ou objets d'entrée. Donc si nous voulons passer un objet complexe dans un champ, nous devons savoir type d'entrée est compatible avec le serveur.

Les définitions de variable peuvent être optionnelles ou requises, dans ce cas, puisqu'il n'y a pas de `!` après le type `Episode`, elle était optionnelle. Cependant, si le champ dans lequel on passe la variable requiert un argument non null, la variable aussi doit être requise.

##### Variables par défaut

Il est possible de donner un valeur par défaut à une variable, il suffit d'ajouter la valeur par défaut après la déclaration du type.

Exemple d'opération:

```graphql
query HeroNameAndFriends($episode: Episode = JEDI) {
  hero(episode: $episode) {
    name
    friends {
      name
    }
  }
}
```

Lorsqu'une valeur par défaut est donnée, il est possible de ne pas fournir de variable dans la requête, si une variable des passée dans le dictionnaire de variable, la valeur par défaut sera alors écrasée.

#### Directives

Il est possible de devoir changer la structure et forme de la requête en utilisant des variables. 

Exemple d'opération:

```graphql
query Hero($episode: Episode, $withFriends: Boolean!) {
  hero(episode: $episode) {
    name
    friends @include(if: $withFriends) {
      name
    }
  }
}
```

Variables:

```graphql
{
  "episode": "JEDI",
  "withFriends": false
}
```

Réponse:

```graphql
{
  "data": {
    "hero": {
      "name": "R2-D2"
    }
  }
}
```

Exemple d'opération:

```graphql
query Hero($episode: Episode, $withFriends: Boolean!) {
  hero(episode: $episode) {
    name
    friends @include(if: $withFriends) {
      name
    }
  }
}
```

Variables:

```graphql
{
  "episode": "JEDI",
  "withFriends": true
}
```

Réponse:

```graphql
{
  "data": {
    "hero": {
      "name": "R2-D2",
      "friends": [
        {
          "name": "Luke Skywalker"
        },
        {
          "name": "Han Solo"
        },
        {
          "name": "Leia Organa"
        }
      ]
    }
  }
}
```

Voici les directives possibles:

- `@include(if: Booléen)` Inclus seulement si le résultat de l'argument est `true`

- `@skip(if: Booléen)` Passe ce champ si l'argument est `true`

Les directives sont utiles pour éviter les situations où il faudrait modifier manuellement la requête pour ajouter ou enlever des morceaux.

#### Mutations

La plupart du temps où nous parlons de GraphQL, nous parlons de la récupération de données, mais n'importe quelle plateforme de données complète a besoin d'avoir une façon de modifier les données du côté serveur aussi.

Dans REST, une requête peut parfois produire des effets secondaires sur le serveur. Cependant, il est recommandé par convention d'éviter d'utiliser les requêtes `GET` pour modifier des données. GraphQl fonctionne de façon similaire, techniquement une requête pourrait être implémentée pour écrire des données. Cependant, il est bon d'établir une convention disant qu'une requête qui écrit des données devrait être explicitement envoyée par mutation.

Tout comme dans une requête, si le champ de mutation retourne un objet,il est possible de demandé pour les champs imbriqués. Cela peut s'avérer utile pour récupérer le nouvel état d'un objet après une modification.

Voici un exemple simple de mutation:

```graphql
mutation CreateReviewForEpisode($ep: Episode!, $review: ReviewInput!) {
  createReview(episode: $ep, review: $review) {
    stars
    commentary
  }
}
```

Variables:

```graphql
{
  "ep": "JEDI",
  "review": {
    "stars": 5,
    "commentary": "This is a great movie!"
  }
}
```

Réponse:

```graphql
{
  "data": {
    "createReview": {
      "stars": 5,
      "commentary": "This is a great movie!"
    }
  }
}
```

Remarquez que le champ createReview retourne les champs stars et commentary de l'avis nouvellement créé. Cela est particulièrement utile lors de la modification de données existantes. Par exemple, lors de l'incrémentation d'un champ, on peut modifier et interroger la nouvelle valeur du champ en une seule requête.

##### Plusieurs champs dans les mutations

Tout comme une requête, une mutation peut contenir  plusieurs champs. Il y a une distinction importante entre les requête et le mutations, autre que le nom: 

**Cependant, contrairement aux requêtes, les champs des mutations sont exécutés en série, et non en parallèle.**

Cela signifie que si nous envoyons 2 mutations d'`incrementCredits` en une seule requête, la première finira assurément avant que la deuxième commence, ce qui assure que nous ne seront pas dans une course contre nous-même.

#### Fragments en ligne

Comme dans de nombreux systèmes de types, les schémas GraphQL permettent de définir des interfaces et des types unions.

Lorsqu’on interroge un champ renvoyant une interface ou un type union dans GraphQL, on utilise des fragments en ligne pour accéder aux données du type concret sous-jacent. Cela permet de structurer les réponses en fonction du type spécifique des données récupérées.

Exemple d'opération:

```graphql
query HeroForEpisode($ep: Episode!) {
  hero(episode: $ep) {
    name
    ... on Droid {
      primaryFunction
    }
    ... on Human {
      height
    }
  }
}
```

Variables:

```graphql
{
  "ep": "JEDI"
}
```

Réponse:

```graphql
{
  "data": {
    "hero": {
      "name": "R2-D2",
      "primaryFunction": "Astromech"
    }
  }
}
```

Dans cette requête, le champ `hero` retourne le type de `Character`, qui peut être soit `Human` ou `Droid` en fonction de l'argument `Episode`. Lors de la sélection directe, on peut uniquement demander des champs présents dans l'interface `Character`, comme `name`.

Pour accéder à un champ d’un type concret dans GraphQL, il faut utiliser un fragment en ligne avec une condition de type. Par exemple, si un fragment est marqué comme `... on Droid`, le champ `primaryFunction` ne sera exécuté que si le `Character` renvoyé par `hero` est de type `Droid`. De même pour le champ `height` pour le type `Human`.

Les fragments nommés peuvent également être utilisés de la même manière, car un fragment nommé est toujours associé à un type.

#### Champs Meta

Étant donné qu'il existe des situations où vous ne savez pas quel type vous recevrez du service GraphQL, vous avez besoin d'un moyen pour déterminer comment gérer ces données côté client. GraphQL vous permet de demander `__typename`, un champ méta, à tout moment dans une requête pour obtenir le nom du type d'objet à ce moment-là.

Exemple d'opération:

```graphql
{
  search(text: "an") {
    __typename
    ... on Human {
      name
    }
    ... on Droid {
      name
    }
    ... on Starship {
      name
    }
  }
}
```

Réponse:

```graphql
{
  "data": {
    "search": [
      {
        "__typename": "Human",
        "name": "Han Solo"
      },
      {
        "__typename": "Human",
        "name": "Leia Organa"
      },
      {
        "__typename": "Starship",
        "name": "TIE Advanced x1"
      }
    ]
  }
}
```

Dans la requête précédente, `search` retourne un type union qui peut être une des trois options. Il serait impossible de différencier les types du clients sans le champ `__typename`.

### Schémas et Types

#### Système de type

Le langage de requête GraphQL sélectionne des champs sur des objets.

Exemple d'opération:

```graphql
{
  hero {
    name
    appearsIn
  }
}
```

Réponse:

```graphql
{
  "data": {
    "hero": {
      "name": "R2-D2",
      "appearsIn": [
        "NEWHOPE",
        "EMPIRE",
        "JEDI"
      ]
    }
  }
}
```

1. Nous commençons avec l'objet spécial à la racine
2. Nous sélectionnons le champ `hero` sur celui-ci
3. Nous sélectionnons les champs `name` et `appearIn` sur l'objet retourné par `hero`

La structure d'une requête GraphQL correspond étroitement au résultat, ce qui permet de prédire ce que la requête retournera sans nécessairement connaître le serveur. Cependant, il est utile d'avoir la bonne description de ce que nous allons demander.

#### Type de langage

Les services de GraphQL peuvent être écrit dans n'importe quel langage. 

#### Types d'objets et Champs

La composante la plus simple d'un schémas GraphQL est les types d'objets, qui représente les sortes d'objet que l'on peut aller chercher avec le service et ses champs. 

Exemple:

```graphql
type Character {
  name: String!
  appearsIn: [Episode!]!
}
```

Le langage est facile à lire, mais voici le vocabulaire:

- `Character` est un type d'objet GraphQL, ce qui veut dire que c'est un type avec des champs. La plupart des types dans votre schéma seront des types d'objets.

- `name` et `appearsIn` sont des champs du type `Character`. Ce qui veut dire que `name` et `appearsIn` sont les seuls champs qui peuvent apparaître dans n'importe quel partie d'une requête GraphQL qui opère sur le type `Character`.

- `String` est un des types scalaires intégré.

- `String!`signifie que le champ n'est pas *nullable*, ce qui signifie que le service GraphQL promet de toujours donner une valeur lorsque ce champ est interrogé.

- `[Episode!]!` représente un *array* d'objet `Episode`. Puisqu'il est aussi non *nullable*, on peut toujours s'attendre à un *array* (avec 0 ou plus d'items) lorsqu'on interroge le champ `appearsIn`. Puisqu' `Episode!` est aussi non *nullable*, nous pouvons toujours nous attendre à chaque item de l'*array* soit un objet `Episode`.

#### Type scalaire

Un type d'objet GraphQL a un nom et des champs, mais à un moment, ces champs doivent devenir des données concrètes. C'est là que les types scalaires entre en compte: ils représentent les feuilles de la requête.

Dans la requête suivante, les champs `name` et `appearsIn` se résoudront à des types scalaires. Les types scalaires fournissent les valeurs finales dans une requête GraphQL, représentant des données simples, comme des *string*, *int* ou *bool*.

Exemple d'opération:

```graphql
{
  hero {
    name
    appearsIn
  }
}
```

Réponse:

```graphql
{
  "data": {
    "hero": {
      "name": "R2-D2",
      "appearsIn": [
        "NEWHOPE",
        "EMPIRE",
        "JEDI"
      ]
    }
  }
}
```

Dans la plupart des services d'implémentation GraphQL, il est aussi possible de spécifier un type scalaire personnalisé. Par exemple, on pourrait définir un type `Date`:

```graphql
scalar Date
```

Il revient ensuite à notre implémentation de définir comment ce type doit être sérialisé, désérialisé et validé. Par exemple, on pourrait spécifier que le type `Date` doit toujours être sérialisé sous forme de timestamp entier, et le client doit savoir qu'il peut s'attendre à ce format pour tous les champs de date.

#### Type énumération

Aussi appelé *Enums*, les types énumération sont une sorte de scalaire spécial qui sont restreint à un ensemble de valeur particulier. Ça nous permet de:

1. Valider que les arguments de ce type font partie des valeurs permises
2. Communiquer à l'aide du système type qu'un champ aura toujours une valeur définie parmi un ensemble

Voici de quoi peut avoir l'air une définition d'*enum* dans le langage de schéma GraphQL:

```graphql
enum Episode {
  NEWHOPE
  EMPIRE
  JEDI
}
```

#### Listes et non null

Les types objet, enums et scalaires sont les seuls sorte de type pouvant être défini dans GraphQL. Cependant, lorsque les types sont utilisés dans d'autres parties du schéma, ou dans les déclarations de variables de requête, il est possible d'ajouter des *type modifier* additionnel qui affecte la validation de ces valeurs. 

Voici un exemple:

```graphql
type Character {
  name: String!
  appearsIn: [Episode]!
}
```

Dans cet exemple, nous utilisons un type `String` en précisant qu'il doit être non null en ajoutant `!` après le nom du type. 

Le modificateur de type non-null peut aussi être utiliser lors de la définition des arguments pour un champ.

Si un élément censé être non null retourne la valeur null, le serveur GraphQL retourne alors une erreur.

Exemple d'opération:

```graphql
query DroidById($id: ID!) {
  droid(id: $id) {
    name
  }
}
```

Variables:

```graphql
{
  "id": null
}
```

Réponse:

```graphql
{
  "errors": [
    {
      "message": "Variable \"$id\" of non-null type \"ID!\" must not be null.",
      "locations": [
        {
          "line": 1,
          "column": 17
        }
      ]
    }
  ]
}
```

Les listes fonctionnent de façon relativement similaire il est possible d,utiliser un modificateur de type pour marqué un type en `List`, ce qui signifie que ce champs retournera un *array* de ce type. On l'écrit en mettant `[` avant et `]` après.Ça fonctionne de la même façon pour les arguments, où l'étape de validation va s'attendre à recevoir un *array* de cette valeur.

Le modificateur non-null et List peuvent être combinés. Par exemple, il est possible d'avoir une liste de *strings* non-null:

```graphql
myField: [String!]
```

Ce qui veut dire que la liste en elle-même peut être null, mais ses items ne peuvent pas l'être. Par exemple, en JSON:

```graphql
myField: null // valide
myField: [] // valide
myField: ["a", "b"] // valide
myField: ["a", null, "b"] // erreur
```

Maintenant, si nous définissons une liste non-null de *strings*:

```graphql
myField: [String]!
```

Ce qui veut dire que la liste ne peut être null, mais ses items peuvent l'être. Par exemple en JSON:

```graphql
myField: null // erreur
myField: [] // valide
myField: ["a", "b"] // valide
myField: ["a", null, "b"] // valider
```

Il est possible d'imbriquer le nombre désiré de modificateur list et non-null.