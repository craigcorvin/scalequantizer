<h2>Scale Quantizer</h2>

C++ class for quantizing a frequency to a musical scale.

Author: Craig Corvin

// Class initialization

ScaleQuantizer quant;

quant.Init();

// Describe your desired scale as a boolean array and feed it into UpdateScale.

// initialize as a Major scale
// {C, C#, D, D#, E, F, F#, G, G#, A, A#, B}	

bool initScale[12] = {1,0,1,0,1,1,0,1,0,1,0,1};

// update scale

quant.UpdateScale(initScale);

// Retrieve your quantized frequency

float quantizedFrequency = quant.Process(frequency);

// You can also set EDO using SetSemitonesPerOctave, and multi-octave scales are possible.

// Example: Prometheus Chord, C F# Bb E A D, over four octaves.

quant.SetSemitonesPerOctave(12.0f);

bool startScale[48] = {
0,0,0,0,0,1,0,0,0,0,0,0,
0,0,0,0,0,1,0,0,0,0,0,1,
0,0,0,1,0,0,0,0,0,1,0,0,
0,0,1,0,0,0,0,1,0,0,0,0
};

quant.UpdateScale(startScale);


