## Typescript tipos simples de variáveis
- number
- string
- boolean

Existe duas maneiras de se criar variáveis com Typescript

- Explicíto:
```typescript
let firstName: string = "Fulano";
```

- Implícito
```typescript
let firstName = "Fulano";
```
**Observação**: neste segundo caso o ypescript irá inferir o valor de acordo com o valor atribuído a variável.

## Typescript tipos especiais de variáveis
- any
- unknown
- never
- undefined & null

Aqui será explicado os tipos de variáveis mais usuais

**Type any**

*any* é tipo de dado disabilita a checagem de tipo na variável e permite todos os tipos de dados para ser utilizado.
```typescript
let v: any = true;
```

**Type unknown**

*unknown* é uma alternativa ao tipo *any*, porém mais segura. O Typescript irá evitar de utilizar os tipos unknown. 

```typescript
let w: unknown = 1;
w = "string"; // nenhum erro

w = {
    runANonExistentMethod: () => {
        console.log("Penso, logo existo");
    } as {runANonExistentMethod: () => void}

    if(typeof w === 'object' && w !== null){
        (w as {runANonExistentMethod: Function}).runANonExistentMethod();
    }
}
```

***Observação***: o tipo unknown é o melhor tipo de dado para ser utilizado quando você não sabe o tipo de dado a ser tipado. Para utilizar um tipo depois você precisará utilizar *casting* (quando você utiliza a keyword *as* para dizer a propriedade ou da uma tipagem para variável).