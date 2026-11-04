# Projet_tutor-

KUZMENKO Anton
FAVRE Awa Marie Paulette
Wu Mingzhe
SAKKAKI seyed Mohammadreza


Sujet: Système d'alerte intelligent doté d'une fonction de mise à jour automatique pour un commerce.


Introduction

Voici l'idée divisée en deux parties (la "vitrine" et les "coulisses") :

Côté "Vitrine" : L'idée métier (Ce que ça apporte au commerçant)

Problématique: Y aura-t-il suffisamment de produits pour répondre à la
demande future des clients ?

En entrée : Mettre à jour la situation du jour au système.
(exemple : "il nous reste 5 paquets de café")

En sortie : Le système nous répond en nous prédisant le besoin. 
(exemple:"Alerte ! Selon les prévisions de ventes, le stock actuel risque d'être 
insuffisant pour les trois prochains jours.".)



Côté "Coulisses" : Nous allons surtout nous intéresser à la chaîne d’automatisation 

Le projet (MLOps): Le système permettra d'automatiser le réentraînement et
la mise à jour du modèle, après vérification de ses performances. Dès que
l'on ajoute les nouvelles données de vente de la semaine, cela déclenche un
"interrupteur automatique" en arrière-plan. Le système va lui-même lire les
données, réapprendre, et remplacer l'ancienne IA par la nouvelle version plus 
performante. Le tout sans aucune intervention humaine.










Projet détaillé:

SmartStock AI — Version simplifiée avec MLOps


1. L'application web

Une plateforme destinée aux petits commerces (cafés, épiceries, etc.) qui permet de :

- Gérer les produits et les stocks.
- Prédire les ventes futures grâce au Machine Learning.
- Recevoir des alertes en cas de risque de rupture de stock.
- Obtenir des suggestions de réapprovisionnement.

2. La partie Machine Learning

Un modèle développé avec Python et Scikit-learn analyse l'historique des ventes pour prédire la demande future.

Par exemple, si un magasin possède 20 unités d'un produit et que le modèle prévoit 30 ventes la semaine suivante, le système signale un risque de rupture.

3. La partie MLOps simplifiée

Le fonctionnement serait le suivant :

1. Le commerçant ajoute de nouvelles données de vente (CSV).
2. Un processus automatique réentraîne le modèle.
3. Le nouveau modèle est évalué et comparé à l'ancien.
4. Si les résultats sont satisfaisants, le modèle est mis à jour automatiquement.
5. L'application utilise le modèle validé pour ses prochaines prédictions.

Cela permet de démontrer un véritable pipeline MLOps sans devoir construire une infrastructure industrielle complexe.

4. Technologies

Python, Pandas, Scikit-learn, Flask, HTML, CSS, JavaScript, SQL et GitHub Actions.

Docker pourrait être ajouté si nécessaire.


En résumé: ce projet conserve l'idée de prédiction intelligente des stocks et ajoute une automatisation du réentraînement et de la mise à jour du modèle, sans multiplier les fonctionnalités techniques. Nous prévoyons d'utiliser un jeu de données public contenant un historique des ventes pour entraîner et évaluer notre modèle.
