# [[Computação/Programação/JavaScript/Node.js/Node.js|Node.js]] - Executando Scripts
Depois de instalar o node, pode-se executar um arquivo ".js" com o comando de terminal `node <filepath>`:
```shell
node app.js
```

Pode-se também utilizar o [[TODO/Shebang|Shebang]]. Adicionando o comando seguinte como primeira linha do script, o Sistema Operacional automaticamente utilizará o node para executar o arquivo:
```javascript
#!/usr/bin/node

// Resto do código
```

> **OBS:** Em OS baseados em Unix é necessário dar permissão ao script para torna-lo executável: `chmod u+x app.js`

## Relacionado
- <https://nodejs.dev/en/learn/run-nodejs-scripts-from-the-command-line/>
- [[Computação/Programação/JavaScript/Node.js/Node.js|Node.js]]