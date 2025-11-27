---
layout: project-desc
permalink: /projects/encoder/
---


# MA732 Magnetic Encoder Breakout Board

<div class="clearfix" style="clear: both; display: table; margin: 2vw 2vw;">
  <div style="float: left; width: 55.7%; padding: 5px;">
    <img class="title-img" src="/pictures/ma732/ma732-black.png" alt="Base quadtrax model in tan"> 
  </div>
  <div style="float: right; width: 40%; padding: 5px;">
    <img class="title-img" src="/pictures/ma732/pcb-layout.png" alt="Base quadtrax model in red">
  </div>
</div>


<div class="pdf">
  <iframe src="/pictures/ma732/ma732-schematic.pdf" width="70%" height="900px"></iframe>
</div>
<div style="text-align: justify;">
This is the first PCB I've ever built so I decided to use it as a learning experience to familiarize myself with PCB design. I designed it in EasyEDA based on an encoder made by mjbots and ordered the assembled PCB through JLCPCB.

The MA732 is a great compact encoder option. I'm a fan of contactless encoders like this one for the versatility of them. This one in particular can operate mounted in two orientations: end-of-shaft (left) and side-shaft (right) which is great for an application like the lidar I'm building with a hollow shaft gimbal motor that makes great use of the side-shaft configuration alongside a ring-shaped diametric magnet. 

<div class="clearfix" style="clear: both; display: table; margin: 2vw 2vw;">
  <div style="float: left; width: 49%; padding: 5px;">
    <img class="title-img" src="/pictures/ma732/end-of-shaft.png" alt="Base quadtrax model in tan"> 
  </div>
  <div style="float: right; width: 45%; padding: 5px;">
    <img class="title-img" src="/pictures/ma732/side-shaft.png" alt="Base quadtrax model in red">
  </div>
</div>

Using the side-shaft configuration does come with some unique challenges that can luckily be addressed by configuring the microcontroller. The method best supported by the MA732 is known as "bias current trimming."

## Bias Current Trimming (BCT)

Within the MA732, Hall effect sensors are oriented to detect the in-plane components of the magnetic field in the plane parallel to the package's top surface. In the case of side-shaft mounting, the magnetic field angle is no longer directly proportional to the shaft angle as with end-of-shaft mounting. By modifying the BCT settings in the register map, specifically register 2, the MA732 can be calibrated to compensate for this non-linearity and recover the linear relationship between the mechanical angle and the sensor output.

<div style="display: flex; justify-content: center;  padding: 5px; margin: 2vw 2vw;">
    <img class="title-img" src="/pictures/ma732/error-bct-0.png" alt="side-shaft error curve plot with no BCT enabled" width=60%>
</div>


</div>