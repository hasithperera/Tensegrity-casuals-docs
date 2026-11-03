---
marp: "true"
paginate: "True"
footer: Tensegrity | Casuals
theme: neobeam-neonbeam
---
 # Workshop 2: Slides on the go !
Team Casuals | Tensegrity
Hasith Perera, Justin Hsu, David Niemczura, and Jaylin Washington
<!-- _class: title -->

---
# SMILE  - Alternate design
- Rejected due to design timeline constraints
- Would require custom Hardware and Electronic design 

![bg right contain](res/Pasted%20image%2020261014231026.png)

---


<!-- _header: "Yale PCB constraints Desing" -->

![bg right contain](res/Pasted%20image%2020261009191118.png)

- This is the Yale control board; the COTS board has everything you need and more, but the physical dimensions are not feasible
- We are leaning toward a custom PCB order with a minimum design
	- Remove force feedback, but maintain the form factor
	- Add the current module 
---
![bg contain](res/Pasted%20image%2020261020184109.png)

---
<!-- _header: "Our modifications" -->

![bg right contain](res/Pasted%20image%2020261020182220.png)

## Removed:
- Force feedback and all capacitive sensors
- MOSFET's designed for the electro magnets

---
![bg contain](res/Pasted%20image%2020261020182246.png)

---
![bg contain](res/Pasted%20image%2020261020182541.png)

---
<!-- _header: " Initial proposed time line" -->

![bg contain](res/Pasted%20image%2020261020182445.png)

---

 # Workshop 3: Update
Team Casuals | Tensegrity
Hasith Perera, Justin Hsu, David Niemczura, and Jaylin Washington
<!-- _class: title -->

---
# Updated and current time line

![bg right contain](res/Pasted%20image%2020261103130828.png)

- Additional constrains and resubmission of the BOM added a week of delay
- Item review and delivery/pickup again added ~ 1.5 weeks 
- Lab space/soldering access has not been provided yet
---
# Progress

- **Justin and Hasith** put together a model to see how this design will work and maintain stability
	- it works on a ratchet mechanism
- We found that the fixed string length is a constraint we have to tune. (This is not specified in any of the public documents)

![bg contain right ](res/Pasted%20image%2020261103131302.png)

---
# Current issues we are thinking about - Controls (Hasith)

- The controller Yale design is using is a **Nano 33 IoT**
	- This is a single core 
	- they are not using interupts in there code
	- using UDP packets to get data in and out of the 3 structs
	- no close loop controllers are running in the struts
		- Would putting 4 encoder signals break the speed required for UDP data
	- Should we upgrade to a dual core processor 
		- can be done
