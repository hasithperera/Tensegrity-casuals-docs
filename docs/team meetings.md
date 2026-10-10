## Task list and timeline

- [ ] Document the model - pull some dimensions📅 2026-10-16 #David
- [ ] Make a scale-down mock model 📅 ⏳ 2026-10-16 #Justin
- [ ] Look into the PCB - remake it 📅 2026-10-16 #Hasith
- [ ] Potential 2nd design: #Garren
- [ ] BOM - translation to our case (ASAP)
	- Mechanical #David #Jaylin
	- Electronics #Hasith 
- [ ] Schedule a meeting with Lu: 
	- Not Thursday afternoon - email her about a meeting
	- Talk about the high-level plan
	- Controller design - external controller 
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
