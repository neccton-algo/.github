---
title: Python Coding Standards
description: Tools to help you write clean code
published: true
date: 2021-05-11T14:46:51.926Z
tags: 
editor: markdown
dateCreated: 2021-01-28T10:21:49.628Z
---

# Outils de qualification du code python
## Qualité du code
Il existe plusieurs définitions et la plupart de ces définitions s'accordent sur les points suivants:
* le code fait ce qu’il est supposé faire : s’il ne fait pas cette exigence de base, il ne sert à rien de parler de qualité de code.

* le code ne contient pas de défauts ou de bugs : comme n’importe quel produit, avant d’être industrialisé, il faut gommer tous les défauts indésirables. En d’autres termes, pour parler de haute qualité, il faut que votre application prévoie tous les cas de figure et être capable de les adresser.

* le code est facile à lire, à entretenir et à étendre : Personne ne veut être dans la position où il doit lire, maintenir ou étendre un code de mauvaise qualité.

## PEP 8 pour un bon développement
PEP (Python Enhancement Proposal : proposition d’amélioration de Python) est une convention d'écriture de code conçue pour améliorer certains aspects de python, allant des performances aux nouvelles fonctionnalités, en passant par la documentation. 

La PEP 8 consiste en un nombre important de recommandations sur la syntaxe de Python. Il est vivement recommandé de lire la PEP 8 en entier au moins une fois pour avoir une bonne vue d'ensemble. On ne présentera ici qu'un rapide résumé de cette PEP 8 :

### Indentation
Il faut mettre 4 espaces pour bien séparer les blocs et avoir un code lisible (pas de tabulation). Pour cela, il faut régler l’éditeur de code, pour faire en sorte que lorsqu’on presse la touche tabulation, cela ajoute 4 espaces et non un caractère tabulation.

### Règles de nommage
* Packages /Modules : Doit utiliser uniquement des minuscules. Les traits de soulignement peuvent être utilisés si nécessaire, mais sont déconseillés. Exp : `package ou module.py`

* Constantes : Sont écrites en majuscule. Exp : `My_CONST = ‘…’`.

* Fonctions / Variables : En minuscule avec éventuellement des underscores. Exp : `my_function(), my_variable`

* Arguments de fonction / méthode : minuscule et underscore si besoin (snake case). Exp : unit_price

* Classes / Exception : Doit utiliser `CapWords`(upper camel case). Il est recommandé de ne pas utiliser le mot Classe dans le nom. Exp : `MyClasse, MyException`.

### Longueur de ligne
Une ligne de code ne doit pas dépasser 79 caractères, pour des raisons tant historiques que de lisibilité.
On peut utiliser le caractère \ pour couper des lignes trop longues. Par exemple :
{{{
>>> ma_variable = 3
>>> if ma_variable > 1 and ma_variable < 10 \
... and ma_variable % 2 == 1 and ma_variable % 3 == 0:
...     print("ma variable vaut {}".format(ma_variable))
...
ma variable vaut 3
}}}
À l'intérieur d'une parenthèse, on peut revenir à la ligne sans utiliser le caractère \. C'est particulièrement utile pour préciser les arguments d'une fonction ou d'une méthode, lors de sa création ou lors de son utilisation :
{{{
>>> def ma_fonction(argument_1, argument_2,
...                 argument_3, argument_4):
...     return argument_1 + argument_2
...
>>> ma_fonction("texte très long", "tigre",
...             "singe", "souris")
'texte très longtigre'
}}}
### Lignes vides
Les lignes vides sont utiles pour séparer visuellement les différentes parties du code.

Il est recommandé de laisser deux lignes vides avant la définition d'une fonction ou d'une classe et de laisser une seule ligne vide avant la définition d'une méthode (dans une classe).

On peut aussi laisser une ligne vide dans le corps d'une fonction pour séparer les sections logiques de la fonction, mais cela est à utiliser avec parcimonie.

### Commentaires
Les commentaires débutent toujours par le symbole # suivi d'un espace. Ils donnent des explications claires sur l'utilité du code et doivent être synchronisés avec le code, c'est-à-dire que si le code est modifié, les commentaires doivent l'être aussi.

Les commentaires sont au même niveau d'indentation que le code qu'ils commentent. Les commentaires sont constitués de phrases complètes, avec une majuscule au début (sauf si le premier mot est une variable qui s'écrit sans majuscule) et un point à la fin.

La PEP 8 recommande très fortement d'écrire les commentaires en anglais, sauf si on est sûr que le code ne sera lu que par des francophones. Dans la mesure où on va souvent développer des programmes scientifiques, il est conseillé d'écrire les commentaires en anglais.

Pour plus d’informations, se référer à la page suivante: https://www.python.org/dev/peps/pep-0008/

## PEP 257 et les docstrings
PEP 257 est une proposition décrivant les conventions relatives aux docstrings de Python. Ce sont des chaînes de caractères destinées à documenter des modules, des classes, des fonctions et des méthodes. Lorsque l'explication est courte et compacte comme dans certaines fonctions ou méthodes simples, il faut utiliser des docstrings d'une ligne :

`"""Docstring simple d'une ligne se finissant par un point."""`

Lorsqu'on a besoin de décrire plus en détail un module, une fonction, une classe ou une méthode, il faut utiliser une docstring sur plusieurs lignes.

{{{
"""Docstring de plusieurs lignes, la première ligne est un résumé.

Après avoir sauté une ligne, on décrit les détails de cette docstring.
tototo
tititi
grosminet
On termine la docstring avec les triples guillemets sur la ligne suivante.
"""
}}}

La PEP 257 n’exige pas un style particulier. NumPy Style Python Docstring, très utilisé en analyse de données, a un style très intéressant.

{{{
def function_with_types_in_docstring(param1, param2):
    """Example function with types documented in the docstring.
 
    Parameters
    ----------
    param1 : int
        The first parameter.
    param2 : str
        The second parameter.
 
    Returns
    -------
    bool
        True if successful, False otherwise.
 
    .. _PEP 484:
        https://www.python.org/dev/peps/pep-0484/
 
    """
}}}
Si les docstrings sont cohérents, il existe des outils capables de générer de la documentation directement à partir du code.
Pour plus d’informations, se référer à la page : https://www.python.org/dev/peps/pep-0257/

Donc, les guides PEP8 et PEP257 définissent un moyen de styliser le code. Mais comment l’appliquer ? Et qu’en est-il des défauts et des problèmes dans le code, comment pouvoir les détecter ? C’est là que les outils de contrôle de qualité de code (Linters) entrent en jeu.

## Linter tools pour une meilleur qualité de code
Pour évaluer la qualité d’un code Python, c’est-à-dire sa conformité avec les recommandations de la PEP 8 et de la PEP 257, on peut utiliser des outils automatisés dédiés tels que pycodestyle, pydocstyle et pylint. Pour ce faire on peut utiliser par exemple la commande suivante:
`$ conda install -c conda-forge pycodestyle pydocstyle pylint`

* NB: *Les outils pycodestyle, pydocstyle et pylint sont des linters, c'est-à-dire des programmes qui vont chercher les sources potentielles d'erreurs dans un code informatique. Ces erreurs peuvent être des erreurs de style (PEP 8 et 257) ou des erreurs logiques (manipulation d'une variable, chargement de module).

Prenons l'exemple du script génération de cache de l'opendap avant de faire un contrôle de qualité avec les Linters:
{{{
#!/usr/bin/env python3
# -*- coding: utf-8 -*-

from multiprocessing import Pool
import requests
from siphon.catalog import TDSCatalog

def generatecache(url):
    dataset = requests.get(url)
    print("{0:03d} {1:s}".format(dataset.status_code, url))

def fetchlist(urtmp, listds):
    cat = TDSCatalog(urtmp)

    if cat.datasets:
        listds.extend(cat.datasets)

    listurl = []

    for i in cat.catalog_refs.values():
        listurl.append(i.href)
        listtmp = fetchlist(i.href,listds)
        listurl.extend(listtmp)

    return listurl

def main():
    urlbase = 'http://tdspub-02.mercator-ocean.fr:8080/thredds/catalog.html'
    listds = []
    fetchlist(urlbase, listds)
    hostlist = ["http://tdspub-02.mercator-ocean.fr:8080","http://tdspub-01.mercator-ocean.fr:8080"]
    proc = Pool(10)
    listurl = [host+"/thredds/dodsC/"+x+".html" for x in listds for host in hostlist]
    proc.map(generatecache, listurl)
    proc.close()
    proc.join()
if __name__ == '__main__':
    main()
}}}

Nous allons tout d'abord vérifier la conformité avec la PEP 8 grâce à l'outil pycodestyle :
{{{
mrached@px-149:/home/mrached/ $ pycodestyle cachegeneration.py
cachegeneration.py:13:1: E302 expected 2 blank lines, found 1
cachegeneration.py:17:1: E302 expected 2 blank lines, found 1
cachegeneration.py:27:35: E231 missing whitespace after ','
cachegeneration.py:32:1: E302 expected 2 blank lines, found 1
cachegeneration.py:36:58: E231 missing whitespace after ','
cachegeneration.py:36:80: E501 line too long (100 > 79 characters)
cachegeneration.py:38:80: E501 line too long (85 > 79 characters)
cachegeneration.py:42:1: E305 expected 2 blank lines after class or function definition, found 0
}}}

Ensuite, nous vérifions à l'aide de l'outil pycodestyle la conformité avec la PEP 257 qui s'intéresse particulièrement aux docstrings:
{{{
mrached@px-149:/home/mrached/ $ pydocstyle cachegeneration.py
cachegenerationt.py:3 at module level:
        D400: First line should end with a period (not '0')
cachegeneration.py:13 in public function `generatecache`:
        D103: Missing docstring in public function
cachegeneration.py:17 in public function `fetchlist`:
        D103: Missing docstring in public function
cachegeneration.py:32 in public function `main`:
        D103: Missing docstring in public function

* Remarque: *Les outils pycodestyle et pydocstyle permettent uniquement de vérifier la conformité aux PEP 8 et 257. 
}}}
### Pylint Tool
En plus de la vérification des règles de conformité avec PEP 8 et PEP 257, cet outil va essayer de comprendre le contexte du code et proposer des éléments d'amélioration.

{{{
mrached@px-149:/home/mrached/scripts/opendap $ pylint cachegeneration.py
************* Module cachegenerationtest
cachegeneration.py:27:34: C0326: Exactly one space required after comma
        listtmp = fetchlist(i.href,listds)
                                  ^ (bad-whitespace)
cachegeneration.py:36:57: C0326: Exactly one space required after comma
    hostlist = ["http://tdspub-02.mercator-ocean.fr:8080","http://tdspub-01.mercator-ocean.fr:8080"]
                                                         ^ (bad-whitespace)
cachegeneration.py:13:0: C0111: Missing function docstring (missing-docstring)
cachegeneration.py:17:0: C0111: Missing function docstring (missing-docstring)
cachegeneration.py:32:0: C0111: Missing function docstring (missing-docstring)

-----------------------------------
Your code has been rated at 8.21/10
}}}

En suivant les recommandations de cet outil, le script a été corrigé:
{{{
#!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
Created on Wed Jun 24 08:12:51 2020

@author: mrached
"""

from multiprocessing import Pool
import requests
from siphon.catalog import TDSCatalog

def generatecache(url):
    """Get data from url address"""
    dataset = requests.get(url)
    print("{0:03d} {1:s}".format(dataset.status_code, url))

def fetchlist(urtmp, listds):
    """Return list of dataset"""
    cat = TDSCatalog(urtmp)

    if cat.datasets:
        listds.extend(cat.datasets)

    listurl = []

    for i in cat.catalog_refs.values():
        listurl.append(i.href)
        listtmp = fetchlist(i.href, listds)
        listurl.extend(listtmp)

    return listurl

def main():
}}}

Les résultats suivants sont obtenus suite au lancement de la commande pylint:

{{{
mrached@px-149:/home/mrached/ $ pylint cachegeneration.py

--------------------------------------------------------------------
Your code has been rated at 10.00/10 (previous run: 10.00/10, +0.00)
}}}

*Remarques :*
la plupart des IDE ont déjà des linters intégrés comme par exemple :

* `Spyder` : https://www.spyder-ide.org/
* `Sublime Text` : http://www.sublimelinter.com/en/stable/linter_settings.html#python
* `Atom`: http://https://atom.io/packages/linter-python-pep8
* `PyCharm`: https://plugins.jetbrains.com/plugin/11084-pylint
* `Eclipse avec pydev` : http://www.pydev.org/












