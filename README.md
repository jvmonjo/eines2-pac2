# PAC2

## Docs

### Guia d'estils

S'ha instal·lat stylelint i s'han importat els estàndards per a Sass. Com a nomenclatura s'ha procurat usar BEM

### Issues

He hagut de fer un downgrade de jQuery degut a aquest bug: https://github.com/twbs/bootstrap/issues/30553

El problema estarà arreglat en la versió 4.4.2 de Bootstrap que encara no està disponible

Al usar el patró de nomenclatura BEM, el stylelint em retorna l'error:
´´´
Selector should be written in lowercase with hyphens (selector-class-pattern)stylelint(selector-class-pattern)
´´´

Seguint la recomanació trobada a aquest issue obert a github https://github.com/simonsmith/stylelint-selector-bem-pattern/issues/36, ho he solucionat afegint aquesta regla al stylelint.json:

```
"rules": {
  "selector-class-pattern": null
}
```
