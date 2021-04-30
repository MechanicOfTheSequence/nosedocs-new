# game ideas

these are some game ideas I have ween contemplating

### dobble game clone

@[youtube](https://www.youtube.com/watch?v=oyqD1Sg5M4Q)

take the maths for dobble:

```js
// knicked from: https://mickydore.medium.com/the-dobble-algorithm-b9c9018afc52

let i, j, k
let n = 3                 //order of plane, must be a prime number
let numOfSymbols = n + 1  //order of plane + 1
let cards = [] //the deck of cards
let card = [] //the current card we are building

// to start, we build the first card
for (i = 1; i<= n+1; i++) {
  card.push(i)
}
cards.push(card)

// then we build the next n number of cards
for (j=1; j<=n; j++) {
  card = []
  card.push(1)

  for (k=1; k<=n; k++) {
    card.push(n * j + (k+1))
  }

  cards.push(card)
}

// finally we build the next n² number of cards
for (i= 1; i<=n; i++) {
  for (j=1; j<=n; j++) {
    card = []
    card.push(i+1)

    for (k=1; k<= n; k++) {
      card.push(n + 2 + n * (k-1) + (((i-1) * (k-1) + j-1) % n))
    }

    cards.push(card)
  }
}
```

add some vector symbols (or let people upload their own) and then add a matching game to it. needs more thought going into what to do with the monomatching. I don't have any immediate ideas on it, but a simple matching game can be made, then expanded on.

ok, icons can be found here: http://christianp.github.io/droste-dobble/
