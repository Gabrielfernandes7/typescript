# Functions

## Return type
O tipo de valor que a função retorna pode ser definido, como no exemplo abaixo

```typescript
function ageUser(): number{
    // code
}
```

***Observação***: o tipo *void* é quando a função retorna *any*

```typescript
function printHello(): void{
    // code
}
```

## Parâmetros
Os parâmetros de uma função no Typescript são tipados

```typescript
function multiply(a: number, b: number){
    return a * b;
}
```

## Parâmetros opcionais
Por definição Typescript irá exigir a tipagem dos parâmetro, mas colocando o operador '?' pode explicitar como opcional

```typescript
function add(a: number, b: number, c?: number) {
  return a + b + (c || 0);
}
```

## Default parameters
para parâmetros com valores padrão, o valor padrão vai após a anotação de tipo:
```typescript
function pow(value: number, exponent: number = 10) {
  return value ** exponent;
}
```
Typescript pode inferir o valor padrão.

## Named Parameters

Tipando os parâmetros nomeados seguem o mesmo padrão como a tipagem normal de parametros

```typescript
function divide({ dividend, divisor }: { dividend: number, divisor: number }) {
  return dividend / divisor;
}
```

## Rest Parameters

Rest parameters pode ser tipado como os parâmetros normais, mas o tipo deve ser no array como rest parameters
```typescript
function add(a: number, b: number, ...rest: number[]) {
  return a + b + rest.reduce((p, c) => p + c, 0);
}
```

## Type Alias

Os tipos de função podem ser especificados separadamente das funções com aliases de tipo.

```typescript
type Negate = (value: number) => number;

const negateFunction: Negate = (value) => value * -1;
```
