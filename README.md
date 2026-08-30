# Smart Utility Toolkit

A hands-on Node.js lab project built entirely with **core modules** — no external
packages or frameworks (`process`, `http`, `fs`, `crypto`).

## Files

| File | Purpose |
|---|---|
| `calculator.js` | CLI calculator using `process.argv` (add, sub, mul, div) |
| `modules/isEven.js` | Custom module — checks if a number is even |
| `modules/logger.js` | Custom module — timestamped console logging |
| `app.js` | Demonstrates reusing `isEven` and `logger` modules |
| `server.js` | Basic HTTP server with `/`, `/about`, `/contact` routes |
| `fileManager.js` | CRUD file operations using the `fs` module |
| `dice.js` | Secure random dice roller using the `crypto` module |
| `test.txt` | Sample file used/created by `fileManager.js` |

## How to Run

```bash
# 1. Calculator
node calculator.js add 10 5
node calculator.js sub 10 5
node calculator.js mul 10 5
node calculator.js div 10 0

# 2. Custom module demo
node app.js

# 3. HTTP server (then visit http://localhost:3000/, /about, /contact)
node server.js

# 4. File manager (Create -> Read -> Update -> Delete)
node fileManager.js

# 5. Dice roller (roll 5 times)
node dice.js 5
```

## Notes

- All async file operations use callback-style `fs` methods to make the
  asynchronous, non-blocking nature of Node.js visible in the console logs.
- `crypto.randomInt()` is used instead of `Math.random()` for
  cryptographically secure randomness in the dice generator.
- The logger module timestamps every log line, which is useful for observing
  execution order (see: Execution Flow & Console Analysis requirement).
