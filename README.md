![logo](./chessjslogo.svg)

# chess.js

[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/pabrams/chess.js/node.js.yml)](https://github.com/pabrams/chess.js/actions)
[![npm](https://img.shields.io/npm/v/chess.js?color=blue)](https://www.npmjs.com/package/chess.js)
[![npm](https://img.shields.io/npm/dm/chess.js)](https://www.npmjs.com/package/chess.js)

This is a fork of @jhlywa/chess.js that adds features such as "xray attack", (boolean `xray` parameter added to `attackers` method - see [Counting attackers, bearing in mind batteries #542](https://github.com/jhlywa/chess.js/issues/542)).

chess.js is a TypeScript chess library used for chess move
generation/validation, piece placement/movement, and check/checkmate/stalemate
detection - basically everything but the AI.

chess.js has been extensively tested in node.js and most modern browsers.

## Documentation

This README provides a quick example, full documentation can be found at
[https://github.com/pabrams/chess.js](https://github.com/pabrams/chess.js).

## Installation

Run the following command to install the most recent version of chess.js from
NPM:

```sh
npm install @pabrams/chess.js
```

## Example Code

The code below plays a random game of chess:

```ts
import { Chess } from 'chess.js'

const chess = new Chess()

while (!chess.isGameOver()) {
  const moves = chess.moves()
  const move = moves[Math.floor(Math.random() * moves.length)]
  chess.move(move)
}
console.log(chess.pgn())
```

## Contributing

If you have any questions, suggestions, or find any bugs please open an issue.
PRs are very welcome too, please read the [Contributing Guide](CONTRIBUTING.md)
first to help make it a smooth process.
