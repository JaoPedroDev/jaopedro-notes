# [[Programação/JavaScript/Node.js/Node.js|Node.js]] - ESM
O sistema de módulos do ECMAScript gira em volta dos statements `import` e `export`.

Utilizamos o `export` quando queremos que uma função, variável, objeto, etc. possa ser importada e utilizada por outros arquivos:
```javascript
// Nome do arquivo: elements.js
// Exportando diretamente
export let string = "something";
export const number = 1515;
export var bool = true;
// Default define o elemento padrão exportado quando nenhum elemento for explicitamente solicitado
export default function defaultElement() {
	// CODE
}

// Exportando varios elementos
export { string, number, bool, exportedFunction};
```

O `import` é utilizado quando queremos acessar os elementos exportados de um arquivo:
```javascript
import defaultElement from "./elements.js";
import * as alias from "./elements.js";
import { string } from "./elements.js";
import {number as numeros} from "./elements.js";

// Podemos chamar a função importada
defaultElement();
```

## Relacionado
- [[Programação/JavaScript/Node.js/Node.js|Node.js]]
- [[Programação/JavaScript/Node.js/Node.js - NPM|Node.js - NPM]]