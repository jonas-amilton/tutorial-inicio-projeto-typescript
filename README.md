1º Comando no terminal: "npm init -y" - Inicializa o repositório com o npm

2º Comando no terminal: "npm i -D typescript @types/node ts-node-dev" - Adiciona as dependências iniciais do projeto

3º Comando no terminal: "tsc --init" - Inicializa o tsconfig.json para configuração do uso do typescript

4º Modifica arquivo: tsconfig.json 
  - Altera versão do target para o que seu projeto utilizará;
  - Descomenta e adiciona o rootDir como (geralmente) "./src";
  - Descomenta e adiciona o outDir como (geralmente) "./build";
  - Adiciona antes do último fechamento de chaves ("}") o include e exclude, que é o que será respectivamente incluído e excluído da compilação dos arquivos;

5º Adiciona os seguintes scripts no package.json:
  - "dev": "tsnd | ts-node-dev --respawn --transpile-only --cls ./src",
  - "build": "tsc",
  - "start": "node ./build"