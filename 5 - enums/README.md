# Enums

Enums é um tipo especial de classe que representa um grupo de constantes (variáveis imutáveis)

Os enums podem ser de dois tipos: *string* e *number*.

Você pode declarar apenas o primeiro valor numérico, e o restante será incrementado automaticamente.

```typescript
enum CardinalDirections {
    North = 1,
    East,
    South,
    West
}

// logs 1
console.log(CardinalDirections.North);

// logs 2
console.log(CardinalDirections.East)
```

## Numeric Enums - Fully Inicialized
Inicializar todos os enums
```typescript
enum StatusCodes {
    NotFound   = 404,
    Success    = 200,
    Accept     = 202,
    BadRequest = 400
}

// logs 404
console.log(StatusCodes.NotFound)
```

## Strigs Enums
```typescript
enum CardinalDirections = {
    North = 'North',
    East  = "East",
    South = "South",
    West = "West"
}

// log "North"
console.log(CardinalDirections.North)
```
***Observação***: Você poderia misturar *string* com *number*, porém não é recomendável.