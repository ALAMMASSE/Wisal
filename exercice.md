
#Afficher les sculpteurs d'Auguste Rodin conservés aux Etas-Unis
SELECT ?item ?itemLabel ?lieuDeconservation ?coordonnées WHERE
{
  ?item wdt:P31 wd:Q860861 . #chercher les sculteurs d'Auguste Rodin
  ?item wdt:P170 wd:Q30755 . #tableau de Rodin
  ?item wdt:P17 wd:Q30. #ceux conservés aux Etats-Unis
  OPTIONAL{
  ?item wdt:P276 ?lieuDeconservation. #lieu de conservation
  ?lieuDeconservation wdt:P625 ?coordonnées.    
  } 
    SERVICE wikibase:label {bd:serviceParam wikibase:language "fr"} # Récupérer les labels en français
}
