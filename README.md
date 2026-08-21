# Solidity patterns and finite state machines

This repository demonstrates small Solidity patterns and a product validation
finite state machine using Truffle.

## What is included

- `AccessRestriction.sol` demonstrates ownership checks and delayed renunciation
- `EmergencyStop.sol` demonstrates pausing and emergency withdrawals
- `MemoryArrayBuilding.sol` demonstrates structs and dynamic arrays
- `StateMachine.sol` demonstrates bounded forward and backward transitions
- `StringEquality.sol` demonstrates hash based string comparison
- `TightVariablePacking.sol` demonstrates packed storage values
- `Validator.sol` records and validates product keys
- `FiniteStateMachine.sol` wraps a complete validation round

The `contracts`, `migrations`, and `test` directories contain the implementation,
deployment scripts, and JavaScript tests respectively.

## Requirements

- Node.js 16 or newer
- npm 8 or newer
- Truffle 5.6 or newer
- Ganache running on `127.0.0.1:7545` for the configured development network

Install dependencies with:

```sh
npm ci
```

## Development

Compile the contracts:

```sh
npx truffle compile
```

Deploy to the development network:

```sh
npx truffle migrate --reset
```

Run the full test suite:

```sh
npm test
```

Run one test file:

```sh
npx truffle test test/8_finite_state_machine_test.js
```

Truffle starts a temporary Ganache instance when no configured network is
selected. The development network in `truffle-config.js` expects an external
Ganache instance on port 7545.

## License

This project is available under the MIT License.
