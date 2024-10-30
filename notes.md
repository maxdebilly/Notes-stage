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