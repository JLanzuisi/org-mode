```{=org}
#+FILETAGS: :trab:
```
# EPUB de graham [[graham]{.smallcaps}]{.tag tag-name="graham"} {#epub-de-graham}

## [DONE]{.done .DONE} 0.1-testimonials: nuevo HTML para testimonials antes de la primera página {#testimonials-nuevo-html-para-testimonials-antes-de-la-primera-página}

## [DONE]{.done .DONE} 0.3-cover-art: se cambió toda la sección {#cover-art-se-cambió-toda-la-sección}

## [DONE]{.done .DONE} 13-human: cambios menores (no cambio nada) {#human-cambios-menores-no-cambio-nada}

## [DONE]{.done .DONE} all-vol-bibliography.bib {#all-vol-bibliography.bib}

## [DONE]{.done .DONE} Revisar meld e ir añadiendo diferencias {#revisar-meld-e-ir-añadiendo-diferencias}

## [DONE]{.done .DONE} Revisar con pagina epub checker {#revisar-con-pagina-epub-checker}

## [DONE]{.done .DONE} Subir al github {#subir-al-github}

## [DONE]{.done .DONE} Arreglar cap 6 {#arreglar-cap-6}

### Añadir imágenes usando calibre

### Si los cambios son demasiado grandes, intentar convertir tex en html

## [TODO]{.todo .TODO} Añadir cap 16 (y mover posteriores) {#añadir-cap-16-y-mover-posteriores}

### [DONE]{.done .DONE} TeX a html {#tex-a-html}

Usar pandoc para convertir de TeX a html. Quitar, antes de convertir,
todo lo que no tenga sentido en el epub (como index) y cualquier otra
cosas que prefiera hacer manualmente después (como añadir una imágen).

### [DONE]{.done .DONE} Añadir nuevo html al epub {#añadir-nuevo-html-al-epub}

Revisar que el epub funcione, es decir, que el capítulo aparezca donde
debería

### Referencias dentros del nuevo Cap

Hay que cambiar los ref y cite dentro del nuevo cap también hay que
añadir una imágen y una tabla

### +1 a los números de los cap

A partit del cap 15 hay que cambiar los números de los caps, añadiendo
1. 16 -\> 17, 17 -\> 18, etc

### Cambiar el indice

Tanto la sección de contenidos como el indice virtual del epub.

### Referencias

Hay que corregir la referencias y cualquier mención de números errados.

1.  [TODO]{.todo .TODO} Descargar *todos* los TeX

2.  Hallar referencias

    Usar grep para obtener todos los `\label` dentro de un cap, luego se
    pueden buscar todos los otros lugares en que aparece cada uno de
    esto `\label` (como argumento de un `\ref`, por ejemplo).

3.  Casos particulares

    -   Cap 17 Growing regenerative businesses and ecosystems: Existen
        varias referencias al cap 16
    -   Caps 18,19,20: No vi ninguna referencia nueva al comparar pdfs,
        es probable que no haya ninguna. De cualquier modo aparecerá en
        los grep.

### Referencias hechas con \"Page\" y similares

No hay páginas en un epub, cambiar esto

## Cosas útiles:

### pdfjam

La utilidad pdfjam de texlive se puede usar para juntar muchas paginas
en un solo scroll:
`pdfjam --nup 1x15 --papersize {"432pt,9720pt"} --outfile new-scroll.pdf new.pdf`

### separar pdfs

Separar los capítulos del pdf es útil para comparar. El siguiente script
lo use:

``` {.bash org-language="sh"}
#!/bin/sh

rm *
pdfseparate -f $1 -l $2 ../OLDMasterEinstein-Picasso-1.pdf %d.pdf
pdfunite *.pdf old.pdf
```

# Ori

## [DONE]{.done .DONE} Poner en el primer articulo bullet points en alguna parte. {#poner-en-el-primer-articulo-bullet-points-en-alguna-parte.}

# Otros

## [TODO]{.todo .TODO} Responder a optimate. Rellenar planilla. {#responder-a-optimate.-rellenar-planilla.}
