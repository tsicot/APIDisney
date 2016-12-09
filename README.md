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

GET api/personnage/:id

  reponse :
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
  
GET api/films

    reponse :
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

    reponse :
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
  
GET api/acteur/:id
{
  id : nombre
  nom : string
  prenom : string
}
