# APIDisney

Personnage
  -> Nom
  -> Film
  -> Genre
  -> Alignement
  -> Acteur
Film
  -> Nom
  -> Personnage
  -> Realisateur
Acteur
  -> Nom
  -> Prénom



GET api/personnage/:id
  {
    id : nombre
    nom : string
    film : string
    genre : string
    alignement : string
    acteur : 
      {
        id : nombre
        nom : string
      }
  }

POST api/personnage
  Content-Type: application/json
    {
    id : nombre
    nom : string
    film : string
    genre : string
    alignement : string
    acteur_id : nombre
    }
  Reponse :
    header location
  
POST api/personnages
  Content-Type: application/json
  [
    {
    id : nombre
    nom : string
    film : string
    genre : string
    alignement : string
    acteur_id : nombre
    }
  ]
  
  Reponse :
    header location

GET api/films
  [
    {
       id : nombre
      nom : string
      realisateur : string
      année : nombre
      personnages : 
      [
        {
           id : nombre
           nom : string
           film : string
           genre : string
           alignement : string
           acteur : 
           {
              id : nombre
              nom : string
           }
        }
      ]
    }
  ]
  
GET api/film/:id
  {
     id : nombre
    nom : string
    realisateur : string
    personnages : 
    [
      {
         id : nombre
         nom : string
         film : string
         genre : string
         alignement : string
         acteur : 
         {
            id : nombre
            nom : string
         }
      }
    ]
  }
  
POST api/film
  Content-Type: application/json
    nom : string
    realisateur : string
    [
      personnages_id : nombre
    ]
  Reponse :
    header location
  
GET api/acteur/:id
{
  id : nombre
  nom : string
  prenom : string
}

POST api/acteur
  Content-Type: application/json
    {
    nom : string
    prenom :string
    }
  Reponse :
    header location
    
POST api/acteurs
  Content-Type: application/json
    [
      {
      nom : string
      prenom :string
      }
    ]
  Reponse :
    header location
