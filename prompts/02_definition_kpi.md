# Prompt 2 – Définir des KPI fiables

## Prompt à adapter

Agis comme un consultant BI spécialisé en banque et Customer Intelligence.

À partir du diagnostic de données validé ci-dessous :
[COLLER LE DIAGNOSTIC VALIDÉ]

Propose un catalogue de 8 à 12 KPI pour un dashboard destiné à la direction de la relation client.

Pour chaque KPI, fournis :
- nom métier ;
- question de pilotage à laquelle il répond ;
- définition précise ;
- formule de calcul ;
- champs nécessaires ;
- niveau de granularité ;
- agrégation à utiliser (COUNT DISTINCT, SUM, AVG, etc.) ;
- filtres possibles ;
- risque de double comptage ;
- contrôle de cohérence ;
- limite d'interprétation.

Classe les KPI par page : Vue exécutive, Customer Intelligence, Crédits & relation client.

Contraintes :
- N'utilise pas SUM sur un solde ou montant de prêt répété sans démontrer que la table est au bon niveau de granularité.
- Distingue nombre de lignes, nombre de transactions et nombre de clients distincts.
- Signale tout KPI impossible à calculer de façon fiable avec les données disponibles.
- Ne propose pas de KPI dont la définition nécessite une donnée absente.

Termine par les 5 KPI prioritaires et justifie leur sélection.

## Vérification humaine
Recalculer au moins 3 KPI indépendamment dans un tableur ou l'outil BI. Documenter les écarts.
