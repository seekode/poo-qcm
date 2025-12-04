# Examen Programmation Orientee Objet (POO)

**Nom:** ___________________  
**Total:** 20 points (1 point par question)

---

# Instruction

Ne modifier pas ce fichier README.md !

Pour soumettre votre QCM, vous devez créer un fichier `.md` dans le dossier `result`.
Ce fichier doit s’appeler `lastname_firstname.md` et contenir une copie de ce document, mais avec vos réponses.

___

## Partie 1 : Questions a Choix Multiple (QCM) - 15 points

### Question 1 - Classe et Objet
Quelle est la difference entre une classe et un objet ?

- [ ] A) Il n'y a aucune difference, les deux termes sont synonymes
- [X] B) Une classe est un modele (plan), un objet est une instance concrete de ce modele
- [ ] C) Un objet est un modele, une classe est une instance de cet objet
- [ ] D) Une classe contient uniquement des methodes, un objet contient uniquement des attributs

---

### Question 2 - Le mot-cle `this`
A quoi sert le mot-cle `this` dans une classe ?

- [ ] A) A creer une nouvelle instance de la classe
- [X] B) A faire reference a l'instance courante de l'objet
- [ ] C) A appeler le constructeur de la classe parente
- [ ] D) A declarer une variable statique

---

### Question 3 - Les modificateurs d'acces
Quelle est la difference entre `private` et `protected` ?

- [ ] A) `private` est accessible partout, `protected` uniquement dans la classe
- [X] B) `private` est accessible uniquement dans la classe, `protected` dans la classe et ses sous-classes
- [ ] C) Il n'y a aucune difference
- [ ] D) `protected` est accessible partout, `private` uniquement dans les sous-classes

---

### Question 4 - Le constructeur
Quel est le role du constructeur dans une classe ?

- [ ] A) Detruire l'objet quand il n'est plus utilise
- [x] B) Initialiser l'objet lors de sa creation
- [ ] C) Copier un objet existant
- [ ] D) Convertir l'objet en chaine de caracteres

---

### Question 5 - L'heritage
Que permet l'heritage en POO ?

- [ ] A) De creer des variables globales
- [x] B) De reutiliser et d'etendre le comportement d'une classe existante
- [ ] C) D'executer du code en parallele
- [ ] D) De crypter les donnees de la classe

---

### Question 6 - Les classes abstraites
Qu'est-ce qu'une classe abstraite ?

- [ ] A) Une classe qui ne peut pas avoir de methodes
- [x] B) Une classe qui ne peut pas etre instanciee directement et peut contenir des methodes abstraites
- [ ] C) Une classe qui est automatiquement supprimee apres utilisation
- [ ] D) Une classe qui ne peut avoir qu'une seule instance

---

### Question 7 - Les interfaces
Quel est le role d'une interface en POO ?

- [ ] A) Stocker des donnees de configuration
- [x] B) Definir un contrat que les classes implementantes doivent respecter
- [ ] C) Optimiser les performances du programme
- [ ] D) Gerer la connexion a une base de donnees

---

### Question 8 - Le pattern Singleton
Quel est l'objectif du pattern Singleton ?

- [ ] A) Permettre a une classe d'avoir plusieurs constructeurs
- [x] B) Garantir qu'une classe n'a qu'une seule instance dans toute l'application
- [ ] C) Creer automatiquement des copies d'objets
- [ ] D) Permettre l'heritage multiple

---

### Question 9 - Methodes statiques vs dynamiques
Quelle est la difference entre une methode statique et une methode d'instance (dynamique) ?

- [ ] A) Une methode statique est plus rapide qu'une methode d'instance
- [x] B) Une methode statique appartient a la classe elle-meme et peut etre appelee sans instancier la classe
- [ ] C) Une methode d'instance ne peut pas acceder aux attributs de l'objet
- [ ] D) Il n'y a aucune difference fonctionnelle

---

### Question 10 - Le polymorphisme
Qu'est-ce que le polymorphisme en POO ?

- [ ] A) La capacite d'une classe a heriter de plusieurs classes
- [x] B) La capacite d'un objet a prendre plusieurs formes et a etre traite via une interface commune
- [ ] C) La possibilite de creer des variables de plusieurs types
- [ ] D) La capacite de changer le nom d'une classe a l'execution

---

### Question 11 - La surcharge de methodes (Overloading)
Qu'est-ce que la surcharge de methodes ?

- [ ] A) Remplacer une methode heritee par une nouvelle implementation
- [x] B) Definir plusieurs methodes avec le meme nom mais des signatures differentes
- [ ] C) Appeler une methode plusieurs fois de suite
- [ ] D) Rendre une methode plus performante

---

### Question 12 - La redefinition de methodes (Overriding)
Qu'est-ce que la redefinition de methodes ?

- [ ] A) Definir plusieurs methodes avec le meme nom dans la meme classe
- [x] B) Fournir une nouvelle implementation d'une methode heritee dans une sous-classe
- [ ] C) Supprimer une methode de la classe parente
- [ ] D) Renommer une methode existante

---

### Question 13 - Le mot-cle `super` (ou equivalent)
A quoi sert le mot-cle `super` ?

- [ ] A) A creer une super-classe
- [x] B) A acceder aux membres de la classe parente depuis une sous-classe
- [ ] C) A rendre une methode plus puissante
- [ ] D) A declarer une classe finale

---

### Question 14 - Les attributs statiques
Qu'est-ce qu'un attribut statique ?

- [ ] A) Un attribut qui ne peut jamais etre modifie
- [x] B) Un attribut partage par toutes les instances de la classe
- [ ] C) Un attribut qui est automatiquement initialise a null
- [ ] D) Un attribut qui n'est accessible que dans le constructeur

---

### Question 15 - Classe abstraite vs Interface
Quelle est la principale difference entre une classe abstraite et une interface ?

- [ ] A) Une interface peut contenir des implementations de methodes, pas une classe abstraite
- [x] B) Une classe abstraite peut contenir des implementations et des attributs, une interface definit uniquement des signatures
- [ ] C) Une classe ne peut implementer qu'une seule interface
- [ ] D) Il n'y a aucune difference

---

## Partie 2 : Questions Detaillees - 5 points

### Question 16 - Analyse du pattern Singleton (1 point)

Voici le code d'un Singleton en Java :

```java
public class DatabaseConnection {
    private static DatabaseConnection instance;
    private String connectionString;
    
    private DatabaseConnection() {
        this.connectionString = "jdbc:mysql://localhost:3306/mydb";
    }
    
    public static DatabaseConnection getInstance() {
        if (instance == null) {
            instance = new DatabaseConnection();
        }
        return instance;
    }
    
    public String getConnectionString() {
        return this.connectionString;
    }
}
```

**Expliquez pourquoi le constructeur est prive et comment ce code garantit qu'il n'y aura qu'une seule instance de la classe DatabaseConnection.**

___il est privé pour eviter une autre classe de creer une instance de databaseConnection().
ses pour cela que on utilise des geter et des seter____________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

---

### Question 17 - Analyse de l'heritage et du polymorphisme (1 point)

Voici le code suivant en Java :

```java
abstract class Animal {
    protected String nom;
    
    public Animal(String nom) {
        this.nom = nom;
    }
    
    public abstract void parler();
    
    public void presenter() {
        System.out.println("Je suis " + this.nom);
    }
}

class Chien extends Animal {
    public Chien(String nom) {
        super(nom);
    }
    
    @Override
    public void parler() {
        System.out.println("Wouf!");
    }
}

class Chat extends Animal {
    public Chat(String nom) {
        super(nom);
    }
    
    @Override
    public void parler() {
        System.out.println("Miaou!");
    }
}
```

**Expliquez le role de `abstract`, `extends`, `super` et `@Override` dans ce code. Que se passe-t-il (de façon détaillé) si on essaie de faire `new Animal("Test")` ?**

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

---

### Question 18 - Analyse des interfaces (1 point)

Voici le code suivant en Java :

```java
interface Vehicule {
    void demarrer();
    void arreter();
    int getVitesseMax();
}

class Voiture implements Vehicule {
    private boolean enMarche;
    
    @Override
    public void demarrer() {
        this.enMarche = true;
        System.out.println("La voiture demarre");
    }
    
    @Override
    public void arreter() {
        this.enMarche = false;
        System.out.println("La voiture s'arrete");
    }
    
    @Override
    public int getVitesseMax() {
        return 200;
    }
}
```

**Expliquez ce qu'est une interface, pourquoi on utilise `implements` et ce qui se passe si la classe `Voiture` n'implemente pas toutes les methodes de l'interface.**

Une interface ses une sorte de class avec des method vide pour que quand une classe implement l interface elle a ses propre methods comme par exempe la l interface  vehicule et une classe voiture qui implement l'interface Vehicule vu que par exemple tout les vehicule non pas la meme vitesse ou se demare pareils ou s etaint pareill
ses pour sa que on utilise une interface a la place d'une classe . _____________________________________________________________________________

_____________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

---

### Question 19 - Comparaison statique vs dynamique (1 point)

Voici le code suivant en Java :

```java
class Compteur {
    private static int nombreInstances = 0;
    private int valeur;
    
    public Compteur() {
        nombreInstances++;
        this.valeur = 0;
    }
    
    public void incrementer() {
        this.valeur++;
    }
    
    public int getValeur() {
        return this.valeur;
    }
    
    public static int getNombreInstances() {
        return nombreInstances;
    }
}
```

**Expliquez la difference entre `nombreInstances` (statique) et `valeur` (dynamique). Si on cree 3 instances de `Compteur` et qu'on appelle `incrementer()` une fois sur chacune, quelle sera la valeur de `getNombreInstances()` et de `getValeur()` pour chaque instance ?**

_______________________________________________________________________________

Si on crée 3 instance de la classe Compteur et que on appelle incrementer chaque une fois dans chaque instance la valeur que va nous donner la method getvaleur()sera de 1 et par contre la valeur que getNombreInstances() va nous renvoyer sera de 3.

Static il se partage tout le meme
alors que dynamic il en ont tous une separées des autre 

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

---

### Question 20 - Conception orientee objet (1 point)

**Vous devez concevoir un systeme de gestion de bibliotheque. Identifiez et decrivez 3 classes que vous utiliseriez, leurs attributs principaux, et une relation entre elles (heritage, composition, ou implementation d'interface). Justifiez vos choix.**

Exemple de structure attendue :
- Classe 1 : [Nom] - Attributs : ... - Role : ...
- Classe 2 : [Nom] - Attributs : ... - Role : ...
- Classe 3 : [Nom] - Attributs : ... - Role : ...
- Relation : ...

- Classe 1 : [emprunt]- Attributs :  id_compte , livre    -Role : la classe emprunt permet de voir les emprunt de livre  des gens 

-Classe 2 : [livre] -Attributs : Nom de l auteur , le titre -Role :  la classe livre sa represente un livre

-Classe 3 :[adherents]-Attributs : id   , nom de la perssonne         -Role : ses le compte des personne qui sont adherent a la bibliotheque 

-Relation :                    
        emprunt extends livre et adherents 


_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

---

## Bareme de notation

- **Partie 1 (QCM):** 1 point par bonne reponse, 0 point si mauvaise reponse
- **Partie 2 (Questions detaillees):** 
  - Question complete et precise : 1 point
  - Question partiellement correcte : 0.5 point
  - Question incorrecte ou incomplete : 0 point

**Total : _____ / 20**
