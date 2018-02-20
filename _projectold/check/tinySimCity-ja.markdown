---
layout: post
title:  "Tiny SimCity"
tile-name: "Tiny SimCity"
thumbnail: "tinySimCity-ja.png"
author: "Javier Argota"
date:   2016-12-18

tags: python programming urban simulation
---

![Hero Image](/img/tinySimCity-ja/hero.png)

<iframe width="100%" src="https://www.youtube.com/embed/X44-5017v1Q" frameborder="0" allowfullscreen></iframe>


GENERAL DESCRIPTION

The purpose of this small tool is developing a simple and comprehensive simulator of urban settlements growth for being used to provide realistic urban backgrounds for design purposes: for inserting a building, for testing urban strategies, etc. The development of urban grids can match different patterns and the aim of this piece of software is replicate some of the patterns observed throughout different human settlements from different historical moments and different cultural contexts. This software tries to engage the user by causing the initialization of the urban development from inputs decided and chosen by the user. 
From the seeds created by the user on the canvas, different patterns can be created procedurally to build up an interconnected network of edges and nodes similar to the found in many human settlements around the world.

![output](/img/tinySimCity-ja/Sintitulo-ja-01.png) 


HELP TEXT (INSTRUCTIONS)

TinySimCity is a synthetic city builder which allows to create procedural random cities from scratch. The builder is divided in two different windows: the GUI window for guiding the process and the introduction of variables, and the map window where the output can be previewed.
The process has three steps, accurately informed by the interface. Before every step the user needs to set the input variable which will control the building process.
1. Street builder
Before press START, user needs to set the size of the city in pixels (which will be the size of the builder windows) and the minimum size of the city block. Then press START and the builder window will be opened and the network of streets will start to grow. By clicking on one of the ends of a street, it will be removed and a new one in a random direction will be created. If click happens in an empty part of the map, just a new street will be created.
2. Buildings placing
While streets are built, user can set the maximum number of buildings to be placed on the city. The buildings placing step is initiated when user press the "next" button on the GUI window when the street builder is running. In the GUI window displayed while the buildings are placed new buildings can be added if desired. Additional, clicking on any already placed building in the map.
3. 3D builder.
Once all the desired buildings are placed on the map, by clicking on the NEXT button on the GUI window the 3D, a Hejduk perspective of the city is built. Additionally, from the GUI window, the colors of the buildings shading can be changed, as well as the orientation of the view. Finally, the work can be saved and exported as a JPG image which will be saved in the script folder.

![output](/img/tinySimCity-ja/Sintitulo-ja-02.png)

ALGOTHMIC STRATEGY

TinySimCity is a small low resolution simulator of urban patterns which is able to render a synthetic procedural city.
The generation of the city is based on rules defined by the programation and on parameters decided by the user.

In a general level, the city generation is divided in three clear steps:

1. Ways builder. The proposed rules-based generation starts with three seed lines with random direction, which are used as based and reference for tracing the rest of the network by perpendicular trajectories. Lines grow until they collide with another line, with the only restriction of a minimum distance between new intersections, for keeping a feasible city block size.
Once the user decides the basic urban network is finished, it can initialize the following routine:
2. Buildings placing. Taking as reference the directions of the streets, random rectangles are created at random locations. Once created, they start to move in the map and to rotate until they find the right position, which is aligned with the streets and at a particular distance which is at least half of the way width. Basically, buildings cannot overlap other buildings or streets.
3. After all the required buildings are placed, finally a 3D perspective is built (actually it is a 2.5D perspective, a Hejduk perspective without reduction in the Z axis). The biggest challenge in this routine is actually figuring out the particular order of drawing in 2D for displaying accurately the different shapes in the right order. The main strategy is based in sorting according to the y coordinate value. Lower values should be drawn before.
Additionally the program allows at the end to save the drawn city as an image.


GRAPHIC USER INTERFACE

TinySimCity starts with a window for the user input and the menus. This floating window for menu is different than the actual windows for the city builder itself. Due to the variable resolution which can be used in the program, the strategy of the floating menus is chosen for making the most of the space on the screen. Furthermore, it avoids wasted space by blank areas. The menu changes its design in every step of the process of design, allowing to the user to enter the required parameters. As well, this menu window contains the help information. This way, the other window managed by the program, the canvas itself where the city is built, it is exclusively used for running the output of the coding. Another feature implemented in the GUI is having the possibility of navigate back and forwards through any step and correcting and changing your decisions during the building process.


