---
layout: project
title: Heat Exchanger Analysis
description: Thermodynamics Mini-Lab Activity
technologies: [In-lab tools, Mathematics, Thermodynamic equations]
image: /assets/images/Thermo_HE_1.png
---

A heat exchanger is used to transfer thermal energy from one fluid to another without them actually mixing. They are used everywhere, such as power plants, refrigeration, air conditioners, and electric generation. Above is the photo of what a heat exchanger looks like. Below is a cross sectional look at the heat exchanger from one end.

![Heat Exchanger]({{ "/assets/images/Thermo_HE_2.png" | relative_url }}){: style="width: 600px"}

In a mini-lab activity for my thermodynamics class at Cornell, I observed parallel flow vs counter flow heat exchanger through measuring the inlet and outlet temperature of both cold and hot water. Below are photos of the heat exchanger setup in the lab. The first one is the parallel flow setup while the second one is the counter flow setup.

![Parallel Flow]({{ "/assets/images/Thermo_HE_Setup1.png" | relative_url }}){: style="width: 600px"}

![Counter flow]({{ "/assets/images/Thermo_HE_Setup2.png" | relative_url }}){: style="width: 600px"}

A solid wall usually separates the hot and cold fluids that flow through the heat exchanger. Heat moves from the hotter fluid to the cooler fluid through the wall, which is known as conduction. The fluids' flow carries heat energy throughout the system, which is known as convection. 

Below is a diagram that depicts an ideal heat exchanger system. I am assuming that the system is steady state control volume, the change in kinetic and potential energies can be neglected, the system is adiabatic, and there is no work done. We could see how the heat loss by the hot fluid is equal to the heat gain of the cold fluid. This heat transfer is primarily driven by temperature difference of outlet vs inlet of each fluid, assuming that pressure is kept constant.

![First Law]({{ "/assets/images/Thermo_HE_FirstLaw.png" | relative_url }}){: style="width: 600px"}

I also evaluated the entropy generation of the system below:

![Second Law]({{ "/assets/images/Thermo_HE_Entropy.png" | relative_url }}){: style="width: 600px"}

During this lab, my group first measured the temperature of the waters of both parallel and counter flow configurations. We also raised the temperature of the hot water to see if there's a major difference. Below are pictures of the overall lab setup: 

Below are the temperatures that we recorded:

![Results]({{ "/assets/images/Thermo_HE_Results.png" | relative_url }}){: style="width: 600px"}

Parallel flow is when the two fluids enters at the same end and moves in the same direction while counter flow is when the fluids enter opposite ends and thus move in opposite directions in the heat exchanger. From inlet to oulet, the temperature of the cold water has increased while the temperature of the hot water decreased. This would make sense since heat energy is being transferred from the hot to cold water. 

During counter flow, it should be expected that the temperature difference should be more than during parallel flow. As noted before, the cold fluid and hot fluid enter opposite ends during counter flow. Therefore, in this configuration, the hot fluid is always flowing next to colder fluid along the length, which means that the temperature difference between the two is large and nearly uniform. Thus, there is strong heat transfer happening throughout the exchanger. At each end of the exchanger, the outlet temperature is influenced by the inlet temperature of the fluid on the same end, so the overall temperature changes of both fluids are usually larger than parallel flow. On the other hand, in parallel flow, since both the hot and cold fluids are entering from the same end, the temperature difference is initally large but decreases as they move together throughout the exchanger and approach the same temperature. 

These trends are apparent as the outlet temperature of the cold water is around 18.4℃ and the outlet temperature of the hot water is around 23.3℃. It is important to note that in the parallel flow configuration, the temperature of the cold water does not exceed the temperature of the hot water. In counter flow, the temperature of the cold water increased by 14.9 ℃ while in parallel flow, the temperature increased by 16.8 ℃. This is expected. However, our results were interesting when we observed the hot water temperatures. In parallel flow, the hot water decreased by 9.9℃ while in counter flow, the hot water decreased by 7.5℃. This doesn't really align with our understanding of counter flow vs parallel flow because we would expect that the temperature difference for counter flow would be greater than the difference for parallel flow. After consulting with our professor, we thought that this could be due to the low inlet temperature of the hot water. Thus, we repeated the same experiement but raised the initial temperature of the hot water to around 40 ℃. This time, we saw that the cold water increased by 18.2 ℃ in parallel flow and increased by 22.3 ℃ in counter flow. The hot water decreased by 15.1 ℃ in parallel flow and decreased by 18.5 ℃ in counter flow. Now this matches our expectations!

Additionally, while it wasn't present in our initial results when the hot inlet fluid was at a lower temperature, the outlet cold water temperature exceeded the outlet hot water temperature in counter flow. While it may initially seem like a violation of the second law of thermodynamics, this does not because each outlet is actually influenced by the inlet on the same end. So for the cold water coming out of the outlet, it's heated closer to the temperature of the hot water coming in through the inlet since they are both at the same end of the heat exchanger. At the same time, the temperature of the hot water coming out of the outlet is cooled by the cold water coming through the inlet since they are both at the same end of the exchanger. 

One possible reason why the counter flow showed less of a temperature difference in the hot water when the initial temperature was flower was that due to the low inlet temperature of the hot water, it may have not been effective since there might not have been enough temperature difference to efffectively drive the heat transfer. Thus, spreading this difference along the length of the exchanger did not allow for full advantage. However, in parallel flow, since the system utilizes the temperature at the inlet to transfer most of the heat, this may have been more effective for the lower inlet temperature.

Overall, this was a great experience in exploring the difference between parallel vs counter flow in heat exchangers. There were some unexpected results such as the temperature difference not being greater in counter flow but through adjusting and experimenting again, our results matched our theory. 
