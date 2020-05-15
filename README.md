# PAC2

## Guia d'estils

S'ha instal·lat stylelint i s'han importat els estàndards per a Sass. Com a criteri de nomenclatura de les classes s'ha usat BEM

## Dependències externes

He instal·lat FontAwesome i Bootstrap com a dependències externes:

```
npm i --save @fortawesome/fontawesome-free bootstrap
```


## Pàgines:

### Portada

Per a la portada s'ha fet ús de CSS Grid amb @supports oferint una versió flex com a alternativa.

### Repartiment

Per a la pàgina del repartiment he creat un layout de graella usant flex. Per a mantenir 3 ítems per fila a pantalles suficientment grans he fet que els ítems tinguen una amblada de 28vw i un marge entre ítems de 0.5vw, a més a més d'un comportament wrap quan no capiguen més ítems a la fila. En pantalles mitjanes s'ha optat per una amplada per ítem de 40vw per facilitar la cabuda de 2 items per filera. En pantalles més petites s'ha optat per una amplada de 95vw per a facilitar un layout vertical d'una sola columna. El media query s'ha fet usant els mixins disponibles a bootstrap en pro d'una integració entre els breakpoints de bootstrap i els estils personalitzats.

### Article

L'article està contingut dins d'un element article. Per a les cites he usat l'element blockquote. Per a les llistes ordenades he customitzat el contador numèric amb CSS per a adapatar-lo a l'estil proposat pel wireframe.


### Contacte

S'ha usat un formulari de Bootstrap per a integrar Netlify forms i poder habilitar així l'enviament real de missatges de contacte.

## Issues

- He hagut de fer un downgrade de jQuery degut a aquest bug: https://github.com/twbs/bootstrap/issues/30553

El problema estarà arreglat en la versió 4.4.2 de Bootstrap que al moment de fer aquest exercici no està disponible a la branca estable.

- Al usar el patró de nomenclatura BEM, el stylelint em retorna l'error:
´´´
Selector should be written in lowercase with hyphens (selector-class-pattern)stylelint(selector-class-pattern)
´´´

Seguint la recomanació trobada a aquest issue obert a github https://github.com/simonsmith/stylelint-selector-bem-pattern/issues/36, ho he solucionat afegint aquesta regla al stylelint.json:

```
"rules": {
  "selector-class-pattern": null
}
```

- També m'he trobat amb aquest problema tan prompte com he afegit pàgines addicionals al projecte: https://github.com/parcel-bundler/parcel/issues/1315

Com a _workaround_ he hagut de canviar l'estructura del projecte de 'pagina/index.html' a 'pagina.html'.

## Validació

La web s'ha validat en els següents estàndards:

- CSS3: https://jigsaw.w3.org/css-validator/
- HTML5: https://validator.w3.org/
- Accessibility Review (Guidelines: WCAG 2.0 (Level AA)): https://achecker.ca/checker/index.php

## Publicació i codi font
La web s'ha publicat a https://eines2-pac2.netlify.app i el codi font està allotjat a https://github.com/jvmonjo/eines2-pac2