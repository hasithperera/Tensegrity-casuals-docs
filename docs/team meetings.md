## Task list and timeline

- [x] Document the model - pull some dimensions #David 📅 2026-10-16 ✅ 2026-10-15
	- 50-70% 
- [x] Make a scale-down mock model 📅 #Justin ⏳ 2026-10-16 ✅ 2026-10-15
- [ ] Look into the PCB - remake it 📅 2026-10-16 #Hasith
	- [x] Completed the PCB review ✅ 2026-10-09
	- [ ] KiCad redesign📅 2026-10-12 
- [ ] Potential 2nd design: #Garren
- [ ] BOM - translation to our case (ASAP)
	- Mechanical #David #Jaylin
	- Electronics #Hasith 
- [x] Schedule a meeting with Lu: #Hasith ✅ 2026-10-15
	- Thursday afternoon - email her about a meeting
	- [x] Talk about the high-level plan ✅ 2026-10-09
	- [x] Controller design - external controller ✅ 2026-10-09
---
# PCB dimensions from Yale

![bg right contain](res/Pasted%20image%2020261009191118.png)

- This is the Yale control board; the COTS board has everything you need and more, but the physical dimensions are not feasible
- We are leaning toward a custom PCB order with a minimum design
	- Remove force feedback, but maintain the form factor
	- Add the current module 
---
# Sensor and data availability: single node 

- Each node will have
	- 9 DOF from the IMU
	- 2 Motor rotation counts 
	- 2 Current sensor data
- Inputs
	- Motor rotation with counts 
- Data via MQTT - basically the same as a ROS msg without the complications of ROS
---
# Program design 

- Each node will run the same basic firmware - sensor interface and motor drive
	- Send data via MQTT
	- High-speed sensor out via wifi (on request)
- Run the control algorithms on a Raspi/Laptop on the same network
- ROS is a possibility
	- I have done some basics about 10 years ago - on a Raspi
	- This feels like a complication at this stage since I am the only one who does software
---
# Questions

- Can we do an external controller? It's not a self-supported robot - **IS THIS OK ?**
	- I think this would be more fun for me to do
- What is the timeline for funding and fabrication?  - **Custom PCB's take time**
- I am concerned about the force feedback not being there 
	- Counts can only give you perceived inputs and not actually what's going on in the real system
	- This can go very wrong just because of the DOF on the system
- What's the use of the IMU?
	- obviously orientation, but that's kind of complicated
	- I think Yale folks had a forward model and a state estimator running in the background to predict the moves
- Electromagnet?
---
## SMILE design

- Probably more feasible 
- Paper from her website: https://smile-robotics-lab.github.io/assets/documents/papers/Tensegrity-Blocks.pdf
- Carbon rods ?
	- Looks like they are bending when the forces are applied
- Do you know the cost for this
	- 8 corners, X 2 motors each 
		- 16 motors, only 12 edges - so some motors are not needed
		- encorders? yes
		- Force feedback? probably no
---

![173](res/Pasted%20image%2020261014231026.png)

---

# Meeting with Luyang

- Force feedback is not needed apparently; it never worked, it seems
- External controller is fine if we do Yale
- Yale design: I think it's the fun way to do it (controller wise)
- She showed the central controller design 
	- This has carbon fiber and springs already to take that fall as opposed to Yale will have to do it on the run time
	- From a comp point of view: central + bar design is the way to meet their criteria 
		- Yale is easy for all of us: no redesign, we just follow the things they have done and just redo it, nothing new
---

![639](res/Pasted%20image%2020261015161732.png)

---

## Hasith's proposal 

- We do both; ask for more money for the 12-motor design 
	- Needs a design + BOM
	- We try Yale; if it fails, then we still have the components to do the other design
		- Mechanical design needs to be done 
		- Electronics need to be figured out to control 12 motors (this is also probably not easy to fit in that structure)
	- https://www.youtube.com/watch?v=YznAy63wcdw : Possible control system and gate
		- there are apparently a lot of implementations out there