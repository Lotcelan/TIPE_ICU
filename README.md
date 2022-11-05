# Projet de TIPE

# Objectifs

Etudier l'impact qu'ont les ICU sur la température d'une masse d'air.

# Utilisation

## Simulation

Compiler le fichier main.c en changeant les paramètres dedans selon ce que l'on veut : `gcc main.c -o main -lm`

## Exploitation

Cela produira alors plusieurs fichiers (selon les noms mis en paramètres) :
  
  -> air_temp.tipe : contient chaque température de chaque subdivision de l'air à chaque itération
  
  -> air_temp_last_first.tipe : contient les mêmes informations mais seulement pour la première et dernière itération
  
  -> masses_last_first.tipe : de même avec les masses

On peut alors :
  1. **Visulaiser** chaque étape avec `python visualisation_toutes_frame_3d.py` (en changeant les paramètres au préalable)
  2. **Calculer la variation d'enthalpie** avec `python calcul_enthalpie.py` (en changeant les paramètres au préalable)


# Exemples

## Simulation

### Une simulation quelconque
https://user-images.githubusercontent.com/40437798/199306062-3a0c620a-3d06-47d7-8765-4789a2dc9178.mp4

## Exploitation

### Variation d'enthalpie

- Différentes configurations avec les mêmes coefficients de convection et de diffusion (et `offset_floor` = `offset_l_wall` = `offset_r_wall`)

![graphe](./assets/K%3D3000_D%3D0.03_all_same_offset.png)

# TODO

## Tests

- Faire un système de test (calcul d'enthalpie pour plusieurs systèmes ...)

## Simulation

- Possibilité de customiser plus précisément que par un `offset` les températures du sol et des murs
