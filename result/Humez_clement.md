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
- [x] B) Une classe est un modele (plan), un objet est une instance concrete de ce modele
- [ ] C) Un objet est un modele, une classe est une instance de cet objet
- [ ] D) Une classe contient uniquement des methodes, un objet contient uniquement des attributs

---

### Question 2 - Le mot-cle `this`
A quoi sert le mot-cle `this` dans une classe ?

- [ ] A) A creer une nouvelle instance de la classe
- [x] B) A faire reference a l'instance courante de l'objet
- [ ] C) A appeler le constructeur de la classe parente
- [ ] D) A declarer une variable statique

---

### Question 3 - Les modificateurs d'acces
Quelle est la difference entre `private` et `protected` ?

- [ ] A) `private` est accessible partout, `protected` uniquement dans la classe
- [x] B) `private` est accessible uniquement dans la classe, `protected` dans la classe et ses sous-classes
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

Il est privé pour empêcher une autre classe de créer une instance de DatabaseConnection avec new DatabaseConnection()
Il est privé pour éviter la lecture et la modification de la variable "connectionString" dans d'autres classes que la classe DatabaseConnection autrement que par le getter et le setter

Il n'y a qu'une seule instance car la variable instance est en static + la méthode getInstance() commence avec une instance null donc elle créé un nouvel objet, puis elle renvoie toujours le même donc ell assure qu’une seule instance existe et est partagée dans tout le programme

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

Ici, le abstract sert à créer une classe abstraite ce qui permet d'avoir la méthode abstraite parler(), cela permet de laisse la méthode vide et de pouvoir la modifier comme on veut dans les classes enfants de la classe Animal

Extends sert à faire de la classe que l'on crée une classe enfant (en l'occurence ici de la classe Animal), cela nous permet de récupérer les attributs grâce à super() et les méthodes de la classe parent

Super() va nous servir à récupérer les attributs de la classe parent (comme dans l'exemple ici super(nom) nous donne l'attribut nom)

@Override est ici utilisé pour modifier la méthode abstraite parler() définie dans la classe parent Animal
On l'utilise deux fois (dans Chien et dans Chat) où l'on peut voir que l'on ne met pas exactement la même chose, dans Chien on met System.out.println("Wouf!"); et dans Chat on met System.out.println("Miaou!");
@Override permet donc d'utiliser une méthode abstraite d'une classe parent (ou d'une Interface) et de la modifier à sa guise en fonction du besoin

Ce qu'il se passe c'est une erreur de compilation car on ne peut pas créer d’instance d’une classe abstraite
Seules les classes concrètes qui héritent de Animal et implémentent les méthodes abstraites peuvent être instanciées (comme new Chien("Rantaplan"), new Chat("Garfield"))

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

Une Interface est une sorte de contrat que s'engagent à respecter les Classes qui l'implémentent
Elle définit des méthodes (vide) que les Classes récupèrent et qu'on peut modifier à notre guise en fonction du besoin de la Classe
Ici, l'Interface Vehicule définir les méthodes demarrer(), arreter() et getVitessemMax()

implements est utilisé pour lier l'Interface à la Classe que l'on crée afin de lui imposer les méthodes de l'Interface

Si la Classe Voiture n'implémente pas toutes les méthodes de l'Interface, le compilateur Java générera une erreur

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


Il n’existe qu’une seule copie de la variable nombreInstances pour toute la classe, partagée par toutes les instances car elle est static
Tandis que chaque objet créé possède sa propre copie de la variable valeur et que modifier valeur dans un objet ne change pas la valeur des autres objets

Si on crée 3 instances de Compteur et que l'on appelle incrementer() sur chaque instance la valeur de getNombreInstances() sera 3 et la valeur de getValeur() sera 1 pour chacune car getNombresInstances() renvoie l'attribut static nombreInstances qui est le même pour toutes les instances (d'où le fait qu'il donne le nombre d'instances) et car getValeur() nous donne la valeur de l'instance qui gagne +1 à chaque appel de incrementer() mais on l'appelle une seule fois pour chaque instance donc elles n'augmentent que d'un chacune

---

### Question 20 - Conception orientee objet (1 point)

**Vous devez concevoir un systeme de gestion de bibliotheque. Identifiez et decrivez 3 classes que vous utiliseriez, leurs attributs principaux, et une relation entre elles (heritage, composition, ou implementation d'interface). Justifiez vos choix.**

Exemple de structure attendue :
- Classe 1 : [Nom] - Attributs : ... - Role : ...
- Classe 2 : [Nom] - Attributs : ... - Role : ...
- Classe 3 : [Nom] - Attributs : ... - Role : ...
- Relation : ...

- Classe 1 : [Livre] 
    - Attributs :
    String titre 
    String auteur
    int id
    boolean disponible

    - Role : Représente un livre de la bibliothèque, la classe stocke les informations essentielles d’un livre et permet de savoir s’il peut être emprunté ou pas

- Classe 2 : [Membre] 
    - Attributs :
    String nom
    int idMembre
    List<Livre> livresEmpruntes

    - Role : Représente une personne inscrite à la bibliothèque, elle permet de suivre quels livres un membre possède actuellement, la liste livresEmpruntes permet de gérer les emprunts du membre

- Classe 3 : [Bibliotheque] 
    - Attributs :
    List<Livre> catalogue
    List<Membre> membres

    - Role : Représente la bibliothèque, elle donne tous les livres disponibles et tous les membres, elle gère le prêt et le retour de livres

- Relation : Composition

    Bibliotheque contient des objets Livre et des objets Membre -> sans la bibliothèque, ces collections n'existent pas dans le système

    Membre contient les livres qu’il a empruntés (List<Livre>), ce qui représente aussi une relation de composition

Car livre n’hérite pas d’autre classe car c’est un objet simple, membre n’hérite pas non plus car son comportement est spécifique et ne représente pas une spécialisation d’un autre type, et bibliotheque n’est pas une classe enfant mais un gestionnaire d’ensemble, ce qui justifie son rôle de classe "principale"

---

## Bareme de notation

- **Partie 1 (QCM):** 1 point par bonne reponse, 0 point si mauvaise reponse
- **Partie 2 (Questions detaillees):** 
  - Question complete et precise : 1 point
  - Question partiellement correcte : 0.5 point
  - Question incorrecte ou incomplete : 0 point

**Total : _____ / 20**
