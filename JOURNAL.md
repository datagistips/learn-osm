## 8 Août 2024

### Notes

multiuse => footway=path
wicket_gate

[surveillance](https://wiki.openstreetmap.org/wiki/FR:Tag:man_made%3Dsurveillance)

### Coller à la même position

ctrl + alt + V

### 32 - Mapper des trottoirs pour l’accessibilité

https://peertube.openstreetmap.fr/w/hD9m929abQqKctgw3nnjV8
80% handicaps invisibles
**sidewalker**
import graphe piéton
cheminements piétons au format **netex**
plans de corps de rue
traversées piétonnes, bordures, obstacles
**application accès libre mobilités**
junglebus sidewalker
**OSMarche**
itinéraires prioritaires
dévers, pente
bâton de randonnée
module d'import de graphe filaire dans OSM
plans de corps de rues très précis
sidewalk=both, sidewalk=right, sidewalk=left
step_count

### 8 - Cartographier les zones climatiques locales avec OpenStreetMap

geoclimate
https://peertube.openstreetmap.fr/w/oG5Ji4Vxn9eSABvG8TLgdQ
ICU souterrain, ICU de surface, ICU atmosphérique, ICU de canopée urbaine
rues canyons
profil de vent d'un quartier
geoclimate
indicateurs géographiques
modélisation
planification
OSM, BDTOPO v2
Pas vu jusqu'au bout
H2GIS
Groovy

### PCRS

https://peertube.openstreetmap.fr/w/xryYzTDDesnPKWgkqdntKF
10 cm de précision
images 5 cm
arbres contours de bâtiments
prestataires caméras, photos
pcrs image + (ou pas) pcrs vecteur
obligation à se servir en 2026
suivi pcrs
ne suivent pas les contours admin.
zone bleue, images rectifiées
200 M euros sur tout le pays
IA via téléchargement des images
accesibilité de la voirie
mesure de voie routière
mesure de voie cyclable
marquage horizontal et vertical
obstacles
positionnement d'adresses
entrées parkings piétons
inventaire de poteaux, etc...
pérennité des infrastructures
plans ETARE
soutien opérationnel et pistes
réservoirs, bassins, moyens de lutte contre l'incendie
volumes des citernes

### JOSM - 10 raccourcis pour se mettre bien feat. PopCat

https://www.youtube.com/watch?v=R4lHkhWHkkE
Alt+A
mollette de la souris + Ctrl : sélectionner objet en dessous
**Maj B intervalles réguliers**
appuyer 2 fois sur A => angles
**approcher un chemin : N**
**suivre un chemin : F**

## 7 Août 2024

https://learnosm.org/fr/josm/josm-tools/

- Sélectionner le chemin puis le noeud => couper le chemin
- Séparer les chemins pour disjoindre
- Shift + ctrl pour pivoter, Alt+Ctrl pour mettre à l'échelle
- [Création de préréglages en XML](https://learnosm.org/fr/josm/creating-presets/)
- Pour la fontaine de la Rotonde : ligne > Cercle > Puis copie mise à l'échelle alt+ctrl
- inner outer : multipolygone (outils > créer un multipolygone
- relations :
  - multipolygone
  - routes
  - limites
  - restrictions
- Edit > Preferences > Imagery pour ajouter une imagerie
- wms.openstreetmap.fr > FR - PACA 13 2009
- https://wiki.openstreetmap.org/wiki/FR:Serveurs/wms.openstreetmap.fr
- noeuds du milieu, noeuds du chemin, noeuds adjacents, sélectionner les noeuds du chemin
- Notes OSM

### Pedestrian Navigation Guidelines

https://wiki.openstreetmap.org/wiki/Guidelines_for_pedestrian_navigation

pedestrian
**shared** ways
**foot**=* https://wiki.openstreetmap.org/wiki/Key:foot
highway=cycleway, foot=yes
segregated
pedestrian crossing : highway=footway, footway=crossing
highway=**crossing**
shared way : highway=*, sidewalk=right/...
**kerb**=* (on on a node at exact location where a highway crosses the kerb) (voir opensidewalks tuto youtube)
**tactile_paving**=* (à voir)
**sidewalk:both=separate** if mapped separately
**sidewalks style**
incline
not share a node between bridge and ways below, between, or above
**barrier**=*
indoor mapping (à voir)
area=yes
highway=pedestrian area=yes
pedestrian areas contiguous must share nodes
**barrier=kerb for sidewalk**
**barrier=fence = linear**
**crossing point : barrier=gate**
barrier=entrance (opening)
access : foot=*, wheelchair=*
exit referenced : **ref=***

### Suite

- https://wiki.openstreetmap.org/wiki/Key:kerb

- Edition > préférences > coloriage > sidewalks
- Arbres et plantnet : https://mapcomplete.org/trees.html?z=18&lat=43.9462647000006&lon=4.8013476999983595#theme-menu:intro

### Plugins

- terracer terraces duplexes
- fastdraw click click
- utilsplugin2

cf https://www.reddit.com/r/openstreetmap/comments/vuvlrw/what_are_some_useful_josm_plugins_you_use/



### Suite

- footway = crossing/traffic_island/sidewalk (https://wiki.openstreetmap.org/wiki/Tag:footway%3Dtraffic_island)
- crossing (https://wiki.openstreetmap.org/wiki/Key:crossing)
- crossing:island (https://wiki.openstreetmap.org/wiki/Key:crossing:island)

## 6 Août 2024

OpenSideWalks

```
### Description

Note: Please map crossings before sidewalks!

We need to add crossing data before we map sidewalks, because mapping sidewalks all by themselves can 'break' the map if they aren't connected to anything! Street crossing provides a means by which sidewalks will be connected to the street network, ensuring that pedestrian data is never in a "broken" state.

Street crossing locations are very important to map out! They include information on where to cross, whether there are markings (like a crosswalk), whether a pedestrian will have to deal with raised curbs or can use curb ramps, and provides a connection to the street network for fallback or alternative modes of travel.

Please refer to [this spreadsheet](https://docs.google.com/spreadsheets/d/1yrZR3_gLBrndYEXGyGS-klnGVyNN9BpE/edit?usp=sharing&ouid=115962062106666304635&rtpof=true&sd=true) to review the types of pedestrian environment features and their related tags that have been adopted in support of the [OpenSidewalks](https://www.opensidewalks.com/) initiative.

If this is your first time contributing to the OpenSidewalks initiative, please review [the OpenSidewalks Mapping Guide](https://drive.google.com/file/d/17jaOMMU2FtfSvV46r_kgIeHs2SzKNHW9/view?usp=sharing), before proceeding to map.

We advise that you base your mapping choices on Bing Aerial satellite images. You can also use [Mapillary](https://www.mapillary.com/) and [Karta View](http://www.kartaview.org/) to access street side images to help inform your mapping decisions.

By mapping out this information, you will be contributing to a global, open dataset of pedestrian pathways that can be used by anyone to create pedestrian routing applications, create analyses used for advocacy work, and provide an extensible basis for more detailed mapping of pedestrian spaces.



Rules For Mapping Crossings

Crossings describe the path a pedestrian can take to cross a street. These are essential for connecting the pedestrian network across streets and to the streets themselves as well.

Crossings are lines (ways in OpenStreetMap).

Crossings are drawn only on the surface of streets: they should not be drawn on top of sidewalks.

Crossings should always start and end with curb nodes.

Crossings are always tagged with “highway=footway, footway=crossing”. These tags will be added automatically with the iD presets described below.

Crossings can be of two types: “marked” and “unmarked”.

- Marked (crossing=marked). A “marked” crossing is one with lines on the ground showing where a pedestrian can cross and is (likely) protected to cross. The iD preset in English is "marked crosswalk".
- Unmarked (crossing=unmarked). An "unmarked" crossing is one where a crossing is implied but lacks ground markings, which is usually at most intersections. The iD preset in English is “unmarked crossing".

Crossings are always connected to the street(s) they cross. This guarantees connectivity with the larger street network, preventing us from accidentally breaking routing software.

Crossings may be enriched with some optional tags. Please consider waiting on adding this information on the first pass, as we just want the core network established ASAP. Those tags are:

- surface=* (surface composition)
- tactile_paving=yes/no (whether the crossing itself has tactile surfaces to aid the blind et al)
```



## 1er Août 2024

- https://www.openstreetmap.org/#map=18/43.53766/5.45589
- [natural](https://wiki.openstreetmap.org/wiki/FR:Key:natural)
  - wood
  - heath
  - grassland
- produce
  - xxx
- leisure
  - [park](https://wiki.openstreetmap.org/wiki/Tag:leisure%3Dpark)
  - [garden](https://wiki.openstreetmap.org/wiki/Tag:leisure=garden)
    - garden:type
  - forest
    - https://help.openstreetmap.org/questions/324/when-should-we-use-landuseforest-rather-than-naturalwood
- traffic_calming
  - bump
- leaf_type
  - needleleaved
- landuse
  - greenery
  - flowerbed
    - greenery
- lamp_mount
  - bend_mast
- highway
  - street_lamp
    - lamp_mount
      - bollard
      - bent_mast
      - straight_mast
  - footway
  - lit
- emergency
  - fire_hydrant
    - fire_hydrant:type
      - pillar
- entrance
  - yes
  - main
- wheelchair
- building
  - entrance
- amenity
  - bench
    - back_rest
  - recycling
    - recycling:newspaper=yes
  - waste_disposal
  - waste_basket
  - parking
    - capacity
  - motorcycle_parking
- material
  - wood
- recycling:green_waste
  - yes
- waste
  - organic
    - https://forum.openstreetmap.fr/t/borne-de-compostage/11108
- building
  - house
  - villa
  - building:levels
- outdoor_seating
- surface
  - ground
  - asphalt
- [waste](https://wiki.openstreetmap.org/wiki/Key:waste)

## 31 Juillet 2024

- https://wiki.openstreetmap.org/wiki/FR:Bonnes_pratiques
- https://wiki.openstreetmap.org/wiki/Editing_Standards_and_Conventions
- Mode Parallèle
- Séparer du chemin
- Fusionner les noeuds
- Mode extrusion
  - Double clic
  - Shift
  - Ctrl
  - Alt
- Télécharger > Saisir une adresse > Puis télécharger la zone
- Shift dans la fenêtre des clés
- Fontaine Pascal
  - Coller les attributs de la sélection précédente
- Plugin opendata
- Raccourcis
  - Touche A
  - Touche S
  - Maj R pour copier les attributs
- Rendre une forme orthogonale