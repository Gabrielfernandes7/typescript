# Tuplas

é um tipo de array pre-definido com tamanho e tipo para cada índice. Por exemplo:
```typescript
// definimos nossa tupla
let ourTuple: [number, boolean, string];

// inicializamos corretamente
ourTuple = [5, false, 'Typescript']
```

**Observação**: Inicializar a tupla com ordem incorreta o Typescript irá jogar um erro.

## Readonly Tuple

Uma boa prática é definir sua tupla com *readonly*

```typescript
const ourReadonlyTuple: readonly [number, boolean, string] = [5, true, 'Typescript'];
```

## Nomear Tuplas

```typescript
const graph: [x: number, y: number] = [90.4, 48.8];
```
Nomear as tuplas fornece mais contexto para o que os nossos valores do índice representam

## Destructuring Tuples

```typescript
const graph: [number, number] = [44.5, 67.3];
const [x, y] = graph;