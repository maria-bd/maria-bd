
# PMO - Documentation Backend avec Spring Boot

## Objectif

**PMO** est une application web qui vise à centraliser et uniformiser la gestion de projets, améliorer la visibilité globale et faciliter le reporting au niveau de la BU Project de Beyn.

## Prérequis



- Postgres 16.3

- pgAdmin 4

- java 21

- Spring boot 3.2.7

- Intellij IDE (code et requetes)

## Initialisation 

### Création du projet

Apres l'installation de postgres/pg admin/ java 21 et Intellij on ouvre Intellij est on choisit: **New Project**

![image](https://github.com/maria-bd/maria-bd/assets/135654272/3c6e5821-c77d-446a-be40-a4fa7adeb686)

- Generator: **Spring Boor**

- Name: **PMO** 

- Language: **Java**

- Type: **Maven**

- Group: **com.beyn**

- JDK: **21**

- Java: **21**

- Packaging : **Jar**


### Dépendances
On vas choisir quelques dépendances tres importante pour commencer le projet et on rajoutera au fur et à mesure

Dans cette étape, on choisira aussi la version de **Spring Boot** qui est **3.2.7**

![image](https://github.com/maria-bd/maria-bd/assets/135654272/81dd236c-54c9-47c1-b4f1-63a3a4d2efac)

### Hierarchy
Apres avoir cree notre projet on tombe sur cette hierarchy

pmo
├── .idea
├── .mvn
│   └── wrapper
│       └── maven-wrapper.properties
├── src
│   └── main
│       ├── java
│       │   └── com.beyn.pmo
│       │       └── PmoApplication.java
│       └── resources
│           ├── static
│           ├── templates
│           └── application.proporties
├── test
├── target
├── .gitignore
├── HELP.md
├── mvnw
├── mvnw.cmd
├── pom.xml



## Développment
### Commancement
Lors du developpement de notre projet on vas traiter sur ces parties : 

pmo
├── .idea
├── .mvn
│   └── wrapper
│       └── maven-wrapper.properties
├── src
│   └── main
│       ├── java
│       │   └── com.beyn.pmo
                |---------------------------------------> on vas ajouter les dossiers qui continnent la majarité de notre code ici
│       │       └── PmoApplication.java
│       └── resources
│           ├── static
│           ├── templates
│           └── application.proporties ---------------------> ce fichier vas etre changer en application.yaml
├── test
├── target
├── .gitignore
├── HELP.md
├── mvnw
├── mvnw.cmd
├── pom.xml ---------------------> ce fichier contient des informations sur le projet ainsi que des plugins et les dépendances, on vas le modifier quand on ajoute des dépendances.

### hierarchy du code source
pmo
├── .idea
├── .mvn
│   └── wrapper
│       └── maven-wrapper.properties
├── src
│   └── main
│       ├── java
│       │   └── com.beyn.pmo
│       │       ├── config
│       │       ├── controllers
│       │       ├── dto
│       │       ├── models
│       │       ├── repositories
│       │       ├── services
│       │       ├── utils
│       │       └── PmoApplication
│       └── resources
│           ├── static
│           ├── templates
│           └── application.yaml
├── test
├── target
├── .gitignore
├── HELP.md
├── mvnw
├── mvnw.cmd
├── pom.xml
└── users.http -------------------> ce fichier vas servir à tester nos requetes.
### Implementation
## Authentification 

