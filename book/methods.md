# Methods

Equijubus Camelotia Procompsognathus Sonorasaurus Xiaosaurus Trinisaura Urbacodon Maiasaura Microceratus Ligabueino Hylaeosaurus Palaeocursornis Sciurumimus Galvesaurus Hagryphus Venaticosuchus Utahceratops Texasetes Vectisaurus Mongolosaurus Kakuru Ruehleia Penelopognathus Colepiocephale Ornithotarsus Wuerhosaurus Xianshanosaurus Trigonosaurus Achillobator Erectopus Mononykus Shuangmiaosaurus Equijubus Razanandrongobe Ornithosuchus Jintasaurus Sinocalliopteryx Lurdusaurus Protarchaeopteryx Brachyceratops Callovosaurus Bissektipelta Luoyanggia Yulong Nedcolbertia Parrosaurus Comahuesaurus Nanningosaurus Parasaurolophus Altirhinus Amtosaurus Gigantoscelus Corythosaurus Pitekunsaurus Tarascosaurus Magnapaulia Siamosaurus Zupaysaurus Zigongosaurus Eolambia Karongasaurus Eshanosaurus Jenghizkhan Vectisaurus Helioceratops Echinodon Elmisaurus Parksosaurus Juratyrant Beishanlong Nuthetes Texasetes Chromogisaurus Equijubus Ammosaurus Heyuannia Nyasasaurus Xenoceratops Limnosaurus Arstanosaurus Mei Albertonykus Pseudolagosuchus Machimosaurus Longisquama Huanghetitan Bactrosaurus Tornieria Bainoceratops Dicraeosaurus Atlasaurus Euskelosaurus Cryolophosaurus Ekrixinatosaurus Dongyangosaurus Hypselorhachis Sonorasaurus Borogovia Chaoyangosaurus Protohadros. See [support from the fossil record](fossil-record) for more details.

## Install prerequisites

You can install the feather identification toolbox via `pip`:

    pip instal -U featherid

```{margin} Learn more
For a review of computer vision algorithms in paleontology see *Evolving Virtual and Computational Paleontology* by Luca Pandolfi, Pasquale Raia, Josep Fortuny and Lorenzo Rook. 
```

Then modify your script to locate feathers on pictures of dinosaur bones. This uses a complex computer vision algorithm [^computer-vision], the details of which are beyond the scope of this document.

[^computer-vision]: Computer vision is a class of algorithms that mimic human vision using a series of complex mathematical operations performed on digital images. Computer vision is nothing like human vision, but some computer vision algorithms can successfully identify hard to see features - like dinosaur feathers.

```python
import featherid as fid

for i, X in enumerate(files):
    Y[i] = fid.find(X)
```

```{warning}
Feathers are very difficult to identify in a fossil. Extreme care should be taken when distinguishing between a feather and other grit and debris that may be present.
```

## Calculating the hypotenuse
To calculate the hypotenuse, $z$, of a right triangle with sides of length $x$ and $y$ use the pythagorean theorem shown in equation {eq}`pythagorean`:

$$
z=\sqrt{x^2+y^2}
$$ (pythagorean)

## Average feather length
From a sample of 100 dinosaurs, the observed feather length was {glue:text}`avg:2.2f` (95% CI {glue:text}`lower:2.2f` / {glue:text}`upper:2.2f`). See {numref}`fig:random` for a correlation of feather length to bone diameter.

```{glue:figure} random-fig
---
name: "fig:random"
---
Feather length vs bone diameter (completely fictional data) for fossils analyzed with the feather identification toolbox (also fictional).
```

