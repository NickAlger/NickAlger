---
title: Astroknot puzzle
layout: page
permalink: astroknot
---

<script>
MathJax = {
  tex: { inlineMath: [['$', '$'], ['\\(', '\\)']], displayMath: [['$$', '$$'], ['\\[', '\\]']] }
};
</script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

The [Astroknot puzzle](http://puzzlesolver.com/puzzle.php?id=45) is one of the most difficult wire-and-string tanglement puzzles I’ve found. This page explains how to solve it, and in the process some general ideas about solving tanglement/topology-ladder puzzles. Here’s a picture of the puzzle; the goal is to remove the string.

![Astroknot whole puzzle](./astroknot/astroknot_all_pic.jpg)

Before going into specifics, there's an important general strategy for circumventing "stuff" that prevents you from passing over a wire loop. The steps are, 
 1. pass the string through the loop, 
 2. circumvent the stuff in the way, and then 
 3. pass the string back through the loop. 
This is shown in the following image:

![circumvent stuff](./astroknot/astroknot_circumvent_stuff_all-303x1024.png)

Now let's go back to the Astroknot. One of the first things we notice is that it's complicated and hard to understand as a whole. In order to attack the problem, let's simplify it a little by doing an imaginary deformation of the outer wire loops so that we can better understand the structure. These loops are made out of metal so we can't bend them in real life, but that doesn't prevent us from bending them in our head.

![imagining deformed puzzle](./astroknot/astroknot_deformed_wire_shape.png)

Now we can devise a strategy based on this deformed shape, and then when we implement it on the real shape, we will just do an extra circumvention sequence (compound move) whenever we want to move a loop of string over the outer wire loops. This is shown in the following image:

![compound move](./astroknot/astroknot_compound_move_full_sequence.png)

Now let's develop our strategy on the deformed version. There's really just one wire that we trace around from the start to the finish, avoiding other obstructions along the way.

![overall sequence](./astroknot/astroknot_overall_sequence.png)

In the actual puzzle, this looks like the following.

![sequence 1](./astroknot/astroknot_strategy_pic1.png)

To go from step 1 to step 2, we just go out and around the left wire loop (which implicitly involves going around the whole thing during the compound move):

![sequence 1 to 2](./astroknot/astroknot_1_to_2.png)

Let's look at that sequence in a little more detail.

![circumvent 0](./astroknot/circumvent_pic_0.png)

![circumvent 1](./astroknot/circumvent_pic_1.png)

![circumvent 2](./astroknot/circumvent_pic_2.png)

![circumvent 3](./astroknot/circumvent_pic_3.png)

![circumvent 4](./astroknot/circumvent_pic_4.png)

![circumvent 5](./astroknot/circumvent_pic_5.png)

![circumvent 6](./astroknot/circumvent_pic_6.png)

![circumvent 71](./astroknot/circumvent_pic_71.png)

Then to go from step 2 to step 3, we do essentially the same thing, but just through the other inner wire loop.

![2 to 4](./astroknot/astroknot_2_to_41-496x1024.png)

In detail, we have the following,

![2 to 4 part 1](./astroknot/astroknot_2_to_4_1.png)

![2 to 4 part 2](./astroknot/astroknot_2_to_4_2.png)

![2 to 4 part 3](./astroknot/astroknot_2_to_4_3.png)

![2 to 4 part 4](./astroknot/astroknot_2_to_4_4.png)

![2 to 4 part 5](./astroknot/astroknot_2_to_4_5.png)

![2 to 4 part 6](./astroknot/astroknot_2_to_4_6.png)

![2 to 4 part 7](./astroknot/astroknot_2_to_4_7.png)

![2 to 4 part 8](./astroknot/astroknot_2_to_4_81.png)

![2 to 4 part 9](./astroknot/astroknot_2_to_4_91.png)

Now we have escaped the inner loops for good, and only have to do one more compound move to take the string off the outer loop.

![final stretch 1](./astroknot/astroknot_final_stretch_1.png)

![final stretch 2](./astroknot/astroknot_final_stretch_2.png)

![final stretch 3](./astroknot/astroknot_final_stretch_3.png)

![final stretch 4](./astroknot/astroknot_final_stretch_4.png)

![astroknot solved](./astroknot/astroknot_solved.png)

----

# See also:

 - [Kevin Sadler's review](http://www.puzzlemad.co.uk/2012/02/last-batch-of-livewire-puzzles-9.html) of the Astroknot puzzle on [PuzzleMad](http://www.puzzlemad.co.uk/)
