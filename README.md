# ArduinoFrekvens

Simple Arduino library for controlling the IKEA FREKVENS LED panel.

## Usage

This library was made and tested for the RP2040 board. It might work on other boards as well, but I cannot guarantee this. For possible pinout settings see `Frekvens.hpp`.

```C++
#include <Arduino.h>

#include "Frekvens.h"

// Create the library.
Frekvens frekvens;

void setup () {
	// Settings, e.g. pinouts, need to be made before call to Init.
	// See Frekvens.hpp for possible settings.
	frekvens.Init();
  
	// Set a pixel using the built-in gamma curve.
	frekvens.SetPixelGamma(15, 12, 0.1);
}

void loop() {
	// Run the internal update loop.
	frekvens.Update();
}
```
