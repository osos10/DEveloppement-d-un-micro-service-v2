# DEveloppement-d-un-micro-service-v2
# Documentation du Projet

## 1. Introduction
Ce document fournit un aperçu complet des différents microservices et applications Angular développés pour gérer les transactions bancaires, y compris les bénéficiaires et les virements. L'architecture microservices permet une extensibilité, une maintenance simplifiée et une meilleure gestion des ressources.

## 2. Table des Matières
1. Introduction
2. Table des Matières
3. Aperçu des Microservices
   - 3.1. Service des Bénéficiaires
   - 3.2. Service de Virement
   - 3.3. Service de Passerelle
   - 3.4. Service de Configuration
   - 3.5. Service de Découverte
4. Applications Angular
   - 4.1. Composant Bénéficiaire
   - 4.2. Composant Virement
5. Conclusion

## 3. Aperçu des Microservices

### 3.1. Service des Bénéficiaires
Le Service des Bénéficiaires est responsable de la gestion des bénéficiaires. Il permet la création, la récupération, la mise à jour et la suppression de bénéficiaires dans le système.

**Points de terminaison clés :**
- `GET /fullBeneficiaries` : Récupérer tous les bénéficiaires.
- `GET /fullBeneficiaries/{id}` : Récupérer un bénéficiaire par ID.
- `POST /beneficiaries` : Créer un nouveau bénéficiaire.
- `PUT /beneficiaries/{id}` : Mettre à jour un bénéficiaire existant.
- `DELETE /beneficiaries/{id}` : Supprimer un bénéficiaire.

### 3.2. Service de Virement
Le Service de Virement est responsable de la gestion des virements bancaires. Il fournit des fonctionnalités pour créer, récupérer, mettre à jour et supprimer des virements.

**Points de terminaison clés :**
- `GET /fullVirement` : Récupérer tous les virements.
- `GET /fullVirement/{id}` : Récupérer un virement par ID.
- `POST /virements` : Créer un nouveau virement.
- `PUT /virements/{id}` : Mettre à jour un virement existant.
- `DELETE /virements/{id}` : Supprimer un virement.

### 3.3. Service de Passerelle
Le Service de Passerelle agit comme un point d'entrée unique pour toutes les demandes des clients. Il redirige les demandes vers les microservices appropriés et gère les préoccupations transversales telles que la sécurité.

### 3.4. Service de Configuration
Le Service de Configuration gère les propriétés de configuration pour tous les microservices. Il utilise Spring Cloud Config ou Consul Config pour fournir une gestion de configuration centralisée.

### 3.5. Service de Découverte
Le Service de Découverte permet aux microservices de se découvrir dynamiquement. Il utilise Eureka Server ou Consul pour la découverte de services.

## 4. Applications Angular

### 4.1. Composant Bénéficiaire
Le Composant Bénéficiaire affiche une liste de bénéficiaires et leurs détails. Il récupère des données du Service des Bénéficiaires et les présente de manière conviviale.

- **Fonctionnalités :**
  - Affichage des bénéficiaires dans un tableau.
  - Récupération des données via le service HTTP.

### 4.2. Composant Virement
Le Composant Virement affiche les détails d'un virement bancaire spécifique. Il récupère des données du Service de Virement en utilisant l'ID du virement.

- **Fonctionnalités :**
  - Affichage des détails d'un virement, y compris l'ID, le montant, la date et la description.

## 5. Conclusion
Cette documentation fournit un aperçu des microservices et des applications Angular développés. Ces services fonctionnent ensemble pour offrir une solution complète pour la gestion des bénéficiaires et des virements bancaires.
