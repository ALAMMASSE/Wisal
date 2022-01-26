
Requête :

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

Résultats :

<iframe style="width: 80vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#%23Afficher%20les%20sculpteurs%20d%27Auguste%20Rodin%20conserv%C3%A9s%20aux%20Etas-Unis%0ASELECT%20%3Fitem%20%3FitemLabel%20%3FlieuDeconservation%20%3Fcoordonn%C3%A9es%20WHERE%0A%7B%0A%20%20%3Fitem%20wdt%3AP31%20wd%3AQ860861%20.%20%23chercher%20les%20sculteurs%20d%27Auguste%20Rodin%0A%20%20%3Fitem%20wdt%3AP170%20wd%3AQ30755%20.%20%23tableau%20de%20Rodin%0A%20%20%3Fitem%20wdt%3AP17%20wd%3AQ30.%20%23ceux%20conserv%C3%A9s%20aux%20Etats-Unis%0A%20%20OPTIONAL%7B%0A%20%20%3Fitem%20wdt%3AP276%20%3FlieuDeconservation.%20%23lieu%20de%20conservation%0A%20%20%3FlieuDeconservation%20wdt%3AP625%20%3Fcoordonn%C3%A9es.%20%20%20%20%0A%20%20%7D%20%0A%20%20%20%20SERVICE%20wikibase%3Alabel%20%7Bbd%3AserviceParam%20wikibase%3Alanguage%20%22fr%22%7D%20%23%20R%C3%A9cup%C3%A9rer%20les%20labels%20en%20fran%C3%A7ais%0A%7D%0A" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>
