# Nos choix de sécurité pour l'application web Champagne & Co
Afin d'assurer une sécurité optimale de l'application web Champagne & Co, nous avons fait le choix de nous réferer aux recommandations du guide de l'ANSSI [Recommandations pour la mise en oeuvre d'un site web : Maîtriser les standards de sécurité côté navigateur.](https://www.ssi.gouv.fr/uploads/2013/05/anssi-guide-recommandations_mise_en_oeuvre_site_web_maitriser_standards_securite_cote_navigateur-v2.0.pdf), de la [checklist OPQUAST](https://checklists.opquast.com/fr/assurance-qualite-web/)ainsi qu'au [guide RGPD de la CNIL.](https://lincnil.github.io/Guide-RGPD-du-developpeur/)

Le maximum des problématiques de sécurité de l'application ont été abordées dès la phase de conception du site Champagne & Co.

---

## 1) Collecte des données personnelles
Notre application web étant une application de vente en ligne, il est nécessaire pour mener à bien certaines finalités du site (achat, livraison...) de collecter des données personnelles auprès des clients du site.
### 1.1) Quelles seront les données personnelles collectées ?
Les données collectées à l'intérieur de l'application web seront réduites au **nécessaire et au minimum.**  
Aucune donnée ne sera récoltée sans le consentement clair et précis de l'utilisateur de l'application.

**Données collectées lors de la phase de création de compte :**
- Genre
- Nom
- Prénom
- Adresse email
- Date de naissance

**Données collectées lors de la phase d'achat :**
- Numéro de la carte bancaire
- Cryptogramme visuel 
- Date d'expiration 


**Données collectées lors de la phase de livraison :**
- Adresse postale 
- Numéro de téléphone

Si l'utilisateur a commandé en tant qu'invité, les données demandées pour la phase de création de compte seton collectées à ce moment 

**Données collectées lors de la phase de facturation :**
- Nom 
- Prénom
- Adresse Postale 
- Numéro de téléphone 
### 1.2) Combien de temps seront stockées les données collectées ?  
Plusieurs phases de stockage des données personnelles sont prévues.  
  
**Effacement immédiat après utilisation :**
- Numéro de la carte bancaire
- Cryptogramme visuel
-  Date d'expiration

**Effacement après un an d'inactivité (pas de connexion - pas d'achats) précédé par une information du client:**
- Adresse email
- Date de naissance 

**Archivage intermédiaire (durée de 10 ans pour les données de facturation) :**
- Genre
- Nom 
- Prénom
- Adresse Postale 
- Numéro de téléphone

Toutes les informations concernant le traitement des données personnelles sont disponibles dans la section **"Confidentialité"** de l'application web Champagne & Co

---

## 2) Utilisation du TLS
Il a été choisi de mettre en oeuvre la solution HTTPS et TLS sur le site Champagne & Co.

La mise en place de HTTPS reposant sur TLS permet d'assurer, à l'application Web Champagne & Co:
- la confidentialité et l'intégrité de toutes les informations échangées
- l'authenticité du serveur contacté.

---
## 3) Politique de sécurisation de l'accés client à l'application web
Notre application web permettant aux utilisateurs de se créer un espace privé, il est nécessaire de définir une politique de sécurité d'accès à cet espace privé. 

### 3.1) Politique de compte privé
1. La création d'un compte privé est possible sans recours à un système d'identification tiers (Réseaux sociaux, google..)
2. La création d'un compte est soumise à un processus de confirmation 
3. L'application propose un mécanisme de prévention des usurpations de compte ou d'identité.
4. Les comptes ouverts en lignes peuvent être fermés en ligne
5. Il est possible de télécharger les contenus personnels via son espace privé
6. Il est possible de se déconnecter de son espace privé

### 3.2) Politique d'authentification par mot de passe
Pour cette partie nous nos réfererons au recommandations de la CNIL [à ce sujet](https://www.cnil.fr/fr/mots-de-passe-une-nouvelle-recommandation-pour-maitriser-sa-securite)

1. Mise en place d'une obligation minimale d'entropie de 80 bits pour la création du mot de passe. Minimum de 12 caractères comprenant des majuscules, des chiffres et des caractères spéciaux à choisir dans une liste d'au moins 37 caractères spéciaux.
2. Mise en place de mécanisme de restriction d'accès au compte
   - Nombre maximal de 3 tentatives dans un délai de 5 minutes
   - Temporisation d'accès au compte d'une heure après 3 échecs
   - Blocage du compte après 6 échecs assorti d'un mécanisme de déblocage.
3. Mécanisme de déblocage avec identification à deux facteurs et blocage du compte au bout de 3 tentatives échouées.




