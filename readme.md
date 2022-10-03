Trying to make sense of [Stable Diffusion][1] through variation in the parameter space.
------

The [Stable Diffusion][1] model has a complex interface, and this is largely a result of the model itself. An understanding of what happens to produce the images would be my first recommendation for getting a grasp on how the different parameters effect output. Unfortunately, that understanding doesn't make everything so clear. So, a good bit of experimentation is needed.

This repository aims to excellerate the experimentation with some examples. 

[Some][2] implementations of [Stable Diffusion][1] have an [X/Y Plot feature][3] which creates a grid of varying parameters. From this we can better understand the resulting output.

Example images have metadata outlining parameters used. Yet, different implementations of [Stable Diffusion][1] can use the parameters differently. In some cases I cannot generate the same images any more. :/


Seamless Texture Studies:
------

* 0466059324-parallax
* 1608700726-leaves
* 1727232361-frogs
* 3086193878-autumn
* 3136066660-monkey
* 4125763558-halloween

Okay, there is the first group of studies - which consist of seamless textures. These differ from the "Tiling" feature of [webui branch][2] in that I'm asking the model to generate a seamless texture instead of it being enforced by the underlying model use.

This might seem weird, but we know the model was trained on A LOT of seamless textures and I want to dial in that feature through prompting and parameters. It was actually easier than I thought it would be - the model definitely understands seamless textures.

If you look at the X/Y studies and examine what parameters actually produce seamless textures. We should ask ourself some questions? What range of CFG Scale produce seamless textures? Is this consistent across the set of tests? How does the step count impact feature presents? Like a good scientist we try to draw some conclusion (to be tested).


Additional Resources:
------

* [Druid princess - step 1 to 101 animation][4]
* [Stable Diffusion: Tutorials, Resources, and Tools][5]
* [Awesome Diffusion][6]

![GitHub repo size][7]


[1]: https://github.com/CompVis/stable-diffusion
[2]: https://github.com/AUTOMATIC1111/stable-diffusion-webui
[3]: https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Features#xy-plot
[4]: https://www.reddit.com/r/StableDiffusion/comments/xay9ts/druid_princess_step_1_to_101_animation/
[5]: https://stackdiary.com/stable-diffusion-resources/
[6]: https://github.com/cobanov/awesome-diffusion
[7]: https://img.shields.io/github/repo-size/bitRAKE/sd-xy-studies?style=for-the-badge
