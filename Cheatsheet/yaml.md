YAML Ain't Markup Language
===
<!-- meta ------------------------------------------------------------------------------

Description ==  Présentation de YAML Ain't Markup Language
Tags        ==  Cheatsheet Language YAML Markup 

Post_Type   ==  Cheatsheet
Preview     ==  cli
Author      ==  Loxcy

Version     == 0.2
Featured    == True
Visible     == False
Draft       == True

created_at  == 2022-01-10 00:00:00
published_at== 2022-01-10 00:00:00
updated_at   == 2022-01-10 00:00:00


---------------------------------------------------------------------------- endmeta -->


### **Introduction à YAML**

YAML (l'acronyme de "YAML Ain't Markup Language") est un langage de marqueur léger utilisé pour la représentation de données structurées. Il a été créé pour faciliter la lecture et l'écriture de fichiers de configuration et de données par des humains, et est souvent utilisé pour remplacer les formats de données plus verbeux tels que XML et JSON.

### **Définition et contexte d'utilisation de YAML**

YAML est utilisé pour représenter des données structurées de manière simple et facile à lire. Il est souvent utilisé pour les fichiers de configuration de logiciels, les fichiers de données de jeux vidéo, les fichiers de description de conteneurs et les fichiers de données de tests. Il est également utilisé pour les fichiers de données d'applications Web, les fichiers de données de bases de données et les fichiers de données de scripts d'automatisation.

### **Comparaison avec d'autres formats de données couramment utilisés (JSON, XML)**

YAML est similaire à JSON en ce qu'il est utilisé pour représenter des données structurées, mais il est généralement considéré comme plus facile à lire et à écrire pour les humains. Il est également plus compact que XML. Alors que les fichiers XML peuvent être verbaux et difficiles à parcourir, les fichiers YAML sont plus concis et plus faciles à lire. Il est également plus facile de convertir les données YAML en un autre format, comme JSON ou XML, car il utilise des conventions de formatage similaires.

### **Structure de base de YAML**

La structure de base de YAML est composée de trois éléments clés : les paires de clé-valeur, les tableaux et les tableaux associatifs. Les paires de clé-valeur sont utilisées pour stocker des informations simples, tandis que les tableaux et les tableaux associatifs sont utilisés pour stocker des structures de données plus complexes.

### **Formatage des données (indentation, espacements, lignes vides)**

La mise en forme des données est importante pour la lisibilité de YAML. L'indentation est utilisée pour définir les relations de parenté entre les éléments de données, avec chaque niveau d'indentation représentant une profondeur de nœud. La norme recommandée est d'utiliser des espacements pour l'indentation plutôt que des tabulations.

Les espacements et les lignes vides sont utilisés pour séparer les éléments de données les uns des autres. Il est important de respecter ces conventions de formatage pour garantir que les fichiers YAML soient valides et qu'ils puissent être correctement interprétés par les outils de traitement de données. Il est important de noter que des espacements ou des retours à la ligne mal placés peuvent rendre un fichier YAML invalide et provoquer des erreurs lors de la lecture du fichier.

**Exemple de formatage :**
```yaml
parent:
    child:
        grandchild: value
    sibling: value
```

Les différents niveaux d'indentation définissent les relations parent-enfant entre les éléments, dans cette exemple grandchild est enfant de child qui est lui même enfant de parent.

Utilisation des séparateurs (espace, tiret, deux-points)
Les séparateurs sont utilisés pour spécifier les types d'éléments de données dans un fichier YAML. Un tiret suivi d'un espace est utilisé pour définir les éléments d'un tableau, tandis qu'un deux-points suivi d'un espace est utilisé pour définir les éléments d'un objet.
**Exemple :**
```yaml
#array
- item1
- item2
#object
key: value
```
### **Notation des listes et des objets**
Les listes sont définies en utilisant un tiret suivi d'un espace, tandis que les objets sont définis en utilisant une paire clé-valeur séparée par un deux-points suivi d'un espace. Les clés doivent être uniques dans un objet, mais peuvent être répétées dans une liste.

### **Exemples de fichiers YAML**
Un exemple courant d'utilisation de YAML est la configuration de logiciels et d'applications. Par exemple, un fichier de configuration pour une application Web pourrait ressembler à ceci :
```yaml
server:
    host: localhost
    port: 8080
database:
    host: localhost
    port: 3306
    user: root
    password: password
```
Dans cet exemple, nous avons un objet "server" qui contient les clés "host" et "port", ainsi qu'un objet "database" qui contient les clés "host", "port", "user" et "password". Cette structure permet à un développeur de facilement comprendre la configuration de l'application et de la modifier si nécessaire.

### **Utilisation de YAML dans les projets informatiques**
YAML est largement utilisé dans de nombreux projets informatiques pour la configuration de logiciels et d'applications. Il est également utilisé dans les environnements de développement intégré (IDE) pour la configuration des projets, dans les systèmes de gestion de contenu (CMS) pour la configuration des modèles de contenu, et dans les outils de déploiement pour la configuration des conteneurs et des clusters.

Un exemple répandu d'utilisation de YAML est dans Kubernetes, qui utilise YAML pour définir les configurations des différents objets dans un cluster, comme les pods, les services, les réplicasets, etc. Cela permet aux administrateurs de clusters de gérer facilement leur infrastructure en utilisant des fichiers de configuration lisibles et faciles à éditer.

Dans les projets Python, YAML est souvent utilisé pour lire et écrire des fichiers de configuration. Il peut être utilisé avec des bibliothèques comme PyYAML pour faciliter la manipulation des données YAML dans un programme Python. Par exemple, voici comment lire un fichier de configuration YAML en Python:

```python
import yaml

with open('config.yaml', 'r') as f:
    config = yaml.load(f, Loader=yaml.FullLoader)

print(config)
```

Ce code utilise la bibliothèque PyYAML pour ouvrir le fichier config.yaml, le charger en utilisant un "Loader" yaml.FullLoader, et ensuite le stocker dans une variable config.

YAML est également souvent utilisé pour stocker des données de test dans les projets Python. Les bibliothèques de tests comme pytest permettent de charger des données de test à partir de fichiers YAML pour les utiliser dans les cas de test. Par exemple, voici comment définir des données de test dans un fichier YAML:

```yaml
# test_data.yaml
- name: 'John Doe'
  age: 25
  occupation: 'Developer'
- name: 'Jane Smith'
  age: 32
  occupation: 'Tester'
```
En utilisant pytest, vous pouvez ensuite utiliser ces données dans un cas de test comme suit:



```python
def test_example(test_data):
    for person in test_data:
        assert person['name']
        assert person['age']
        assert person['occupation']
```
En utilisant pytest il est possible de spécifier que les données de test sont chargées à partir d'un fichier YAML et sont associées à la variable de argument de la fonction test_example


### **Outils et librairies pour travailler avec YAML**
Il existe de nombreuses librairies pour travailler avec YAML dans différents languages de programmation, y compris Python, Ruby, JavaScript et Java. Il existe également des outils en ligne pour convertir des fichiers YAML en d'autres formats, ainsi que des outils pour valider la syntaxe des fichiers YAML.

En conclusion, YAML est un format de données populaire et pratique pour la représentation de données structurées, offrant une lisibilité accrue pour les humains par rapport à des formats tels que XML ou JSON. Il est largement utilisé dans les projets informatiques pour la configuration de logiciels et d'applications, ainsi que dans des outils tels que Kubernetes pour la gestion des clusters. Il existe également de nombreux outils et librairies pour travailler avec YAML dans différents languages de programmation.