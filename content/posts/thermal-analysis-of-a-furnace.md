---
title: Thermal Analysis of a Furnace
subtitle: Hemispherical Bangle Making Furnace
category:
  - Modeling & Simulation
  - Fluid Dynamics
  - Heat Transfer
  - Mechanical Engineering
author: Rutvik Solanki
date: 2020-11-28T13:00:25.827Z
featureImage: /uploads/furnace-bg.png
---
### Quick background on the impact of Project( Skip it, Techies)

Glass bangles are manufactured by skilled artisans in several clusters in Northern India.

Bharatpur in Rajasthan has several artisans engaged in this activity traditionally. Considered very auspicious for weddings across the state of Rajasthan, these bangles are intended to be made joint-less. This makes the crafting process different from their counterparts of Firozabad where jointed bangles are produced. Bharatpur is house to 14 of these bangle-making furnaces operated on loose biomass. The artisans in Bharatpur have been facing several difficulties in the use of traditional furnaces and tools. In the village Unch, in Nadbai block of Bharatpur district, LUPIN Foundation, an NGO has
been working for the betterment of the artisans. At the request of LUPIN Foundation. The Rural Technology Action Group (RuTAG) IIT Delhi has taken the initiative for finding solutions to the problems faced by the artisans engaged in manufacturing glass bangles. The present paper presents the solutions proposed and their implementation in the field.

## Let's Get Technical

### Design of Furnace

A furnace consists of a converging draft chamber. There are 4 layers in the boundary. The most outer part of the furnace is of Iron which helps to furnace to remain in its shape because when the furnace is heated due to expansion the inner layer of boundary tries to expand. Inside this Iron layer, there is a layer of Alumina wool blanket which is used as insulation. So that heat loss through the boundary is minimum. Inside this layer, there is a layer of clay and inside this, there is insulation on the inner side of the furnace. The furnace consisting of 1 primary opening and 16 secondary openings.

The Primary opening is used to feed fuel and secondary openings are used for the fed glass to be
melted. The flue gases released during combustion travel through the converging furnace
driven by the natural draft of air coming through the opening. And air along with flue gases
enters into the chimney. And flue gases comes of the chimney into ambient air

![CAD Design of Traditional Furnace](/uploads/furnace-intro.png "Traditional Furnace Design")

The equation for one-dimensional conduction through the spherical surface is applicable in this case as the given furnace’s shape can be approximated to be hemispherical. The equivalent thermal can be calculated by summing up the conductive and convective resistances which are in series and the overall resistance to heat transfer can be calculated. With both of these, we can calculate the heat loss through the furnace with an inside temperature T. For the first law analysis, we have studied Applied Thermodynamics by Eastop and McConkey. If the interior furnace is taken as our system it can be viewed as a control volume with the steady flow (at steady state) with air entering the system and flue gases exiting. The steady flow equation can be written for the system in which the internal energy of the system remains constant. The work component in the steady flow equation only contains the flow work which is caused by the fluid moving across the system boundary (Win = 0).

![Conservation Equations](/uploads/eq1.png "Conservation Equations")

To calculate the mass flow rate of the inlet air required to achieve a certain furnace temperature has to be calculated. So conservation of energy analysis for flowing fluids with Bernoulli’s equation. Equations for the pressure of the fluid in different zones in the furnace can be used for calculating losses in the pressure (head loss) due to friction and also losses to do sudden expansion and compression which occur at entrances and exits. There is also a head loss term due to the gate valve present in the chimney. The inner surface of the chimney is the ceramic fiber blanket and the flow is assumed to be turbulent. Darcy Weiselbach equation is used to calculate the head loss in the chimney and contraction, expansion losses are also accounted with their resistance coefficients (0.5 and I respectively), The friction factor is taken to be a function of Reynolds number and the relative roughness. Haaland approximation is used to calculate the friction factor for the chimney surface. We have to assume a uniform density of air along with the chimney height.

The furnace can be taken as a steady flow system with no work done by
or on the system. The steady flow equation gives the relation between the heat added and lost
in the system and the change in the enthalpy of inlet and outlet flow along with the change
in potential energy. By the exhaust gas analysis, we can calculate the mass flow rate of flue
gases. By using this along with the steady flow equation we can get the mass of fuel required to
generate the furnace temperature. The mass flow rate Of air inflow has to be estimated along
with the loss factors which are associated with the flow in the furnace. so we do a fluid flow
energy analysis. From the flue gas analysis, we can get the relation between inlet air flow and
the exhaust flue gas mass flow rate. The equations can be written as a function of the inlet
mass flow rate and the inlet mass flow rate can be evaluated for a certain conversion factor
between inlet and exhaust flow rates.

For estimating the temperature of walls and the heat loss, we considered the combined effect
of conduction, convection, and radiation. In the interior, the main conducting element from
the center to walls is air and we are considering the same temperature everywhere inside,
thus considering a major effect of the convective air transfer and estimated the heat transfer
Coefficient.

![wall Equations](/uploads/wall_equations.png "Wall Equations")

To get the solutions for the temperature for evaluating the net attainable steady-state temperature for the given parameters, the following [code](https://drive.google.com/file/d/1pGtLCVNLzW5pb_cD0pGyGzb1tb_PEWwN/view?usp=sharing) has been written in Matlab. The code solves uses [Darcy–Weisbach](<https://en.wikipedia.org/wiki/Darcy%E2%80%93Weisbach_equation#:~:text=Pressure%2Dloss%20form,-In%20a%20cylindrical&text=%2C%20the%20mean%20flow,also%20called%20flow%20coefficient%20%CE%BB).&text=%CE%BC%20is%20the%20dynamic%20viscosity,kg%2F(m%C2%B7s))%3B>) equations along with general pressure drop equations for turns and pipes. These sets of pressure drop Equations are solved iteratively for attaining the steady state solution to the problem.