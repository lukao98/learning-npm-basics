#O que é NPM?

Npm vem da sigla Node Pack Manager (Gerenciador de Pacotes Node). Ele é um repositório online que serve para publicação de desenvolvimentos open source para o Node JS e também é um utilitário que faz a interação com esse repositório ajudando na instalação de pacotes, gerenciamento de versão e gerenciamento de dependências.  

##O que é dependência e o que é dependencia de desenvolvimento?  

Dependências são modulos que seu projeto necessita para rodar, enquanto denpendências de desenvolvimento são modulos que você utiliza para desenvolve-lo.  

- Dependência: request, concat-stream, object.assign...  

- devDependência: mocha, tape, eslint, grunt, browserify...  

####Modulos globais
Com o npm também podemos instalar um modulo global. Um modulo global tem a função de ser executado em linha de comando. Sua instalação é feita da seguinte maneira: `npm install --global nome` ou `npm install -g nome`

##O que é package.json  

É onde o npm gerencia, ou seja, é a raiz do seu projeto, onde está todas as informações, como por exemplo:  
- nome;  
- versão;  
- descrição;  
- autor;    
- licença;    
- dependências;    
Entre outros...  

##Exemplo de prática e algumas explicações  

Sempre quando vamos iniciar um projeto, utilizaremos o `npm init` para criar o **package.json** e inicializar o projeto preenchendo os dados requeridos.  

O comando `npm install` ou `npm i` vai servir para instalar algum modulo ou pacote.  

Suponha-se que você necessite abrir o mesmo projeto em locais diferentes, como fazer para para lembrar dos modulos? A resposta está nas dependências.  

####--save e --save-dev  

Ao instalar o utilizando o `--save` o mudolo será salvo em *dependencies* dentro do **package.json**, por exemplo:  

`npm i --save nome1`    

ficará salvo da seguinte maneira:   

```
"dependencies" : {
  "nome1": "^versão"
 }
```        
Caso seja uma dependência de desenvolvimento, utilizaremos um comando similar: `--save-dev`. O `--save-dev` salvará o modulo em *devDependencies* no **package.json**, por exemplo:  

`npm i --save-dev nome2`  

ficará salvo da seguinte maneira:    

```  
"devDependencies": {
  "nome2": "^versão"
 }
```

