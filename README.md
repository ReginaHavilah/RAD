### **📜 README.md – Projet de Représentation Avancée de Données**  



---

```md
# 🚆 Projet de Représentation Avancée de Données – Optimisation d’un Réseau Ferroviaire / projet 2 java

## 📌 Présentation  
Ce projet a été réalisé dans le cadre du **cours de Représentation Avancée de Données**, avec une date de rendu fixée au **17 mai 2023**.  
Il vise à modéliser un **réseau ferroviaire optimisé** à l’aide d’un **graphe pondéré**, et à appliquer **l’algorithme de Kruskal** afin de minimiser le coût total des infrastructures.  

---

## 🎯 Objectifs
✔️ **Modéliser un réseau ferroviaire sous forme de graphe** avec des **villes** comme **nœuds** et des **voies ferrées** comme **arcs pondérés**  
✔️ **Implémenter l’algorithme de Kruskal** pour construire l’**arbre couvrant minimal** (réseau optimal)  
✔️ **Développer une structure de données efficace** pour stocker et manipuler le graphe  
✔️ **Optimiser la représentation des données** et analyser les performances  

---

## 📂 Structure du projet  
📁 `src/` → Contient les **fichiers source en Java** pour la gestion du graphe et l’algorithme de Kruskal  
📁 `data/` → Contient des **exemples de réseaux ferroviaires** sous forme de fichiers texte  
📁 `docs/` → Contient le **rapport explicatif** du projet en PDF  
📁 `tests/` → Contient les **cas de test** pour valider l’implémentation  

---

## **📜 Description technique**
### **1️⃣ Modélisation du graphe**  
Le réseau ferroviaire est représenté sous forme de **graphe non orienté pondéré**, où :  
- Les **nœuds** représentent des **villes**  
- Les **arcs pondérés** représentent des **voies ferrées**, le poids correspondant au **coût d’exploitation**  

**Fonctionnalités principales** :  
🔹 **Ajout de villes** au graphe  
🔹 **Ajout/Suppression de voies ferrées** avec un coût d’exploitation  
🔹 **Vérification de la connectivité** entre deux villes  
🔹 **Affichage des informations du graphe**  

---

### **2️⃣ Algorithme de Kruskal – Construction du réseau optimal**  
L’**algorithme de Kruskal** est utilisé pour **trouver l’arbre couvrant minimal**, c'est-à-dire :  
- **Sélectionner un sous-ensemble de voies ferrées** qui relient toutes les villes  
- **Minimiser le coût total du réseau**  

📌 **Implémentation :**  
- Trier les **arcs** par **poids croissant**  
- Ajouter les arcs **un par un**, en évitant les **cycles**  
- Vérifier que toutes les villes sont connectées  

📌 **Exemple d’exécution :**  
```java
Graph graph = new Graph();
graph.addCity("Paris");
graph.addCity("Lyon");
graph.addRail("Paris", "Lyon", 350);
graph.addRail("Lyon", "Marseille", 250);
graph.optimizeNetwork();
graph.displayNetwork();
```
📌 **Sortie attendue :**  
```
Réseau optimal :
- Paris ↔ Lyon (350)
- Lyon ↔ Marseille (250)
Coût total : 600
```

---

### **3️⃣ Implémentation du Graphe**
Deux structures de données ont été envisagées :  
1️⃣ **Matrice d’adjacence** : Permet un accès rapide mais peu optimale pour l’ajout/suppression d’arcs  
2️⃣ **Liste d’adjacence** : Plus efficace pour les parcours et les algorithmes sur graphes  

📌 **Classes principales :**  
- `Graph` → Gestion du graphe (ajout/suppression de villes et de voies)  
- `Edge` → Représentation d’une voie ferrée (deux villes + coût)  
- `Kruskal` → Implémentation de l’algorithme de Kruskal  

---

## 🚀 **Comment exécuter le projet ?**
1️⃣ **Compiler les fichiers Java** :  
```sh
javac -d bin src/*.java
```
2️⃣ **Exécuter le programme** :  
```sh
java -cp bin Main
```
3️⃣ **Tester avec des fichiers d’entrée** :  
```sh
java -cp bin Main data/reseau1.txt
```

---

## **🛠️ Technologies utilisées**
- **Langage** : Java  
- **Structures de données** : Graphe (Matrice/Liste d’adjacence)  
- **Algorithme** : Kruskal  
- **Outils** : IntelliJ / Eclipse 

---

## 📊 **Analyse des performances**
- **Complexité de Kruskal** : `O(E log E)` (tri des arêtes dominant)  
- **Comparaison entre Matrice vs Liste d’adjacence**  
- **Tests avec différents réseaux**  

---

## 📎 **Liens utiles**
🔗 [Documentation officielle Java](https://docs.oracle.com/en/java/)  
🔗 [Explication de l’algorithme de Kruskal](https://en.wikipedia.org/wiki/Kruskal%27s_algorithm)  

---

## **📌 Auteurs du projet**
👨‍💻 **VOEDZO Essivi Marie-Josée**  
👩‍💻 **DE BADAR BADAROU Hosniath**  



---
