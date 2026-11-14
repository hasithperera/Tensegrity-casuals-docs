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
## 13-Nov

| exp_id | kp   | kd   | ki  | Notes                              |     |
| ------ | ---- | ---- | --- | ---------------------------------- | --- |
| 3      | 0.45 | 0.02 | 0   |                                    |     |
| 4      | 0.6  |      |     |                                    |     |
| 5      | 0.8  | 0.02 |     |                                    |     |
| 6      | 0.8  | .1   |     |                                    |     |
| 7      | 1.5  | .1   |     |                                    |     |
| 8      | 1.1  | .1   | .2  |                                    |     |
| 9      | .9   | .02  | 0   |                                    |     |
| 10     | 0.6  | 0.02 |     | repeate exp r>f                    |     |
| 11     |      |      |     | same as 10, no delay               |     |
| 12,13  |      |      |     | same as exp 11; repeatability test |     |
| 14,15  |      |      |     | dropped threshold to 10            |     |
| 16,17  | .8   |      |     |                                    |     |
| 18     |      |      |     | wifi firmware updated              |     |

---
## PID tuning experiments

![bg right contain](res/Pasted%20image%2020261114120815.png)

- PID tuning was done using sent out to UDP
- It was noted that data was intermittent
- WifiNINA firmware was updated to see if this was a stability issue - no change after update
- **Sub 2 second move is the goal**
- <mark> Alternate option is serial/MQTT data transport </mark>

---
## PID serial data

![bg right contain](res/Pasted%20image%2020261114131842.png)

- Data manually saved from the serial monitor
- No time reference; during wired testing, this is fine
- Chose the Green line, this is not the fastest but it has the least error
---

- [x] Motor drive test ✅ 2026-11-11
	- [x] Motor A - Strut 1 ✅ 2026-11-11
- [x] Encorder testing ✅ 2026-11-11
- [x] Wifi ✅ 2026-11-14
	- [x] Basic network ✅ 2026-11-14
	- [x] UDP testing - async responce ✅ 2026-11-14
	- [x] Set up my wifi extender as the network interface ✅ 2026-11-12
- [ ] PID controller
	- [x] Tuning and engineering plots to show the tuning ✅ 2026-11-14
	- [x] UDP data send ✅ 2026-11-14
		- This has some stability issues; may be due to its UDP and dropped traffic
	- [ ] MQTT test for high-speed data output 
		- [x] Need to find a way to run an MQTT server on Mac ✅ 2026-11-14
			- Dockers
			- [ ] fix firewall issue 
	- [ ] Test both motors
	- [ ] Implement motor state using global status array
- [ ] Controller interface
	- [x] Basic length set packet ✅ 2026-11-14
	- [ ] Data request packets
		- [ ] Init packet `I`
			- `aaaasbbbbI`
			- contains a 4 digit count for each motor 
			- strut id as seperator
		- [ ] Robot handshake 
---
# Tangent - Docker install on Mac

- https://docs.docker.com/desktop/setup/install/mac-install/
- Followed the tutorial here
- **Docker** is running fine:
	- I can connect to it locally using my Mac
	- but my firewall rules are not allowing in coming connections
		- Talk to IT to add an exception to 1883
- Pending
	- Run it on a Pi or use my linux PC to test it
---
