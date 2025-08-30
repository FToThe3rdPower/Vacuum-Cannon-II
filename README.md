# Vacuum Cannon: Rebuilt
**Trey Grijalva** 

![Figure 0: Vacuum Cannon I slow motion (8.9k fps)](figures/sloMoShot.mp4)

---

## Abstract
The vacuum cannon is a deceptively simple device that accelerates a projectile by evacuating air from a sealed tube, yet its dynamics involve rich fluid mechanics and shock physics. Early models, such as those by Ayars and Buchholtz (2004), treated the system with constant and simple variable acceleration approximations, predicting projectile speeds limited by the speed of sound. Subsequent experimental studies, including Schlieren imaging, revealed that shock and rarefaction waves play a crucial role in the projectile’s motion, requiring a more complete theoretical treatment such as Landau and Lifshitz’s one-dimensional gas flow treatment. Renewed efforts at Chico State sought to refine these experiments, but were interrupted by the COVID-19 pandemic. Independently, piston-driven designs popularized in the public sphere offered a practical and scalable alternative to traditional vacuum pump setups. In this work, we constructed such a cannon from recycled materials, recorded preliminary data with high-speed imaging, and identified limitations in both instrumentation and barrel durability. These results motivate future studies combining improved diagnostics with shock-physics-informed models to fully capture the behavior of vacuum cannons.

---

## 1. Introduction
In 2004, two professors at California State University, Chico published the paper *Analysis of the Vacuum Cannon* [1], which explores two simple models and concludes that the ball does not exceed the speed of sound, agreeing with their hypothesis.

---

## 2. Models from Ayars & Buchholtz (2004)

Their *zeroth-order approximation* naively assumes constant acceleration:

$$
a_0 = \frac{F}{m} = \frac{P_0 A}{m}
$$

where $a_0$ is the constant rate of acceleration, $P_0$ is atmospheric pressure and $A$ is the projectile’s cross-sectional area.  

Equation (1) predicts a maximum speed,

$$
v(L) = \sqrt{\frac{2 P_0 A L}{m}}
$$

which is notably dependent on the length of the barrel, $L$:

> “This estimate runs into problems for longer barrels, for which it predicts a speed greater than the speed of sound. The ensuing ‘common-sense correction’ is that the projectile asymptotically approaches the speed of sound.” [1]

The *first-order approximation* that accounts for variable acceleration, obtained from Newton’s second law, predicts:

$$
v_{\text{max}} = \sqrt{a_0 \lambda} = \sqrt{\frac{P_0}{\rho}}
$$

This equation may look familiar, as it is the same form as the speed of sound:

$$
v_s = \sqrt{\frac{\gamma P_0}{\rho}}, \quad \text{where } \gamma = C_p / C_v
$$

---

## 3. Comparison with Early Experiments
Comparing these two models with experimental data obtained via PASCO photogates immediately outside the barrel yields the figure below.

![Figure 1: Comparison of experimental measurements with various models for vacuum cannon velocity.](figures/subsonicModel.ong)

However, the next year, a group from Bethel University in St. Paul, Minnesota, used a much more sophisticated Schlieren imaging setup to image the ball and airflow [2]. They found that both of Ayars’ & Buchholtz’s models were underestimating the maximum velocity, as they did not account for the shock physics.

![Figure 2: Schlieren imaging setup used to study the vacuum cannon flow and projectile.](figures/fig_sclieren_setup.png)

---

## 4. Shock Physics Context (Landau & Lifshitz)
Having seen this new development, Ayars resolved to improve their experimental methods, but desired to make it a project with multiple students. In the meantime, Buchholtz did more literature research to investigate the theory. He found that Landau & Lifshitz were writing their *Course of Theoretical Physics* in 1944 and published the first edition of Volume 6, *Fluid Mechanics*.  

In English, the book includes Chapter IX, “Shock Waves” and Chapter X, “One-Dimensional Gas Flow.” Contained within these chapters is a mathematical description of shock and rarefaction waves in a pipe [3,4].

---

## 5. Project Continuation at Chico (2019) and Interruptions
In 2019, a team of researchers was assembled at Chico State with the mission of continuing the work related to the vacuum cannon. Theoretical and experimental progress were made, and simulations were devised. Unfortunately, COVID-19’s emergence compelled the University to shut down, stalling the project.

---

## 6. Piston-Driven Designs and Our Build
Unbeknownst to the other characters in this story, a YouTuber by the username of [NightHawkInLight](https://www.youtube.com/watch?v=0DKWSXstXuc) had developed and prototyped several iterations of vacuum cannon in 2017. It is a more elegant, cost-effective, and scalable design that uses a piston to replace the rear seal, as well as the vacuum pump itself.  

We became aware of this design shortly before taking the Utrecht Experiment Design course in 2023, and opted to build our own piston-driven version.

![Figure 3: Piston-driven vacuum cannon (thumbnail placeholder from YouTube content by NightHawkInLight).](figures/nighthawkinlightthumbnail.png)

Our version did not have a reusable front seal due to parts availability; it uses aluminum foil. It is also slightly different from NightHawkInLight’s designs in being composed of upcycled components, metric sizing, and immediately catching the projectile to minimize danger. The only purchased component is the winch, and the only custom-made component is the piston.

---

## 7. Performance
Unfortunately, the first model imploded partway through its planned service life, as rapid pressure change and shocks degraded the acrylic barrel. We had collected some data at this point, but it was not particularly precise, as the cannon’s performance is faster than our high-speed camera.  

At the maximum setting, with the sensor cropped to the smallest active area that still had enough pixels to image the entire barrel, the ball still appears oblong instead of spherical, which leads to large measurement uncertainty.

---

## 8. Rebuild
Over the course of the 2024–2025 school year, the broken vacuum cannon was disassembled and parts that could not be reused were disposed of. The piston, winch, and balls that were specifically made or ordered for the project were retained and now operate in the rebuilt cannon. Unfortunately, the piston from the first version does not seal as well in the second version's barrel. A new one is needed.

The new cannon has been built with aesthetics in mind, as well as durability. The body of the cannon is [Trespa](https://www.trespa.com/nl_NL/), the barrel is aluminum, and the bolsters are PMMA. As we have not upgraded our measurement equipment, we are still unable to measure the ball’s velocity inside of the barrel, so making the barrel out of a non-transparent material is inconsequential.

---

## 9. Outlook
The most common use for vacuum cannons at universities is as a demo for the public and prospective students at open days. This cannon was designed with this in mind.

![Figure 5: Vacuum Cannon II.](figures/VacCanII.png)

---

## References
1. E. Ayars and L. Buchholtz. *Analysis of the vacuum cannon.* *American Journal of Physics,* 2004.  
2. R. W. Peterson et al. *The ping-pong cannon: A closer look.* *The Physics Teacher,* 43(1):22–25, Jan 2005.  
3. Лифшиц Е. М. (L. D. Landau Ландау Л. Д. and E. M. Lifshitz). *Механика сплошных сред. Гидродинамика и теория упругости (Continuous Media Mechanics. Hydrodynamics and Theory of Elasticity, “Fluid Mechanics").* Гостехиздат, 1944. [Russian first edition](http://books.e-heritage.ru/book/10077925).  
4. L. D. Landau and E. M. Lifshitz. *Fluid Mechanics.* Pergamon Press, 1959. (English translation, likely based on the 1953 edition).  
