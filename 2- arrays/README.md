# Typescript Arrays

```typescript
const names: string[] = [];
names.push("Fulano")
```

## Readonly
O readonly evita que os arrays sejam mudados

```typescript
const names: readonly string[] = ["fulano"];
```

## Tipo inferência

```typescript
const numbers = [1, 2, 3]; // inferência de tipo: number

numbers.push("2");
```
Neste caso é gerado um erro, pois o Typescript entendeu que o array é composto por números, portanto uma *string* não foi bem vinda.

mensagem de erro: *"O argumento do tipo 'string' não é atribuível ao parâmetro do tipo 'number' "*