Prompt:	platonic solids made of various materials
Steps:	8,16,32,64,128,256,512
DFG Scale:	3,5,7,11,13,17,19,23,29,31


For Exponential Samplers:

Steps:	2,4,6,8,16,24,32,40,48,56,64
DFG Scale:	3,5,7,11,13,17,19,23,29,31,37,41



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


(Step-wise) Relative Performance of Samplers:
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

	* Karras		<uncorreclated with above>
	DPM2 a		07:11
	DPM2			08:31

	* Karras		<uncorreclated with above>
	DPM2 a		2:25:57	156 images
	DPM2			2:15:10	156 images
	LMS			?

5,8,16,24,32,40,48,56,64,128,256,512,1024
3,5,7,11,13,17,19,23,29,31,37,41



Possible Future Work:
* Mean square error graphs to show convergence.
* Difference maps to show convergence visually.
* Further extend some samplers to higher CFG/Step counts.
* Better performance metric?


https://en.wikipedia.org/wiki/Platonic_solid



What are correct images to respond with? "Various materials" implies variety and does "solids". Platonic suggests depth in an intellectual sense - nothing glamorous or flamboyant. The perfect image might be all five platonic solids of different materials each.






Is there a limit to CFG?
	- where all step counts have rounding errors



DPM2 a Karras,
	- after CFG 23.0, rounding errors at high step counts











