## General
____________

### Author
* Josh McIntyre

### Website
* jmcintyre.net

### Overview
* MicroProver helps users visualize proof-of-work algorithms on the Adafruit Circuit Playground Express

## Development
________________

### Git Workflow
* master for releases (merge development)
* development for bugfixes and new features

### Building
* make build
Build the application
* make clean
Clean the build directory

### Features
* A programmable visualization tool for mock proof-of-work - set difficulty from 1-7
* Visualize work being done by displaying each 8 bit hash as LEDs on the board 

### Requirements
* Requires Python 3 and CircuitPython

### Platforms
* Adafruit Circuit Playground Express

## Usage
____________

### General usage
* Copy "code.py" and "boot.py" to the root directory
* Switch the on/off switch (D7) to the right (facing VOUT, A0, A7) and reset. This will ensure the log can be written to the onboard storage
* Set the difficulty rating from 1-7 by pressing the B button. The difficulty will be displayed by the LEDs
* Press A to start hashing - each 8-bit hash value will be shown with the board LEDs. RED == 0, GREEN == 1
* The final solution (hash value) will be displayed by the LEDs
* Press A to restart hashing, or B to return to the difficulty programming menu

### Accessibility
* Shake the Circuit Playground board while in the difficulty menu to turn on accessible "sound mode"
* This mode will read the difficulty target in the programming menu, play a tone when a solution is found,
and read the solution block hash in binary format

### Data visualization
* Copy the logfile (pow_log.csv) from the Circuit Playground Express filesystem to the user machine
* Run `python graph_pow.py` in the log directory
