# POO_Reto_02

### Soy Malcom Yamil Carrillo Quintero y pertenezco al grupo de "Fenomenoides", adelante se muestra nuestro logo
<details><summary>Preparense para ver el grandioso logo: </summary><p>
<div align='center'>
<figure> <img src="https://i.postimg.cc/NFbwf57S/logo-def.png" alt="Logo Fenomenoides" width="400" height="auto"/></br>
<figcaption><b> "somos programadores, no diseñadores" </b></figcaption></figure>
</div>
</p></details><br>


## Diagrama de clases.
### Caso: Hunger Games

Como una saga de libros y peliculas que me gustan decidí realizar el diagrama de clases realizando la abstracción del evento de los juegos del hambre en sí y sus elementos clave junto con sus posibles atributos y metodos. 

Como estos elementos pertenecen a los juegos este diagrama contiene composición en su mayoría
```mermaid
classDiagram
    HungerGames *-- Arena
    HungerGames *-- Tributes
    HungerGames *-- Sponsors
    HungerGames *-- GameMaker
    Arena *-- Pods

    Arena<--GameMaker:updateState()
    Pods<--GameMaker:activatePod()
    Tributes<--Sponsors:giveGift()
    HungerGames<--GameMaker:setState()

    HungerGames : +Edition
    HungerGames : +ArenaCondition
    HungerGames : +Theme
    HungerGames : +Duration
    HungerGames:  +isQuarterQuell()
    HungerGames:  +hasWinner()
    HungerGames:  +isCompleted()
    HungerGames:  +updateArena()
    class Tributes{
      +testScore
      +Weapon
      +SurvivalSkill
      +PhysicalState
      +Allies
      +Icon
      +Attack()
      +Hunt()
      +Rest()
      +allyTribute()
      +Heal()
      +setSnare()
    }
    class Sponsors{
      +Resources
      +sponsor()
      +hasFavourite()
    }
    class Pods{
      +Elements
      +Trap
      +Hazards
      +Activators
      +Criatures
      +activate()
      +automaticallyStart()
    }
    class Arena{
      +Weather
      +Resources
      +Temperature
      +Dynamic
      +Humidity
      +Traps
      +Limits
      +Time
      +changeCycle()
      +DynamicActive()
      +soundCannon()
      +playMessage()
    }
    class GameMaker{
      +Plans
      +deadliness
      +Orders
      +rank
      +desginArena()
      +designPod()
    }
```

En esta otra parte se evidencia la herencia de los "objetos" de los juegos que son ciudadanos
```mermaid
classDiagram

    Tributes --|> Citiziens
    Sponsors --|> Citiziens
    GameMaker --|> Citiziens

    class Citiziens{
      +Name
      +Age
      +District
      +Hunger
      +Thirst
      +HealthState
      +Tiredness
      +Job
      +eat()
      +drink()
      +sleep()
      +talk()
      +work()
    }
    class Tributes{
      +testScore
      +Weapon
      +SurvivalSkill
      +PhysicalState
      +Allies
      +Icon
      +Attack()
      +Hunt()
      +Rest()
      +allyTribute()
      +Heal()
      +setSnare()
    }
    class Sponsors{
      +Resources
      +sponsor()
      +hasFavourite()
    }
    class GameMaker{
      +Plans
      +deadliness
      +Orders
      +rank
      +desginArena()
      +designPod()
    }
```
