---
id: 587d7b87367417b2b2512b41
title: Dichiarare una variabile di sola lettura con la parola chiave const
challengeType: 1
forumTopicId: 301201
dashedName: declare-a-read-only-variable-with-the-const-keyword
---

# --description--

La parola chiave `let` non è l'unico nuovo modo per dichiarare le variabili. In ES6, puoi anche dichiarare variabili usando la parola chiave `const`.

`const` ha tutte le fantastiche caratteristiche che ha `let`, con il il valore aggiunto che le variabili dichiarate utilizzando `const` sono di sola lettura. Esse sono un valore costante, il che significa che una volta assegnata una variabile con `const`, non può più essere riassegnata:

```js
const FAV_PET = "Cats";
FAV_PET = "Dogs";
```

La console mostrerà un errore a causa della riassegnazione del valore di `FAV_PET`.

Dovresti sempre dichiarare le variabili che non vuoi riassegnare usando la parola chiave `const`. Questo aiuta quando nel caso dovessi tentare accidentalmente di riassegnare il valore a una variabile che è destinata a rimanere costante.

Una pratica comune quando si dà il nome alle costanti è usare tutte le lettere maiuscole, separando le parole con un underscore.

**Nota:** È pratica comune per gli sviluppatori usare identificatori di variabili a lettere maiuscole per valori immutabili e a lettere minuscole o camelCase per valori mutabili (oggetti e array). Imparerai di più su oggetti, array, e valori mutabili e immutabili in sfide future. In sfide future vedrai esempi di identificatori di variavile in maiuscolo, minuscolo e camelCase.

# --instructions--

Modifica il codice in modo che tutte le variabili siano dichiarate utilizzando `let` o `const`. Usa `let` quando vuoi che la variabile possa cambiare e `const` quando vuoi che la variabile rimanga costante. Inoltre, rinomina le variabili dichiarate con `const` per conformarti alle pratiche comuni, il che significa che le costanti dovrebbero essere tutte in maiuscolo.

# --hints--

`var` non dovrebbe esistere nel tuo codice.

```js
(getUserInput) => assert(!getUserInput('index').match(/var/g));
```

Dovresti cambiare `fCC` a solo maiuscole.

```js
(getUserInput) => {
  assert(getUserInput('index').match(/(FCC)/));
  assert(!getUserInput('index').match(/fCC/));
}
```

`FCC` dovrebbe essere una variabile costante dichiarata con `const`.

```js
assert.equal(FCC, 'freeCodeCamp');
assert.match(code, /const\s+FCC/);
```

`fact` dovrebbe essere dichiarata con `let`.

```js
(getUserInput) => assert(getUserInput('index').match(/(let fact)/g));
```

`console.log` dovrebbe essere cambiato in modo da stampare le variabili `FCC` e `fact`.

```js
(getUserInput) =>
  assert(getUserInput('index').match(/console\.log\(\s*FCC\s*\,\s*fact\s*\)\s*;?/g));
```

# --seed--

## --seed-contents--

```js
// Only change code below this line
var fCC = "freeCodeCamp";
var fact = "is cool!";
// Only change code above this line

fact = "is awesome!";
console.log(fCC, fact);
```

# --solutions--

```js
const FCC = "freeCodeCamp";
let fact = "is cool!";

fact = "is awesome!";
console.log(FCC, fact);
```
