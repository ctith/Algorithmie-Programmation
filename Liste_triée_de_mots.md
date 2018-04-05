# Recherche dans une liste triée de mots (2005-2006)

## 1) Lire le fichier texte01.txt et construire une liste avec tous ces mots. (4 points)
Input :
```python
def liste_de_mots(file):
    texte = open(file, "r")
    mot = []

    for ligne in texte :
        # append() : sert à ajouter un élément à la fin d'une liste
        mot.append(ligne.replace("\n", ""))

    return mot

liste = liste_de_mots("texte01.txt")
```
Output :
```python
['ABONDANCE', 'ABORD', 'ACCUSE', 'ACHATS', 'ACTUELLE', 'AERIENNES', 'AGRICULTURE', 'AILLEURS', 'AINSI', 'AJOUTE', 'AJUSTEMENT', 'ALLAIT', 'ALLOUE', 'AMERICAIN', 'AMERICAINE', 'AMERICAINS', 'AMOINDRIR', 'AN', 'ANALYSE', 'ANCIENNE', 'ANDREAS', 'ANGLO-SAXON', 'ANNEES', 'ANNONCANT', 'ANNONCE', 'ANORMALEMENT', 'ANS', 'ANTICIPATIONS', 'ANTICIPENT', 'ANXIETE', 'AOUT', 'APPELLENT', 'APPLIQUER', 'APPUYER', 'APRES', 'ARMES', 'ASSOCIATIONS', 'ASSUMER', 'ASSURANCE', 'ASSURANCE-MALADIE', 'ASSURANCE-SANTE', 'ATTENDAIENT', 'ATTENDENT', 'ATTENTES', 'AU', 'AUCUNE', 'AUGMENTATIONS', 'AUGMENTE', 'AUGMENTERA', 'AUPRES', 'AUQUEL', 'AURA', 'AURAIT', 'AUSSI', 'AUTEUR', 'AUTOMOBILES', 'AUTRE', 'AUTRES', 'AUX', 'AVAIENT', 'AVANT', 'AVANTAGE', 'AVANTAGES', 'AVEC', 'AVOIR', 'BAISSE', 'BANQUE', 'BANQUES', 'BANQUIERS', 'BAS', 'BATIS', 'BEAUCOUP', 'BEIGE', 'BIEN', 'BLOQUES', 'BON', 'BONDISSENT', 'BOOK', 'BOUGE', 'BRUXELLOIS', 'BUDGET', 'CAMPAGNE', 'CAPABLES', 'CAPACITE', 'CAPITAL', 'CAS', 'CATEGORIE', 'CE', 'CELA', 'CELLE', 'CELLE-CI', 'CELLES', 'CELUI-CI', 'CENTRALE', 'CENTRALES', 'CENTRAUX', 'CERTES', 'CES', 'CET', 'CETTE', 'CEUX', 'CEUX-CI', 'CHAMBRE', 'CHANGER', 'CHIFFRE', 'CHIMIE', 'CHOMAGE', 'CHOMEURS', 'CIRCULATION', 'CITOYENS', 'CLASSE', 'CLES', 'COMME', 'COMMERCE', 'COMMUNAUTE', 'COMPAGNIES', 'COMPARATIF', 'COMPENSER', 'COMPLEMENTAIRES', 'COMPOSANTS', 'COMPREND', 'COMPTE', 'CONCERNANT', 'CONCLUT', 'CONFIANCE', 'CONSERVATISME', 'CONSERVER', 'CONSOMMATEURS', 'CONTAGION', 'CONTENIR', 'CONTINENTAL', 'CONTINENTAUX', 'CONTINUER', 'CONTRARIE', 'CONTRE', 'CONTROLER', 'CONVAINCRE', 'COTISATIONS', 'COTISER', 'COUCHES', 'COURS', 'COUTS', 'COUVERTURE', 'CRAINTES', 'CREATEURS', 'CREATION', 'CREDIBILITE', 'CRISE', 'CROISSANCE', 'CROISSANTE', 'DANS', 'DE', 'DEBUT', 'DECIDER', 'DEFICIT', 'DEJA', 'DELE', 'DELITEMENT', 'DELPHI', 'DEMANDE', 'DEMANDER', 'DEPENS', 'DEPENSES', 'DEPUIS', 'DERAPAGE', 'DERNIERES', 'DERNIERS', 'DES', 'DEUX', 'DEVALUATIONS', 'DEVANT', 'DEVELOPPEMENT', 'DEVENU', 'DEVENUE', 'DEVIENT', 'DEVRAIENT', 'DEVRAIT', 'DIFFERENTS', 'DIFFICILE', 'DIRECTEMENT', 'DIRECTEUR', 'DIRECTEURS', 'DIRIGEE', 'DISTINGUE', 'DOCUMENTS', 'DOIVENT-ILS', 'DOLLARS', 'DOMAINE', 'DONC', 'DONNE', 'DONT', 'DU', 'DUMPING', 'DURABLE', 'DURER', 'DYNAMISME', 'ECHELLE', 'ECONOMIE', 'ECONOMIES', 'ECONOMIQUE', 'ECONOMISTES', 'ECROULER', 'EFFET', 'EFFICACE', 'EFFICACES', 'EFFORTS', 'ELEMENTS', 'ELEVE', 'ELEVEE', 'ELEVES', 'ELLE', 'ELLES', 'EMPECHER', 'EMPLOI', 'EMPRUNTS', 'EN', 'ENCADRES', 'ENERGIE', 'ENQUETE', 'ENSEMBLE', 'ENTRENT', 'ENTREPRISE', 'ENTREPRISES', 'ENVIRONNEMENT', 'EQUITABLE', 'EROSION', 'ESSAYER', 'EST', 'ESTIME', 'ESTIMENT', 'ET', 'ETAIENT', 'ETAT', 'ETATS', 'ETATS-UNIS', 'ETE', 'ETRE', 'ETUDE', 'EURO', 'EUROPE', 'EUROPEEN', 'EUROPEENS', 'EVENTAIL', 'EVITER', 'EVOLUTION', 'EXISTE', 'EXPERTS', 'EXPLIQUE', 'EXPLIQUENT', 'FABRICANTS', 'FABRIQUAIT', 'FACTEUR', 'FACTEURS', 'FAIBLE', 'FAIBLES', 'FAILLITE', 'FAIRE', 'FAIT', 'FALLOIR', 'FAMEUSE', 'FAUDRAIT', 'FAUT', 'FAUTE', 'FAVEUR', 'FAVORABLES', 'FED', 'FEDERAL', 'FEDERALE', 'FIABLES', 'FIERE', 'FIGURE', 'FILIALE', 'FIN', 'FINANCE', 'FINANCIERE', 'FINANCIERES', 'FINANCIERS', 'FINIR', 'FISCAL', 'FLEXIBILITE', 'FOIS', 'FORCE', 'FORTE', 'FORTES', 'FORTS', 'FRAIS', 'FRANCAISE', 'FUTURE', 'GARANTIES', 'GAUCHE', 'GEANT', 'GENERALISE', 'GENERE', 'GENERER', 'GENEREUSES', 'GLOBALEMENT', 'GRAND', 'GRANDE', 'GRANDS', 'GRAVE', 'GROS', 'GROSSE', 'GROUPES', 'HAUSSE', 'HAUT', 'HOEFERT', 'HORIZONS', 'IDEE', 'IL', 'ILS', 'IMPORTANTES', 'IMPORTATIONS', 'IMPRESSIONNANT', 'IMPRESSIONNANTE', 'IMPRUDENTS', 'INCONVENIENTS', 'INDEMNISATION', 'INDEMNITES', 'INDISPENSABLE', 'INDUSTRIELLES', 'INDUSTRIELS', 'INEFFICACE', 'INEFFICACES', 'INEQUITABLE', 'INFLATION', 'INFLEXIBILITE', 'INQUIETER', 'INSECURITE', 'INSTABLE', 'INSTITUT', 'INTENTIONS', 'INTERDICTION', 'INTERDIT', 'INTERET', 'INTERROGE-T-IL', 'INTERROGES', 'INVERSEE', 'INVESTISSEURS', 'JEU', 'JEUDI', 'JOUAIT', 'JOUE', 'LA', 'LAA', 'LANCANT', 'LANCEMENT', 'LAQUELLE', 'LARGE', 'LARGES', 'LE', 'LEGEREMENT', 'LENTS', 'LEQUEL', 'LES', 'LEUR', 'LIBERTE', 'LIBRE', 'LICENCIEMENT', 'LICENCIEMENTS', 'LIMITEE', 'LIMITER', 'LIMITES', 'LIQUIDITES', 'LOIN', 'LONG', 'LONGS', 'LORS', 'LOUIS', 'LUI', 'LUI-MEME', 'MAIS', 'MAJORITE', 'MARCHE', 'MARCHES', 'MARDI', 'MEDITERRANEEN', 'MEDITERRANEENS', 'MEMBRES', 'MEME', 'MERCREDI', 'METTE', 'MEURTRIERE', 'MIEUX', 'MILLIARD', 'MILLION', 'MILLIONS', 'MINIMUM', 'MODELE', 'MODELES', 'MOINS', 'MOIS', 'MONDIALES', 'MONDIALISATION', 'MONETAIRE', 'MONTRE', 'MONTRER', 'MOUVANT', 'MOUVEMENT', 'MOYENNE', 'MOYENS', 'NATIONAL', 'NE', 'NI', 'NIVEAU', 'NON', 'NORDIQUE', 'NOS', 'NOTE', 'NOUVEAU', 'OBLIGATAIRES', 'OBLIGATIONS', 'OBLIGER', 'OBTENIR', 'OCTOBRE', 'OFFRE', 'ON', 'ONT', 'OPERER', 'OPINION', 'OR', 'ORGANISME', 'OU', 'OUI', 'OUR', 'OUTRE', 'OUVRIER', 'PAIE', 'PAIEMENT', 'PAN', 'PAR', 'PARCE', 'PARTICULIER', 'PARTICULIERS', 'PARTS', 'PARVIENT', 'PAS', 'PAYS', 'PENSENT', 'PERCEVOIR', 'PERDRONT', 'PERMETTRA', 'PERSISTANTE', 'PERSPECTIVE', 'PERTE', 'PERTES', 'PETROLE', 'PEU', 'PEURS', 'PEUVENT', 'PLACE', 'PLAIDANT', 'PLAN', 'PLUS', 'PLUSIEURS', 'POLITIQUE', 'POPULATION', 'PORT', 'POSSIBILITE', 'POUR', 'POURSUIVIE', 'PRECEDES', 'PRECISEMENT', 'PRES', 'PRESERVATION', 'PRESQUE', 'PRESSION', 'PREVISIONNISTES', 'PREVISIONS', 'PREVOIR', 'PRIMO', 'PRIVE', 'PRIVEE', 'PRIVENT', 'PRIX', 'PROBLEME', 'PROCEDER', 'PROCHAIN', 'PROCHAINE', 'PROCHAINES', 'PROFESSEUR', 'PROFESSIONNELS', 'PROTECTION', 'PROTEGE', 'PROVIENT', 'PUBLIE', 'PUBLIER', 'PUBLIQUE', 'PUISQUE', 'QU', 'QUALIFIES', 'QUANT', 'QUATRE', 'QUE', 'QUESTION', 'QUI', 'QUOI', 'RADIO-TELEVISEE', 'RALENTIS', 'RAPIDEMENT', 'RAPPELE', 'RAPPELLE', 'RAPPORT', 'RECETTE', 'RECHERCHE', 'RECUEILLAIT', 'RECUL', 'REDUIRE', 'REFERENDUM', 'REFLECHIR', 'REFLETENT', 'REGARDER', 'REGIME', 'REGIONS', 'REJOINDRE', 'RELEVE', 'RELIQUES', 'RENDEMENTS', 'REPERCUTEE', 'REPETER', 'REPONDRE', 'REPONDU', 'REPONSES', 'REPRENDRE', 'RESERVE', 'RESPONSABLES', 'RESSERREMENT', 'RESSERRER', 'RESSORTISSANTS', 'RESTE', 'RESULTE', 'RESUME', 'RETRAITES', 'RETROUVE', 'RETROUVER', 'REUNION', 'REUSSITE', 'RISQUE', 'RISQUENT', 'SA', 'SAINT', 'SALAIRES', 'SALARIES', 'SANS', 'SAUF', 'SCRUTIN', 'SE', 'SECTEURS', 'SECUNDO', 'SELON', 'SEMAINE', 'SEMAINES', 'SEPTEMBRE', 'SERAIENT', 'SERVICES', 'SES', 'SEUL', 'SEULEMENT', 'SEULS', 'SI', 'SIDERURGIE', 'SIGNIFIE', 'SOCIAL', 'SOCIALE', 'SOCIALES', 'SOCIAUX', 'SOIENT', 'SOIR', 'SOLIDE', 'SON', 'SONGER', 'SONT', 'SOUFFRE', 'SOUS', 'SPIRALE', 'STABLE', 'SUBI', 'SUFFI', 'SUGGERENT', 'SUIVI', 'SUIVRA', 'SUR', 'SUREMENT', 'SUREVALUES', 'SURSAUT', 'SYNDICATS', 'SYSTEME', 'SYSTEMES', 'TAUX', 'TELLE', 'TEMPORAIRES', 'TEND', 'TENDANCE', 'TENTES', 'TERME', 'THEMATIQUE', 'THEORIE', 'TOMBERONT', 'TOT', 'TOUJOURS', 'TOUR', 'TOUS', 'TOUT', 'TOUTE', 'TOUTES', 'TRADITIONNELS', 'TRANSFERE', 'TRANSMETTE', 'TRAVAUX', 'TRES', 'TROP', 'TYPE', 'UN', 'UNE', 'UNIQUE', 'UNIVERSITE', 'VA', 'VENDREDI', 'VERSE', 'VERSEMENTS', 'VEUT', 'VICE-PRESIDENT', 'VIENNENT', 'VIENT', 'VINGT', 'VOIE', 'VOLONTE', 'VONT', 'VOTE', 'VOULAIENT', 'VOULOIR', 'VU']
```

## 2) Construire une fonction qui vérifie que la liste chargée à la question précédente est triée. (4 points)
Input :
```python
def bool_tri (mot) :
    # range() : permet de créer une liste avec 3 paramètres : 1. numéro de départ de la liste, 2. dernier nombre de la liste et 3.incrément entre chaque nombre généré (par défaut, 1)
    # len() :  retourne le nombre d'éléments d'une chaîne de caractères ou d'une liste.
    for i in range (1, len (mot)) :
        if mot[i-1] > mot[i] :
            return False
        return True

tri = bool_tri (mot)
print "Liste triée ?", tri
```
Output :
```python
Liste triée ? True
```

## 3) Construire une fonction qui recherche un mot X dans la liste et qui retourne sa position ou -1 si ce mot n’y est pas. (4 points)
> Cette fonction prend deux paramètres : la liste et le mot à chercher. Elle retourne un entier. On précise que pour savoir si deux chaînes de caractères sont égales, il faut utiliser l’opérateur ==. 
Input :
```python

```
Output :
```python

```

## 4) Quels sont les positions des mots "UN" et "DEUX" ? (2 points)
> Il faudra écrire aussi le nombre de comparaisons effectuées pour trouver ces deux positions. 

Input :
```python

```
Output :
```python

```

## 5) Recherche dichotomique (4 points)

> Lorsqu’une liste est triée, rechercher un élément est beaucoup plus rapide. Si on cherche le mot X dans la liste, il suffit de le comparer au mot du milieu pour savoir si ce mot est situé dans la partie basse (X inférieur au mot du milieu), la partie haute (X supérieur au mot du milieu). S’il est égal, le mot a été trouvé. Si le mot n’a pas été trouvé, on recommence avec la sous-liste inférieure ou supérieure selon les cas jusqu’à ce qu’on ait trouvé le mot ou qu’on soit sûr que le mot cherché n’y est pas.
Le résultat de la recherche est la position du mot dans la liste ou -1 si ce mot n’a pas été trouvé. Cette recherche s’appelle une recherche dichotomique.

> Ecrire la fonction qui effectue la recherche dichotomique d’un mot dans une liste triée de mots.
Vérifiez que les deux fonctions retournent bien les mêmes résultats. Cette fonction peut être récursive
ou non. Elle prend au moins les deux mêmes paramètres que ceux de la question 3, si elle en a
d’autres, il faudra leur donner une valeur par défaut. On précise que les comparaisons entre chaînes
de caractères utilisent aussi les opérateurs <, ==, >. 

## 6) Normalement, les positions des mots "UN" et "DEUX" n’ont pas changé mais il faut de nouveau déterminer le nombre d’itérations effectuées pour trouver ces deux positions avec la recherche dichotomique. (2 points)

Input :
```python

```
Output :
```python

```

## 7) Quel est, au pire*, le coût d’une recherche non dichotomique ? (1 point) 
> * On cherche la meilleure majoration du coût de la recherche non dichotomique en fonction de la taille n de la
liste.

Input :
```python

```
Output :
```python

```

## 8) Quel est, au pire, le coût d’une recherche dichotomique ? (1 point)

