---
layout: project-desc
permalink: /projects/quadtrax/
---


# MG-A1 Quadtrax Tank Retrofit

<img class="title-img" src="/pictures/quadtrax/tan-quadtrax.jpeg" alt="Base quadtrax model in tan"> 
<img class="title-img" src="/pictures/quadtrax/red-quadtrax.jpg" alt="Base quadtrax model in red">

While roaming on FB Marketplace, as I often do, I came upon two of these RC tanks that caught my attention. Having never seen anything like these and at only $20 for the pair, I couldn't pass up the opportunity to pick these up. 

I couldn't find any documentation apart from this [manual][manual] ([archived][archived-manual]) but there were a few blog posts and YouTube videos of the tanks in action.

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/uu17HlXAB0g?si=dZg3zANBFZYQ9I0p" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/KIVWXEgtYbQ?si=10MGfgmw7kSt6rMO" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Some of my planned modifications for this tank include:
- Swapping the 9.6V 700mAh NiCd battery for a 3S LiPo battery
- Upgrading the RS380 motors to RS395 motors which should measurably improve the overall tank's power 
- Adding magnetic encoders to the motors for positional feedback. *See the magnetic encoders I'll be using [here][magnetic-encoder].*
- Establish odometry without relying on dead reckoning, tanks are prone to slippage which destroys the accuracy of deadreckoning. Currently considering IMU, GPS, visual odometry.
- Attach my [lidar][lidar] to the tank 


[manual]: https://fcc.report/FCC-ID/LU9276203/454831.pdf
[archived-manual]: https://web.archive.org/web/20251126050455/https://fcc.report/FCC-ID/LU9276203/454831.pdf
[magnetic-encoder]: https://www.lucaslanzendorf.com/projects/encoder
[lidar]: https://www.lucaslanzendorf.com/projects/lidar