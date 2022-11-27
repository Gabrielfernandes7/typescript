# Começando com Typescript                 

Typescript é um superset sintático do Javascript com tipagem estática

## Compilador Typescript

Dentro de seu npm digite:
```shell
$ npm install typescript --save-dev
```
Para verificar se o Typescript está habilitado basta verificar em package.json:
```json
{
  "devDependencies": {
    "typescript": "^4.9.3"
  }
}
```

O compilador Typescript está instalado no diretório **node_modules** e pode ser utilizado com:
```shell
$ tsc <nome_do_arquivo.ts>
```
Dessa forma o arquivo Typescript é compilado gerando um arquivo Javascript

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" style="max-width: 30px;"/>
---->
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" style="max-width: 30px;"/>