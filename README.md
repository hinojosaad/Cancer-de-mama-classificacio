# Càncer-de-mama-classificació

La meva soluciò al repte proposat per Nuwe a la  web https://nuwe.io/challenge/repte-4-models-de-classificacio

## Descripció del repte
El repte consisteix en construir un model predictiu a partir del conjunt de dates _train_ que conte les medicions de mostres de tumors mamaris. Adicionalment el _train_ conté una columna amb el diagnotic del tumor:

* 0 Benigne
* 1 Maligne


Adicionalent es proporciona l'arxiu _test_ que conte medicions de mostres de tomesr mamaris amb diagnostic desconegut. El repte consta de tres objetius

* Comprendre el conjunt de dades i netejar-lo (si cal).

* Construir models de classificació per predir si el tipus de càncer és maligne o benigne, variable "diagnosi" 0 benigne i 1 maligne.

* També ajustar els hiperparàmetres i comparar les mètriques davaluació de diversos algorismes de classificació.

## Arxius del repositori

* Repte_classificacio.ipynb: Notebook amb el códi en python de la solució proposada al repte
* predictions.csv: Arxiu que conté les prediccions de diagnosi pels valors de les mostres en _test_ fetas pel millor model trobat 


## Models utilizats i resultats
Es van fer us de cinc models de classificació de la llibreria _sklearn_ combinats amb un reescalat _RobustScaler_ amb les seguents resultats amb la metrica f1 abans i desprès de fixar parameters
|                            | **f1_macro** | **tuned f1_macro** |
|----------------------------|--------------|--------------------|
| **Decission Tree**         | .9193        | .9497              |
| **Random Forest**          | .9575        | .9622              |
| **K Neighbors**            | .9497        | .9665              |
| **Support Vector Machine** | .9691        | **.9762**          |
| **Gradient Boosting**      | .9503        | .9666              |
