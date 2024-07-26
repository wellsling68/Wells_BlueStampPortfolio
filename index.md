# CNC Pen Plotter
<!---Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
-->



| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Wells L | Saratoga High School | Electrical Engineering | Rising Junior

<img src="Wells L (1).png" width="500" height="420">

# Modifications
For my modification, I wanted to make my pen plotter able to draw in color. To start, I wanted to see if this had been done before by searching for this modification online. To my suprise, I found a very well documented <a href="https://www.instructables.com/Tims-10-Colour-Plotter-Pen/">article</a> on Instructables detailing the steps to make the pen plotter draw in color. The article provided 3d printable models that I could download and implement onto my machine, saving me the time I would have needed to design my own model. 

I faced many challenges while working on this modification, including some I had not anticipated. One of the challenges was with my 3D printed parts. Because I did not have experience with CAD before, the tool holder, which I had modified to mount onto my existing plotter, had to be reprinted 5 times since I made many errors while cadding. This led to a lot of time being wasted, since each part took anywhere from 30 minutes to 1.5 hours. After assembling all of the 3D printed parts, I found myself with an unexpected issue: the color changing module was too heavy. To fix this, I came up with 3 solutions. The first was to reprint the parts with less infill to hopefully make it lighter (10% --> 5%). The second was to add a baseplate which would not only hold the paper while plotting but also support the pen as it moved. The last was to add counterweights to the pen's guide rail, which would prevent the plotter from tipping over.  

Unfortunately, I was not able to fully complete the color switching mechanism at Bluestamp. This is due to my board not having GPIO (General Purpose Input/Output) pins which my geared DC motor could use. The best solution I came up before Bluestamp ended was to manually power the DC motor with a 9V battery whenever I wanted to change colors.  

<!--# Demo Night Presentation
<iframe width="560" height="315" src="https://www.youtube.com/embed/SiCJL7baP7g?si=7E9pX54SVRi4F1Ub" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
-->

# Final Milestone

<!--
**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**
-->

<iframe width="560" height="315" src="https://www.youtube.com/embed/AqdlKlqbwig?si=8Nbrbh2Gn9EWJudT" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<!--
For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE
-->
## Summary:
For my final milestone, I made my CNC pen plotter capable of drawing custom images. Since my second milestone, I downloaded new software, Inkscape and UGS (Universal G-code Sender), which allowed me to complete this milestone. These programs were key for allowing me to generate and execute G-code files efficiently and consistently. Here is the process for this multi-step task:

&emsp<ol>
  <li>Find an image, preferably in SVG format</li>
  <li>Upload the image to Inkscape</li>
  <li>Turn the image into paths, then convert the paths into G-code</li>
  <li>Save the G-code to a directory</li>
  <li>Connect the USB cable and the power supply to the Arduino Uno</li>
  <li>Upload the G-code file to UGS</li>
  <li>Run the program</li>
</ol>

## Challenges:
While completing my final milestone, I ran into significant issues with the servo that slides the pen vertically. The issue came when generating G-code. The application I used to generate G-code, Inkscape, used a seperate command to control the Z-axis, which could not be read by the servo which controlled the Z-axis on my machine. To fix this, I found the specific G-code that would activate the servo and, as part of G-code generation, manually replaced all the dysfunctional commands with the functional commands (M3S1000 and M5). 

## What's Next:
After finishing my project, I plan on working on modifications which will make the plotter capable of drawing in color.

# Second Milestone
<!--
**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**
-->
<iframe width="560" height="315" src="https://www.youtube.com/embed/bXM9CBqnt5A?si=2iOWLGW5lnr_fxpR" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<!--
For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 
-->
## Summary:
For my second milestone, I installed and set up the software that was provided with the kit, GRBL Candle 0.9. After that, I uploaded the firmware the kit provided onto the microcontroller on my pen plotter, an Arduino UNO. To start the pen plotter, I would connect my computer to the Arduino UNO with a USB cable, then GRBL Candle 0.9 allowed me to send Gcode (geometric code) instructions from my computer to the Arduino UNO on the pen plotter. I considered this milestone to be complete when I was able to fully print quality samples of the templates provided to me, which were a wiresphere and a clock.

## Challenges:
So far, I was most suprised by the accuracy in which the pen potter could draw since I did not think that motors could spin so precisely. Besides that, I found that finding the correct position for the plotter to begin drawing the most challenging since the software I was using, GRBL Candle 0.9, did not have a visualizer showing which direction the pen plotter would move or the ability to zero the machine coordinates. Because of this, many issues arose in the beginning, such as drawing off the paper or the machine jamming into its sides. Eventually, after many attempts, I was able to figure out the starting positions for each the template images, allowing me to finally complete this milestone.

## What's Next:
For my next milestone, I would like to be able to draw my own custom images on my plotter. I would also like to find new software that would give me more controll over my machine.

# First Milestone

<!--
**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**
-->

<iframe width="560" height="315" src="https://www.youtube.com/embed/idlkSNiSGeU?si=dgGiI-cUJyXilO2X" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<!---
For your first milestone, describe what your project is and how you plan to build it. You can include:
- An explanation about the different components of your project and how they will all integrate together
- Technical progress you've made so far
- Challenges you're facing and solving in your future milestones
- What your plan is to complete your project
-->
## Summary:
For my first milestone, I fully assembled and wired the main hardware of the pen plotter. The pen plotter kit came with assembly instructions, which I downloaded off the <a href="https://www.doesbot.com/corexy-pen-plotter/45-doesbot-a4-working-area-xy-plotter-printer-handwriting-writer-drawing-robot-kit-corexy-structure-assemble-needed-diy-cnc.html">Doesbot website</a>, so this step was relatively simple. The assembled pen plotter included acrylic frames, stepper motors, two guide rails per axis, a belt, a servo for lifting the pen, and wires connecting the electronics to the Arduino (grbl microcontroller). 

Functionally, the pen plotter works by processing instructions from my computer in the Arduino, which then tells the two stepper motors to spin. To move the pen, a belt is attatched to the motors to ensure the pen would move to the correct area.

## Challenges:
The biggest challenge I had to overcome for this milestone would be assembling the acrylic parts correctly. This is because when assembling, I didn't pay attention to the orientation of the pieces I was building, so when I realized the mistakes I had made, I had to disassemble and reassemble the plotter many times. Although fixing these issues took a few extra hours to complete, I learned to be more diligent while working on this project.

## What's Next:
After this, I plan on installing the software that came with the pen plotter and working on plotting the template images also provided within the kit.

# Starter Project

<iframe width="560" height="315" src="https://www.youtube.com/embed/q2l6TSXJP5E?si=09z19mXJhHxSLTIz" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


## Summary:
For my starter project, I chose the calculator. This project was pretty simple, as it mainly involved me soldering the buttons, main chip, battery holder, and display onto the given PCB. After I finished soldering, I inserted the battery and tested the calculator by performing some basic operations. The final step before finishing the project was to assemble the provided case.

## Challenges: 
This was my first time soldering, so my soldering skills were not the best. This resulted in inconsistant solders where it was not fully filled.

## What's Next: 
I am going to start my final project, the CNC Pen Plotter.

<!---
# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 
-->
# Bill of Materials

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Soldering Practice Kit | To practice soldering | $16.99 | <a href="[https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/Kit-Calculator-Resistance-Electronic-HUAGZIMO/dp/B0D13C9SYT/ref=sr_1_3?crid=3HGJTLNZ9O2GX&dib=eyJ2IjoiMSJ9._SWtzcdxglPoBR9j02Ru8HdkQYctYGhXoQSzf1MVwW8-wdJNSkQkLmCAtn4dRp6g-6R7J9461vhIP2EF_nk7Tig6XDG9bCrlMTSlmck5MBQwLRhhnSiQUGo0QJa1GwgSj6a6-1yBKFqneN2-Z0AqO-StnMGL2G8655x5qfsjKhjBt48dYiTRy3_0E2_Jk5agtyEMTLExRFtYVrPI5ML2CKLPh8c4dT4clp-o5in2kS0.ajrpXguZyLba8zZbq_b1WT_1ccEQlOe_PpesP9bkSUM&dib_tag=se&keywords=calculator+solder&qid=1717994208&sprefix=calculator+solde%2Caps%2C148&sr=8-3)"> Link </a> |
| AX4 XY Pen Plotter | My main project | $129.99 | <a href="https://www.doesbot.com/corexy-pen-plotter/45-doesbot-a4-working-area-xy-plotter-printer-handwriting-writer-drawing-robot-kit-corexy-structure-assemble-needed-diy-cnc.html"> Link </a> |
| DC Gear Motor | Part of my modification | $13.99 | <a href="https://www.amazon.com/200RPM-Torque-Reduction-Gearwheel-Gearbox/dp/B09YV4PK55/ref=asc_df_B09YV4PK55/?tag=hyprod-20&linkCode=df0&hvadid=692875362841&hvpos=&hvnetw=g&hvrand=191741027004351481&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9032183&hvtargid=pla-2281435177578&mcid=af7d165fd28b3f3eb082fd4452d055c5&hvocijid=191741027004351481-B09YV4PK55-&hvexpln=73&gad_source=1&th=1"> Link </a> |
| 10 Color Pen | Modification for plotting in color | $10.99 | <a href="https://www.amazon.com/HeTaoCat-Multicolor-0-5mm-Retractable-Ballpoint/dp/B08BYN3LZW?th=1"> Link </a> |
| GRBL 1.1 Microcontroller | What the item is used for | $29.99 | <a href="https://www.amazon.com/Doesbot-Control-Support-Spindle-Engraving/dp/B0C625ZCN7)"> Link </a> |
| 3d Printed Parts | Parts integral for my modification | N/A | <a href=""> N/A </a> |

<!---
| Item Name | What the item is used for | $Price | <a href=""> Link </a> |
| Item Name | What the item is used for | $Price | <a href=""> Link </a> |
-->

<!---
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.

# Other Resources/Examples

- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
-->
