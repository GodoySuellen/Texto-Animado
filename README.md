## Texto Animado

### Dependências

1. Copie para seu repositório os arquivos disponíveis nesta pasta: `assets/vendor/typed.js/typed.min.js`
2. No seu arquivo `main.js` adicone a função: 
``` 
(function() {
  "use strict";
  
  const select = (el, all = false) => {
    el = el.trim()
    if (all) {
      return [...document.querySelectorAll(el)]
    } else {
      return document.querySelector(el)
    }
  }
  
  /**
   * Hero type effect
   * Dependência: assets/vendor/typed.js/typed.min.js
   */
  const typed = select(".typed");
  if (typed) {
    console.log(typed)
    let typed_strings = typed.getAttribute("data-typed-items");
    console.log(typed_strings)
    typed_strings = typed_strings.split(",");
    new Typed(".typed", {
      strings: typed_strings,
      loop: true,
      typeSpeed: 100,
      backSpeed: 50,
      backDelay: 2000,
    });
  }

})()
```
3. Não esqueça de importar os arquivos no seu `index.html`

# Voilà
![animate](texto_animado.gif)


