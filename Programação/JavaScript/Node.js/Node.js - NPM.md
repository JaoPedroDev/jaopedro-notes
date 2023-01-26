# [[Node.js]] - NPM
NPM é o gerenciador de pacotes padrão do Node.

[Yarn](https://classic.yarnpkg.com/en/) e [Pnpm](https://pnpm.io/)(Recomendo 👍) são gerenciadores de pacotes alternativos para o Node.

## Instalando dependências
O NPM controla os downloads das dependências dos projetos, se  há um `package.json` na pasta do projeto, basta rodar o seguinte comando para baixar todas as dependências:
```shell
npm install
```

## Instalando novos pacotes
Basta especificar o nome do pacote:
```shell
npm install <package-name>
```

Esse comando também adiciona o pacote instalado ao `package.json` como uma dependência.

## Atualizando pacotes
Para atualizar todos os pacotes de um projeto:
```shell
npm update
```

Para atualizar um pacote especifico:
```shell
npm update <package-name>
```

## Relacionado
- [[Node.js]]