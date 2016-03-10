# Projet Architecture Distribuée

L'idée de ce projet est de mettre en place un système
de communication entre un serveur REST et un client.

La partie serveur se charge de récupérer les requêtes et exécute l'une des actions suivantes:


| Method         | Action                                                         |
| :------------- | :------------------------------------------------------------- |
| GET            | Renvoie la liste des villes                                    |
| GET            | Renvoie la ville dont le nom est passé en paramètre            |
| POST           | Renvoie la ville présente aux coordonnées passées en paramètre |
| POST           | Renvoie la ville proche des coordonnées passées en paramètres  |
| PUT            | Ajoute la ville spécifiée                                      |
| DELETE         | Supprime la ville spécifiée                                    |


**La proximitée des villes s'effectue de la manière suivante:**

```
Pour chaque ville enregistrée
    on calcule la distance entre ces deux villes
    Si distance < 10 Alors
        on ajoute cette ville à la liste de villes à renvoyer
    Fin Si
Fin Pour
```
