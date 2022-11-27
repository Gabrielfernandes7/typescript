# Typescript Interface e Aliases

## Type Aliases

Type aliases (tipos de apelido) permitem que definimos um tipo com um nome.

```typescript
type input = number | string; // tipo que eu crieio

function sumValues(input1: input, input2: input){
    if(typeof input1 === "string" || typeof input2 === "string"){
        return input1.toString() + input2.toString();
    } else{
        return input1 + input2;
    }
}

// somar valores
console.log(sumValues(2.5, 5.4));
```

Aliases podem se utilizados com tipos de dados simples também com os mais complexos, como: arrays e objects.

```typescript
type CarYear = number
type CarModel = string

type Car = {
    year: CarYear,
    model: CarModel
}

const carYear: CarYear = 2024;
const carModel: CarModel = "Corolla"
const car: Car = {
    year: carYear,
    model: carModel
}

```

## Interfaces
Interfaces são similares aos aliases, mas eles só se aplicam a objects.

```typescript
interface Square{
    l: number
}

const square : Square = {
    l: 30
};
```

## Extending interfaces
Significa que você criou uma npva interface com as mesmas propriedades que a a interface pai e adicionou algo novo (herança).
```typescript
interface Square{
    l: number
}

interface ColorSquare extends Square {
    color: string
}

const coloredSquared: ColoredSquare = {
    l: 30,
    color: "red"
}
```