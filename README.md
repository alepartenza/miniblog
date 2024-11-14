### Progetto di Test: **API per Mini Blog con Categorie e Tag**

#### Obiettivo del Progetto
Sviluppare un backend Django RESTful per un mini blog che offra API per gestire post, categorie e tag. Il progetto serve a valutare la capacità di creare e strutturare un’applicazione Django che fornisca un set di endpoint per CRUD (Create, Read, Update, Delete), relazioni tra modelli e filtri di base.

#### Specifiche del Progetto

1. **Modelli**
   - **Category**: rappresenta una categoria di post.
     - Campi:
       - `nome`: nome della categoria (univoco).
       - `descrizione`: descrizione opzionale della categoria.
   - **Tag**: rappresenta un tag associabile ai post.
     - Campi:
       - `nome`: nome del tag (univoco).
   - **Post**: rappresenta i post del blog.
     - Campi:
       - `titolo`: titolo del post.
       - `contenuto`: contenuto del post.
       - `data_creazione`: data e ora della creazione.
       - `categoria`: relazione a chiave esterna con `Category`.
       - `tags`: relazione molti-a-molti con `Tag`.

2. **Endpoint API**
   - **Category**
     - **GET /api/categories/** - Elenco di tutte le categorie.
     - **GET /api/categories/<id>/** - Dettagli di una categoria specifica.
   - **Tag**
     - **GET /api/tags/** - Elenco di tutti i tag.
     - **GET /api/tags/<id>/** - Dettagli di un tag specifico.
   - **Post**
     - **GET /api/posts/** - Elenco di tutti i post, con possibilità di filtrare per categoria o tag.
     - **GET /api/posts/<id>/** - Dettagli di un post specifico, inclusi categoria e tag associati.
     - **POST /api/posts/** - Crea un nuovo post.
     - **PUT /api/posts/<id>/** - Modifica un post esistente.
     - **DELETE /api/posts/<id>/** - Cancella un post.

3. **Requisiti Tecnici**
   - Utilizzare **Django** e **Django REST framework**.
   - Non è necessaria alcuna autenticazione per l’accesso agli endpoint.
   - Creare i filtri di base per ottenere i post in base a `categoria` o `tag`.
