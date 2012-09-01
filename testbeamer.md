
<!---
 Creació de presentacions beamer des de markdown
 De markdown a beamer
 Joan Queralt Gil
 CataLàTeX
 1 de setembre de 2012
--> 

<!--
	Si només hem de crear el fitxer tex no posem pàgina de títol 
	Però si passem de markdown a beamer cal descomentar les línies següents:

 % Creació de presentacions beamer des de markdown
 % De markdown a beamer
 % Joan Queralt Gil
 % CataLàTeX
 % 1 de setembre de 2012
-->



# Objectius

## Objectius
Els **objectius** d'aquest presentació són:

> * Provar *pandoc* per passar de `markdown` a `beamer`.
> * Estudiar el procés.
> * Introduir personalitzacions.
> * Publicar el resultat a [cataLàTeX](http://phobos.xtec.cat/jqueralt)

# Procediment

## Primer pas
1. Crear un document de text en format *markdown* anomenat `test.md`
2. Els títols de Nivell 1 (`#`) seran les seccions de la presentació.
3. Els títols de Nivell 2 (`##`) seran els títols de les diapositives.

Sintaxi markdown:
<http://daringfireball.net/projects/markdown/>

## Segon pas
* Preparar un fitxer `matriu.tex` amb les especificacions per beamer.
* Que cridi a fitxer `test.tex` on hi haurà el contingut de les diapositives.

Documentació de Beamer:
<http://ctan.org/beamer>

## Tercer pas
* Fer que *pandoc* transformi `test.md` en `test.tex`

Comandament de pandoc:

 `pandoc test.md --slide-level 2 -t beamer -o test.tex`

## Quart pas
* Crear el document PDF de la presentació.

Comandament de LaTeX:

`pdflatex matriu.tex`

## Pas alternatiu
* Fer el pas directament des de pandoc.

Comandament de pandoc:

`pandoc --toc --slide-level 2 -V theme:NomTema -t beamer test.md -o test.pdf`

# Resultat

------------------

\centering\includegraphics[scale=0.4]{fitxer.jpg}

## Resultat
El que esteu veient.

## Crèdits
Idea original: <https://github.com/jeromyanglim>

Imatge amb llicència CC de [FlicrCC](http://flickrcc.bluemountains.net/flickrCC/index.php)
