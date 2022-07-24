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
* preddictions.csv: Arxiu que conté les prediccions de diagnosi pels valors de les mostres en _test_ fetas pel millor model trobat 


## Models utilizats i resultats
Se utilizaron cuatro modelos distintos de la librería _sklearn_ combinados con un reescalado _RobustScaler_ obteniendo el siguiente desempeño antes y después de afinar parámetros

|                            | **f1_macro** | **tuned f1_macro** |
|----------------------------|--------------|--------------------|
| **Random Forest**          | .7519        | .7619              |
| **K Neighbors**            | .7682        | .7761              |
| **Support Vector Machine** | .7501        | **.7822**          |
| **Gradient Boosting**      | .7421        | .7621              |
