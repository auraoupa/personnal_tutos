- Attention ne render qu'un seul output, donc bien préciser : 
```python
import warnings
warnings.filterwarnings('ignore')
```

- Ne render pas les équations non plus, donc astuce :
  - impr ecran de l'équation => un fichier image
  - Image pas importée dans un ipynb mais md seulement
  - Pour avoir bonne adresse créer un snippet dans le répertoire
