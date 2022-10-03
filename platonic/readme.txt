Prompt:	platonic solids made of various materials
Steps:	8,16,32,64,128,256,512
DFG Scale:	3,5,7,11,13,17,19,23,29,31


It's beneficial to explore the step/CFG space to understand how/if samplers converge. This prompt highlights many perspective of the different samplers.


Some things to note:
* Samplers perform at different speeds (per step) on same hardware.
* DPM adaptive sampler doesn't use the step count. Only CFG Scale impacts image variation.
* With DDIM/PLMS samplers the step count is quantized - not all step counts are possible.
* With DDIM/PLMS samplers the step count is limited to 250 max.


We can ask a number of questions about the results:
* Does the model know what the platonic solids are?
* How predictable is a sampler across steps/CFG?
* What are the limits of each CFG Scale (under-/over- fitting step range)?
* What step range produces the best images (sharp edges, shadows, reflections, subject matter)?


Relative Performance of Samplers:
				3090ti
	DPM adaptive	02:21
	DDIM			04:41
	PLMS			05:23
	Euler a		06:54
	LMS			07:10
	Euler			07:13
	DPM fast		07:20
	DPM2 a		12:16
	DPM2			13:17
	Heun			13:17


Possible Future Work:
* Mean square error graphs to show convergence.
* Difference maps to show convergence visually.
* Further extend some samplers to higher CFG/Step counts.
* Better performance metric?
