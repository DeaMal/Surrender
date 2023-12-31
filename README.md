# Surrender, You're Surrounded
A game with random generation of the field and enemies, the task is to get to the exit while running away from enemies.

## Overview

A simple turn-based terminal game. All game elements are randomly generated. The size of the field, the number of walls and enemies are set by the user when starting the program. The user's task is to get to the exit by moving in four directions. Enemies move towards the user trying to catch him.

## Installation

    mkdir target

    javac -d target/ -sourcepath Game/src/main/java/ -cp Game/lib/\*  Game/src/main/java/edu/school21/game/app/Program.java ChaseLogic/src/main/java/edu/school21/chase/logic/*.java

    cp -r Game/src/main/resources/*.* target

    cd target
    jar xf ../Game/lib/jcommander-1.78.jar
    jar xf ../Game/lib/JCDP-4.0.2.jar
    rm -rf META-INF
    cd ..

    jar cmf Game/manifest.txt game.jar -C target .

    rm -rf target

    java -jar game.jar --enemiesCount=10 --wallsCount=10 --size=30 --profile=production

## Usage

To start playing, you need to follow the instructions above.
You can change the number of enemies, default is 10:

>--enemiesCount=10

number of walls inside the map, default 10:

>--wallsCount=10

map size, default 30:

>--size=30

game mode 'production' or debug mode 'dev'

>--profile=production

The user moves using the following keys:

`1 - left`\
`2 - down`\
`3 - right`\
`5 - up`\
`9 - give up`

In dev mode, all enemy movements must be confirmed by pressing the key `8`

You can customize the colors and appearance of the map by editing files:
- for dev mode

    Game\src\main\resources\application-dev.properties

- for production mode

    Game\src\main\resources\application-production.properties

Have a nice game!!!

![ScreenShot](screenshot.png)

## Remove

    rm game.jar