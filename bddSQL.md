### Base de données et MySQL

Base de données : c'est un emsemble qui va permettre de stockées des données.

SGBD : System de gestion de données

ce qui compose une base de données :
```
données et SGBD
```
différents types de SGBD : Oracles, SQL Server, MySQL.

### les données structurés

les bases de données sont découper en plusieurs granularité :

la banque de données : emsemble de bases de données (répertoire).
    base de données
            tables
                lignes d'enregistrement


les taches du SGBD :

le SGBD a plusieurs composants tel que :
- moteur MySQL
- Catalogue
- langages de requêtes
- processeur de requêtes

moteur SQL : réalise toutes les manipulation sur les fichiers physique.
lis les différentes lignes d'enregistrement et nous les retranscrirs de manière compréhensive.

Catalogue : contient la description de la base de données
            les droit utilisateurs (droit d'acces).
            verifie les droit d'acces
            (acces denied si les autorisations sont refusées).

Langages de requêtes: être capable de communiquer le SGBD
                      langages utilisé : SQL

Processeur de requêtes : permet au SGBD  de comprendre la demande dans le langage de requetes.
transforme en la demande en commande pour le moteur SQL.

### realisation d'une requete SQL

1.j'écris ma requete SQL

2.le processeur de requetes le traduit et determine un plan d'execution

3.vérification dans le catalogue si l'utilisateur les droit pour faire toutes les opération nécessaires au plan d'execution.

4.On envoie alors le plan d'execution au moteur SQL qui va manipuler les fichiers et faire les traitement nécessaires

5.On obtient le résultat de la requetes.

### Modèle conceptuel de données
    # modele entité - association:
    - modele conceptuel de données (MCD) c'est a dire une représentation abstraite des données
    - utilise une representation graphique des données

##principe :
- données regroupées en entités et lié par des associations.
#repose sur 3 concept de bases:
- l'entité
- l'attribut
- l'associations

entité : emsemble d'objet similaire pouvant être regroupé

Occurence d'entité: objet discernable parmis d'autre objets.
#(voir cahier pour les exemple)

| produits (entité)|  
|:-------:|
| refprod |
| design  |
| Prix HT |

#ocurences d'entités

| produits      |  produits      |
|:-------------:| :-------------:|
| r0123         | ro124          |
| imprimentes   | ecran          |
| 140e          | 220e           |

## Attribut et identifiants

attribut d'une entité : caractéristique de l'entité
- chaque attribut porte un nom
- chaque attribut possede une valeur dans un domaine

## identifiants (clé) d'une entité :
emsemble minimal d'attribut déterminant de manière unique une occurence dans l'entité.  

| produits(entité)       | Factures(entité)       |
|:---------------------: |:----------------------:|
| refProd (identifiants) | NomFact (identifiants) |
| Design (attribut)      | DatFact (attribut)     |
| Prix HT (attribut)     

## Association : relie plusieur entités (deux ou plus)
- Porte un nom
- peut avoir des attribut.(ex: quantité facturés).
(voir shéma).

## cardinalité d'une association:

###cardinalité d'une association A vis à vis d'une entité E:

Nombre minimum et maximum de fois où une occurence E peut apparaitre dans l'association A.

###cardinalité minimum:
0: il peut exister des occurences de E qui n'apparaisse pas dans A

1: toute occurence de E apparait au moin une fois dans A

### cardinalité maximum:

1: toute occurences de E apparait au plus une fois dans A

n: il peut exister des occurences de E aparaissant plusieur fois dans A.
(voir schéma).

## Exemple de cardinalité :

###Association n,n
