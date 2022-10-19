![one](https://user-images.githubusercontent.com/79809962/196716164-0b634adf-3761-4e63-8ff7-2f3ce6440c72.jpg)
***
# Kompari
### A comparator module for Eurorack
  
***
### Features:
- 2 ±12V inputs, each with attenuverter
- Unipolar/Bipolar output switch
- 1 ±10V output, with attenuverter
  

Plug any CV or audio source into one of the two inputs, and it will be compared against the other.  

The output will be high (+10V) if input A is greater than input B.  

The output will be low (-10V if set to bipolar, 0V if set to unipolar) if input B is greater than input A.  

Both inputs have an attenuverter, and are both normalled to +12V, so with only one input, the value of input B can be controlled simply using the attenuverter as a ±10V voltage source.  
***
![four](https://user-images.githubusercontent.com/79809962/196716859-4d0df47c-d791-474e-b0f0-062920693c78.jpg)
***
### Easy to DIY
The module has fairly few components, and is entirely through hole. It is also 'free hardware' so you can access all the design files in this repo, and check out the [Interactive Bill of Materials here!](https://htmlpreview.github.io/?https://raw.githubusercontent.com/Allen-Synthesis/Kompari/main/kicad/bom/ibom.html)

***
### Patch Examples

#### PWM
While the concept may seem simple, the versatility of a comparator in Eurorack is far reaching.  
For example, feeding a triangle wave input to input A will result in a square wave output of the same wave, and input B (or simply the attenuverter normalled to +12) will act as PWM to that square wave. Plug the original triangle and this new PWM square wave into a crossfader/mixer and you now have a pretty modulatable waveshaper.  
  
#### Compressor
Another more complex case would be to run an audio source through an envelope follower, then into input A. Use input B to set a maximum voltage (volume), and when the volume of the audio (envelope follower voltage) goes above this voltage, the Kompari output should trigger an envelope generator which has a negative effect on the volume of a VCA on the original audio. You now have a slightly roundabout, but fully fledged compressor! The envelope generator's attack and decay controls are the response of the compressor, the VCA's unaltered input voltage (before subtracting the envelope) is the makeup gain, and the Kompari's input B is the threshold.  
  
As you can see, it's easy to get carried away with using a comparator module such as the Kompari, and the patches you can make are only limited by your imagination!
