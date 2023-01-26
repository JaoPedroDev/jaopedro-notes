# [[Node.js]] - Sistemas de Módulos
Atualmente no desenvolvimento de software, módulos organizam o código em vários pedaços que fazem uma tarefa especifica, e que juntos formam aplicações mais complexas.

No navegador, o [[../JavaScript|JavaScript]] importa e exporta seus módulos através do [[Node.js - ESM]], que utiliza os statements `import` e `export` respectivamente.

Porem, no [[Node.js]] é utilizado o CommonJS como sistema de módulos padrão, carregando módulos com o `require()` e exportando com o `module.exports`.

É possível mudar o sistema de módulos do [[Node.js]] para usar o mais atual ESM. Basta adicionar a propriedade `type: "module"` ao *package.json*. Exemplo:
```json
{
  "name": "app",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "type": "module", // Tipo de sistema de módulo
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
  }
}
```

# Relacionado
- [[Node.js]]