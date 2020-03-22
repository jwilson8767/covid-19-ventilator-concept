# COVID-19 Ventilator Concept
This is a ventilator system concept that I think solves several of the major challenges presented (especially cost and material availability), but will need a lot of prototyping to determine if it's viable. DISCLAIMER: I have no medical, engineering (except the software kind), or manufacturing experience and am simply presenting this concept for your consideration.

## Intermittent positive-pressure ventilation to two patients
This ventilator concept is designed to regulate approximately 3.6L of air (IPPV) to **two** patients. It includes only two components: 

##### A reserve canister / cylinder (Component A)

![Component A](/Component%20A.png)

##### A valve manifold (Component B)

![Component B](/Component%20B.png)
 
 In this concept I've sized the canister to use readily available 6in PVC pipe (with minimally modified end caps) and a free-floating chamber separation plug / seal (not sure the proper name). I arbitrarily chose 2cm diameter tubes for my concept, but any size should be possible with minimal adaptation. The valve manifold is designed to be CNC machined from a single piece of stock material (reductive manufacturing), but has additional parts for each valve. Rotating half-circle valves are actuated by a small electric motor (that should have speed controls!). These valves may not work at all as I have no experience with pneumatic valves, but the real concept here is to 1) centralize parts requiring precision to as few parts as possible and 2) synchronize the four one-way valves (V1-4) so that air is flowing through V1 and V4 at the same time, then V2 and V3, and back to V1 and V3, such that the free-floating plug alternates back and forth in the cylinder.

A few dimensions I baked into this design that will definitely need to be reviewed by a medical professional:
- Tube diameter (currently 2cm)
- Valve diameter / throughput (tried to stay consistent at 2cm)
- Inspiration air volume (3.6L is based on an adult male's IRV, but is *way* too much for females.)
- I have no idea what the thickness of the plug should be, just be careful in sizing it so it cannot skew sideways in the cylinder, thereby jamming the ventilator.

## Materials
I don't know enough to dictate what materials should be used for any parts in this contraption, but from my limited knowledge of plastics:
 - I would suggest that delrin plastic could be a decent choice for the plug and possibly some of the moving valve parts as it is somewhat self-lubricating. Alternatively, the plug could be almost any plastic with a rubber seal around the outside. 
 - I imagined the manifold base and face plate being CNCed from clear acrylic because it would look cool and finding acrylic stock that is ~3cm thick shouldn't be too too hard (or perhaps thinner pieces could be glued together prior to machining).
 - As mentioned above, 6in PVC pipe forms the body of the cylinder (though tube fittings could be of any material)

## Air supply
Air supply may be delivered via any compressed air source, and filter either pre-ventilator or post-ventilator. I imagine that, in a pinch, portable air compressors (the kind that run air tools) could be used, perhaps in a bank of multiple compressors to provide redundancy / overcome duty cycle limitations. I read somewhere that 50PSI was required for inspiration, which sounds high to me, but regardless this concept should be able to be used for any pressure given the right materials.

## Expiration
This ventilator concept is only concerned with providing positive pressure for inspiration, relying on natural lung elasticity and pressure differential for expiration.

## Limitations
- When ventilating two patients at once, both will receive the same volume of air at the same pressure and should therefore have very close to the same size lungs. 
- This ventilator concept makes no provisions for oxygen or CO2 sensing. In that way it is a "dumb" ventilator and relies on functional alveoli and medical personnel to get supplemental oxygen balanced correctly. 
- This ventilator concept has NO ALARMS and NO COMPUTERS. 
- The input pressure is the pressure that will be applied to the patients, and the speed of the electric motor sets the rate of inspiration. There will be some threshold below which the input pressure is not enough to fully actuate the cylinder
- This ventilator concept doesn't try to address face mask / intubation / whatever that bubble head thing is.


## Next steps
I don't have any plans to attempt to build this ventilator myself, but offer it up to the world in the hope that it *inspires* (pun intended) someone out there. Please use it in your hackathon or however! If you have any questions please open an issue on this repository.

## LICENSE AND DISCLAIMER
Copyright 2020 jwilson8767 on GitHub

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
