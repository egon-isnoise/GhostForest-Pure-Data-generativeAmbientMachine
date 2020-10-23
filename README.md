# GhostForest-Pure-Data-generativeAmbientMachine


Some time ago I found on YT a tutorial on how to make Brian Eno-like tape recording styled generative ambient music. 
I got intrigued so I expanded on the concept in order to create this patch.

Thanks to https://github.com/MikeMorenoDSP for the harp~.pd object without which this patch would be way less interesting :)


**===== HOW TO USE IT =====**

Download and unzip the files,
open the main folder and either:

a) open the GhostForest patch or 
b) make a new patch (inside the folder) and create the [GhostForest] object

I created the patch in Purr Data (L2Ork) but I avoided using external libraries as much as possible so it 
should
run on PD Vanilla without issues.



***DO NOT REMOVE harp~.pd FROM THE FOLDER OR HALF OF THE PATCH WILL BE SILENT***


**===== THE CONTROLS =====**

From top to bottom the controls are:



START ME: 
pretty self explanatory :) Turning it off turn down the main volume to zero (the patch never really stops once it has started).

RANDOMIZE ALL ON/OFF: 
This is ON by default. It keeps randomizing the repeat speeds of both the Synth sounds and the Harp sounds, 
as well as the octaves that they play on, the reverb parameters and the time at which every re-randomization happens.
(this gets more clear if you look at the yellow-ish section of the patch)


CHANGE CHORDS: 
There are three options for this. In every option there are 2 different chord voicings that switch every minute. 
C major and A minor are selected at the start. If you turn OFF randomize all the patch will stop switching chords and play only the one on which it currently is.

SYNTH DECAY:
Defines how long every synth note will be.

SINE WAVE VOL:
The synth sounds are comprised of two wave forms, this control sets the volume for the sine wave, or [osc~] object. 

SQUARE WAVE VOL:
The synth sounds are comprised of two wave forms, this control sets the volume for the square wave, or [phasor~] object. 

REPEATS TIME:
These 2 controls deciede how often notes from a specific sounds are played, respectively the synth sound and the harp sound.
As long as the RANDOMIZE ALL is on these controls decide only the range of the spedd randomization.
(Again refer to the yellow-ish part of the patch)

REVERB VOLUME:
no need to talk about this :)

REVERB PARAM 1:
This control starts a cascade of equations inside the [pd myVerb] object. Is not precise. Change the value at will.

REVERB PARAM 2:
Same as Param1.

