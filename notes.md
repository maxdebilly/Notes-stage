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

1. Se connecter à notre compte goHighLevel et aller dans la section "paramètres". 

2. Cliquer sur "Sub Accounts" et ensuite sur "Créer un nouveau Sub Account".

3. Remplir toutes les informations demandées.

4. Choisir le niveau d'accès pour le client et les membres de l'équipe de travail. Il est possible de donner tous les accès ou donner des accès restreints.

5. Cliquer sur "Créer Le Sub Account". Le client a maintenant sont propre CRM giHighLevel.

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

1. **Créer un compte et aller au tableau de bord dans Make.com**

2. **Créer un nouveau scénario**
    1. Cliquer sur le bouton "Créer un nouveau scénario
    
    2. Ajouter Webhook comme premier module.

3. **Configurer le module Webhook**

    1. Ajout d'un Webhook, sélectionner "Custom Webhook"

    2. Créer un Webhook personnalisé: cliquer sur "Ajouter"

    3. Copier l'URL générer par Make

    4. Cliquer sur "OK" pour valider la création du module

4. **Configurer Phantombuster pour *scraper* les données** 

    (Phantombuster est un outil de scraping permettant d'extraire des données provenant du web automatiquement)

    1. Se connecter à Phantombuster

    2. Choisir l'agent de *scraping*

    3. Configurer l'agent choisi: suivre les étapes pour configurer l'agent en fonction des besoins

    4. Ajouter l'URL du Webhook Make.com

    5. Tester l'exécution

5. **Analyser les données JSON reçues**

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
