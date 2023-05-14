# Tutorial de como iniciar um projeto em TypeScript

1º Comando no terminal: "npm init -y" - Inicializa o repositório com o npm

2º Comando no terminal: "npm i -D typescript @types/node ts-node-dev" - Adiciona as dependências iniciais do projeto

3º Certifique-se de ter o TypeScript instalado globalmente no seu sistema. Para instalar globalmente, você pode executar o seguinte comando no terminal:

``
npm install -g typescript
``

4º Modifica arquivo: tsconfig.json

Crie o arquivo tsconfig.json na raiz do projeto se ele ainda não existir

- Alterar versão do target para a que seu projeto utilizará
````
// exemplo:

"target": "es2022"
````
- Descomentar e adicionar o rootDir como (geralmente) "./src"
````
// exemplo:

"rootDir": "./src"
````
- Descomentar e adicionar o outDir como (geralmente) "./build"
````
// exemplo:

"outDir": "./build"
````
- Adicionar antes do último fechamento de chaves o include e exclude, que é o que será respectivamente incluído e excluído da compilação dos arquivos
 ````
 // exemplo:
 
  "include":["./src/**/*.ts"],
  "exclude":["node_modules"]
 ````

5º Adiciona os seguintes scripts no package.json:

````
"dev": "tsnd | ts-node-dev --respawn --transpile-only --cls ./src",
"build": "tsc",
"start": "node ./build"
````

6º Após isso você pode criar uma pasta src na raíz do projeto e incluir uma pasta index.ts

- Para executar basta usar o comando npm run dev no terminal
