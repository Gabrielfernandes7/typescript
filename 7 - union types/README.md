# Union Types

## Union | (OR)
Utilizamos o | para dizer que nosso parâmetro é *string* ou *number*

```typescript
function printStatusCode(code: string | number){
    console.log(`My satus code is: ${code}`)
}

printStatusCode(404);
printStatusCode('404');
```