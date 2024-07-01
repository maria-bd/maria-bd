
# PMO - Documentation Backend avec Spring Boot

## Objectif

**PMO** est une application web qui vise à centraliser et uniformiser la gestion de projets, améliorer la visibilité globale et faciliter le reporting au niveau de la BU Project de Beyn.

## Prérequis
Pour construire et exécuter l'application, vous aurez besoin de :

- Postgres 16.3

- pgAdmin 4

- java 21

- Spring boot 3.2.7

- Intellij IDE (pour: code et requetes)

## Initialisation 

### Création du projet

Apres l'installation de postgres/pg admin/ java 21 et Intellij on ouvre Intellij est on choisit: **New Project**

![image](https://github.com/maria-bd/maria-bd/assets/135654272/de512f24-412e-4304-be65-268baf440f71)

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
## Database Connection 
Pour mettre en place a base de donner suivez les étapes dans les captures
- Chosir une source Postgresql
![image](https://github.com/maria-bd/maria-bd/assets/135654272/2eb3ff46-17a0-49b7-aab0-abedc9f05df7)
- Donnez un nom à votre schéma et a votre base de donner (par défaut le mot de passe pour postgres est postgres)
 ![image](https://github.com/maria-bd/maria-bd/assets/135654272/236e26ee-d989-488d-adbb-12bc2c069e21)
- clicker dur test Connection est si tout est bon clicker sur apply pour la creer
- afficher tout les schémas de la BD on choisissant All Shemas
![image](https://github.com/maria-bd/maria-bd/assets/135654272/504116c5-4e27-47d9-b5bc-ec337fd341fa)
- Modifier le fichier application.properties :
   - renommer le fichier : application.yaml
   - ajouter ce code pour faire la liaison avec la BD :
  ```bash
  spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/pmo_db
    username: postgres
    password: postgres
    driver-class-name: org.postgresql.Driver
  jpa:
    hibernate:
      ddl-auto: create
    database: postgresql
    database-platform: org.hibernate.dialect.PostgreSQLDialect
  ```
### Implementation
## Authentification 

