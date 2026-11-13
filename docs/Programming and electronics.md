---
marp: "true"
paginate: "True"
footer: "**Tensegrity** **Clemson University**  **Casuals**"
theme: neobeam-neonbeam
---
 # Electronics and Program design progress
Team Casuals |  Hasith Perera
<!-- _class: title -->

---
## 10-Nov 

- Populated a single PCB with the Nano and the motor controller
	- Nano starts heating up
	- 3v3: measured at 2.x V
	- Possible faulty board
- Checked PCB for any stray voltages 
---

## 11-Nov

- Tested the remaining nano 33 IoT boards with USB power, and they both show 3.3v on the out put pin and are not heating up (Tested fresh out the box)
- Unit 1:
	- soldered header pins
	- blink running 
	- 3v3 pin measured: 3.03 V 1629 h
	- Keep it plug in for 15 mins and monitor temp
---
![bg contain](res/Pasted%20image%2020261112094131.png)

---
![bg contain](res/Pasted%20image%2020261112094225.png)

---
## 12 - Nov

- Basic wifi config
	- there is a WifiNINA firmware missmatch 
	- but it connected to the open wifi network and the ips are shown without an issue
	![](res/Pasted%20image%2020261112194118.png)
	- [ ] update the firmware if UDP is not working 🔽 
- [x] UDP basic controllers and python commanding ✅ 2026-11-12
---
- [ ] Find a table clamp/borrow from a lab to mount it to my table
	- get a second wifi interface for my laptop to be able to use both networks
- Motor count limits
	- 13500 counts is the max counts the string on S1A is capable of moving
	- implemented a hard-coded stop at 12500 counts at max speed (255)
		- momentum keeps its moving more I think 
	- PID implementation needs to be done
---
## Basic packet structure

 - xxyyzzpqrs
	 - xx,yy,zz - strut 1/2/3 lengths
- Need to implement a test packet
	- xxyyzzpqrs
		- Check s:  `if packet[10]=='T'` 
		- go to alternate packet spec
			- xxy: speed
			- y = ','
			- z = strut (1/2/3)
			- z = motor id (0/1)
---
### Programming todo`

- [x] Motor drive test ✅ 2026-11-11
	- [x] Motor A - Strut 1 ✅ 2026-11-11
- [x] Encorder testing ✅ 2026-11-11
- [ ] Wifi 
	- [ ] Basic network
	- [ ] UDP testing - async responce
	- [x] Set up my wifi extender as the network interface ✅ 2026-11-12