Admin Cloud - Projet Chef d'Oeuvre
# Cahier des charges pour le déploiement d'une application web open-source avec une infrastructure Azure Kubernetes Service (AKS)

## 1. Introduction

L'objectif de ce projet est de mettre en place une infrastructure pour le déploiement automatisé d'une application web open-source (WordPress) sur une infrastructure Azure Kubernetes Service (AKS). Ce projet utilise Terraform pour la gestion de l'infrastructure, Helm pour le déploiement des services, Prometheus/Grafana pour la supervision et GitHub Actions pour l'intégration continue/déploiement continu (CI/CD).

## 2. Description du projet :

### 2.1. Infrastructure AKS

L'infrastructure sera déployée sur Microsoft Azure en utilisant AKS. Il doit inclure :

* Un cluster Kubernetes
* Une stratégie de mise à l'échelle automatique (autoscaling) pour les nœuds du cluster
* Un réseau virtuel Azure pour la connectivité du cluster

### 2.2. Déploiement de l'application

L'application WordPress sera déployée en utilisant Helm, un outil qui simplifie le déploiement et la gestion des applications sur Kubernetes.

### 2.3. Gestion des conteneurs

Les conteneurs seront gérés avec Kubernetes qui fournira l'ordonnancement et la réplication des conteneurs, ainsi que la mise à l'échelle automatique basée sur la charge de travail.

### 2.4. Supervision

Prometheus sera utilisé pour la collecte des métriques et Grafana pour la visualisation et la création de tableaux de bord.

### 2.5. CI/CD

GitHub Actions sera utilisé pour automatiser les tâches de CI/CD, y compris la construction de l'image Docker, le déploiement de l'infrastructure avec Terraform et le déploiement de l'application avec Helm.

## 3. Rôles et responsabilités

L'apprenant sera responsable de :

* La conception et le développement de l'infrastructure as code
* La vérification du code terraform automatisé avant la publication sur le repo (sécurité)
* Le déploiement et la gestion de l'application WordPress en automatique pour les changements de version
* La scalabilité des services (php, WordPress et base de donnée)
* La mise en place de la supervision
* La mise en place de la CI/CD
* La mise en place d'un système de backup multizone de la base de donnée
* Un plan de reprise d'activité après sinistre
* Monitoring du SLA et de la backup

## 4. Livrables

À la fin du projet, l'étudiant devra fournir :

* Le code source de l'infrastructure Terraform
* Le code source du chart Helm pour l'application WordPress
* Les tableaux de bord Grafana
* La configuration de Prometheus
* Le pipeline de CI/CD dans GitHub Actions
* La documentation du projet, y compris l'architecture de l'infrastructure, la description des composants, le processus de déploiement et la gestion de l'application, le plan de reprise d'activité, la configuration de la supervision et du CI/CD.

## 5. Contraintes

*  Le projet doit être réalisé en utilisant les outils et technologies spécifiés.
*  Le projet doit respecter les bonnes pratiques de sécurité, notamment en ce qui concerne la gestion des secrets et l'accès à l'infrastructure et à l'application.

## 6. Critères de réussite

Le projet sera considéré comme réussi si :

* L'infrastructure est correctement déployée sur Azure.
* L'application WordPress est déployée et fonctionnelle.
* La supervision est en place et permet de surveiller l'état et la performance de l'infrastructure et de l'application.
* Le pipeline de CI/CD est fonctionnel et permet de déployer automatiquement des modifications de l'infrastructure et de l'application.
* La documentation du projet est complète et permet de comprendre l'architecture de l'infrastructure, les composants utilisés, le processus de déploiement et de gestion de l'application, la configuration de la supervision et du CI/CD.
