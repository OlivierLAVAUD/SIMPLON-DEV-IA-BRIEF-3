
[FastAPI](brief3.jpg "FastAPI")

# FastAPI - exposer les données de transactions immobilières via une API

### Contexte
Des users story

### Guide d'installation
Maintenant que vous avez réussi à développer quelques requêtes SQL répondant aux besoins de votre client, vous êtes en charge de développer une API REST en utilisant FastAPI pour exposer les résultats de vos requêtes.
Référentiels

### Ressource(s)
* <a href="https://docs.google.com/spreadsheets/d/110DFqhV0eNhR1mzBkRR5DD6Aey-lgXuTlf3VeSzWD58/edit#gid=0" rel="nofollow">users story</a>
 * <a href="https://www.kaggle.com/datasets/benoitfavier/immobilier-france/data" rel="nofollow">Le dataset Kaggle"</a>


En tant que dev IA, vous serez régulèrement amené à créer une ou plusieurs API Rest dans le cadre de vos projets.
Vous allez réutiliser la base SQLite contenant la data immo comme lors du dernier Brief en ressource.

​

Vous utiliserez:

    FastAPI pour la création de votre API + documentation
    Sqlite3 pour vous connecter à la DB et executer des requêtes SQL
    Swagger pour tester votre API

​


## Ressources 




<a href="https://fastapi.tiangolo.com/fr/tutorial/first-steps/" rel="nofollow">Premiers pas sur FastAPI</a>

<a href="https://fastapi.tiangolo.com/fr/tutorial/path-params/" rel="nofollow">Paramètres de chemin sur FastAPI</a>


Contexte du projet
En tant que DEV IA participant au projet de développement du nouvel outil d'analyse à destination d'une agence immobilière, vous avez été désigné pour créer une BDD PostgreSQL et l'enrichir avec des données immobilières fournies par l'agence.

### Guide d'Installation


This FastAPI application allows you to explore a SQLite database through a set of predefined queries.

   Clone the repository to your local machine:
 ```
	git clone https://github.com/OLV-DEV-IA/fastapi-chinook-explorer.git
```

Install the required dependencies:
```
	pip install -r env_fastAPI.yml
```
Run the FastAPI application:
```
    uvicorn fastAPI:app --reload
```
   Open your browser and go to http://127.0.0.1:8000/docs to access the Swagger documentation and test the API.


<h3>Anaconda Jupyter Notebook</h3>

You can run the python program directly to Jupyter Notebook with the following file:
03-fastAPI/FastAPI.ipynb		
be sure to have the package installed with the  yml environment file yml env_fastAPI.yml

Anaconda prompt
```
pip install -r env_fastAPI.yml
```

### API Endpoints: 

The following API endpoints are available for exploration:
####
1.  #### URI: /revenu_fiscal_moyen/
	Description: Revenu Fiscal Moyen:        
     year (required): The year for the query (format: YYYY).
      city (optional): The city for which the data is requested.

2.  #### URI: /transactions/
    Description: Transactions Sample
    city (optional): The city for which the data is requested.

3. #### URI: /acquisitions/ 
	Description: Acquisitions    
    Parameters:
        city (optional): The city for which the data is requested.
        
4. #### URI: /prix au m2 moyen/
    Description: Prix au m2 Moyen
    Parameters:
        year (required): The year for the query (format: YYYY).
        
5. #### URI: /nombre d'acquisitions de studios dans ma ville/
    Description: Nombre d'Acquisitions de Studios dans ma Ville
        year (required): The year for the query (format: YYYY).
        city (optional): The city for which the data is requested.

6.  #### URI: /repartition des appartements vendus (à Marseille)/
    Description: Répartition des Appartements Vendus (à Marseille)
    Parameters:
        year (required): The year for the query (format: YYYY).
        city (optional): The city for which the data is requested.

7. #### URI: /prix au m2 moyen pour les maisons vendues/
     Description: Prix au m2 Moyen pour les Maisons Vendues     
        year (required): The year for the query (format: YYYY).
        city (optional): The city for which the data is requested.

8. #### URI: /nombre de transactions (tout type confondu) par département/
    Description: Nombre de Transactions (Tout Type Confondu) par Département
    Parameters: None.

9. #### URI: /nombre total de vente d'appartements en 2022 dans toutes les villes/
    Description:Nombre Total de Vente d'Appartements en 2022 dans Toutes les Villes
    Parameters:
        year (required): The year for the query (format: YYYY).


