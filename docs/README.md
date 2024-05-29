# Wokwi cd4077b Chip

This is a custom chip for [Wokwi](https://wokwi.com/). It implements the cd4077b IC.

## Description

The cd4077b contain faur independent 2-input Exclusive-NOR gates. Each gate performs the Boolean function
of j = NOT(A ⊕ B) (for gate 1 in this case) in positive logic.

## Truth Table (1 for each gate)

| INPUT A | INPUT B |  OUTPUT |
|---------|---------|---------|
|    L    |    L    |    H    |
|    H    |    L    |    L    |
|    L    |    H    |    L    |
|    H    |    H    |    H    |


## Pin names

| Name | Description          |
| ---- | -------------------- |
|  A   | Input signal  A      |
|  B   | Input signal  B      |
|  J   | Gate 1 Output signal |
|  C   | Input signal  C      |
|  D   | Input signal  D      |
|  K   | Gate 2 Output signal |
|  E   | Input signal  E      |
|  F   | Input signal  F      |
|  L   | Gate 3 Output signal |
|  G   | Input signal  G      |
|  H   | Input signal  H      |
|  M   | Gate 4 Output signal |
| GND  | Ground               |
| VCC  | Supply voltage       |


## Usage

To use this chip in your project, include it as a dependency in your `diagram.json` file:

```json
  "dependencies": {
    "chip-cd4077b": "github:wokwi-custom-chips/cd4077b@0.1.0"
  }
```

Then, add the chip to your circuit by adding a `chip-cd4077b` item to the `parts` section of diagram.json:

```json
  "parts": {
    ...,
    { "type": "chip-cd4077b", "id": "chip1" }
  },
```

For a complete example, see [The cd4077b chip test project](https://wokwi.com/projects/398983628077680641).
